# Session 11 - Bài 4: Khai báo GitHub Secrets và cấu hình Đăng nhập Container Registry

Dự án Java Spring Boot cấu hình GitHub Actions CI tự động:
1. Checkout mã nguồn
2. Cài đặt Java 17 (Temurin) & Caching Gradle dependencies
3. Cấp quyền thực thi và chạy kiểm thử Unit Test (`./gradlew test`)
4. Đóng gói tệp ứng dụng JAR (`./gradlew bootJar`)
5. Lưu trữ Artifact `app-jar` (`actions/upload-artifact@v4`)
6. Đăng nhập tự động vào GitHub Container Registry (`ghcr.io`) với GitHub Secret `REGISTRY_TOKEN` (`docker/login-action@v3`).
