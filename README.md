 (cd "$(git rev-parse --show-toplevel)" && git apply --3way <<'EOF' 
diff --git a/README.md b/README.md
index 8b137891791fe96927ad78e64b0aad7bded08bdc..f749aafb2ca5d9148066fe5a895ae1c2454d19c6 100644
--- a/README.md
+++ b/README.md
@@ -1 +1,23 @@
+# Точное время
 
+Простой статический сайт с часами, который показывает текущее время и дату и обновляется каждую секунду.
+
+## Структура
+
+- `docs/index.html` — основная страница сайта с часами.
+- `index.html` — страница-переадресация на `docs/index.html`.
+
+## Запуск локально
+
+```bash
+python3 -m http.server 8000 --bind 0.0.0.0
+```
+
+Откройте в браузере:
+
+- `http://localhost:8000`
+- `http://localhost:8000/docs/index.html` (если редирект отключён)
+
+## Публикация
+
+Для GitHub Pages выберите Source: **Deploy from a branch** и папку **/docs**.
 
EOF
)
