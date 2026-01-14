# BÀI TẬP VỀ NHÀ – MÔN KIỂM THỬ PHẦN MỀM  
## Bài tập Tuần 1
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/a9286dda-b56d-4987-b1c1-1beb80826be3" />

# Student Analyzer – Unit Testing with JUnit Standalone

## Mô tả
Chương trình phân tích điểm số học sinh và kiểm thử đơn vị bằng JUnit Platform Console Standalone.

## Chức năng
- Đếm số học sinh đạt loại Giỏi (>= 8.0)
- Tính điểm trung bình các điểm hợp lệ (0–10)

## Cấu trúc thư mục
- src/: mã nguồn chính
- test/: mã kiểm thử
- lib/: thư viện JUnit standalone

## Cách chạy kiểm thử

### Compile
```bash

javac -cp ".;lib/junit-platform-console-standalone-1.10.2.jar" src/StudentAnalyzer.java test/StudentAnalyzerTest.java
