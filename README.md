 (cd "$(git rev-parse --show-toplevel)" && git apply --3way <<'EOF' 
diff --git a/README.md b/README.md
index bb216892eb5c969b2c3c473454397361fca7bd36..c7a0472d8afb4c6e47202aa5de2258be160ea326 100644
--- a/README.md
+++ b/README.md
@@ -1,2 +1,18 @@
-# codex
-use a codex
+# 연차 관리 시스템
+
+Flask 기반의 간단한 회사 연차 관리 프로그램입니다. 직원 등록, 연차 신청, 승인/거절 처리를 웹 인터페이스에서 수행할 수 있습니다.
+
+## 실행 방법
+
+1. 가상환경을 생성하고 활성화합니다(선택 사항).
+2. 필요한 패키지를 설치합니다.
+   ```bash
+   pip install -r requirements.txt
+   ```
+3. 애플리케이션을 실행합니다.
+   ```bash
+   flask --app app run --debug
+   ```
+4. 브라우저에서 [http://127.0.0.1:5000](http://127.0.0.1:5000) 으로 접속합니다.
+
+최초 요청 시 자동으로 SQLite 데이터베이스(`leave.db`)가 생성되며, 이후 직원 및 연차 신청 데이터를 저장합니다.
 
EOF
)
