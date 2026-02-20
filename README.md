(cd "$(git rev-parse --show-toplevel)" && git apply --3way <<'EOF' 
diff --git a/README.md b/README.md
new file mode 100644
index 0000000000000000000000000000000000000000..2cd8966b97f974cd6a4ced51babef8a9da30ac44
--- /dev/null
+++ b/README.md
@@ -0,0 +1,21 @@
+# Сайт с точным временем на Nginx
+
+Небольшой статический сайт, который отображает текущее время с миллисекундами и текущую дату.
+
+## Запуск
+
+Требуется Docker и Docker Compose plugin.
+
+```bash
+docker compose up -d
+```
+
+После запуска сайт доступен по адресу:
+
+- http://localhost:8080
+
+## Остановка
+
+```bash
+docker compose down
+```
 
EOF
)
