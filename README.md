 (cd "$(git rev-parse --show-toplevel)" && git apply --3way <<'EOF' 
diff --git a/README.md b/README.md
index 8b137891791fe96927ad78e64b0aad7bded08bdc..3e44028f3b3657d63fbc043a8d1d805e1765ecf6 100644
--- a/README.md
+++ b/README.md
@@ -1 +1,21 @@
+# Точное время
 
+Небольшой сайт, который показывает текущее точное время и дату в реальном времени.
+
+## Где открывать
+
+- Основная страница: `docs/index.html`
+- Файл `index.html` в корне делает автоматическое перенаправление в `docs/index.html`, чтобы избежать ошибки `Not Found` в разных конфигурациях хостинга.
+
+## Локальный запуск
+
+Из корня репозитория:
+
+```bash
+python3 -m http.server 8000 --bind 0.0.0.0
+```
+
+Откройте:
+
+- <http://localhost:8000>
+- если не открылось автоматически: <http://localhost:8000/docs/index.html>
 
EOF
)
