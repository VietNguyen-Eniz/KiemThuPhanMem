# MÔN: KIỂM THỬ PHẦN MỀM

# BÁO CÁO KẾT QUẢ CHƯƠNG 1

## 1. Kết quả thực hành trên "Can't Unsee"
Trong bài tập này, em đã thực hiện kiểm thử khả năng quan sát và nhận diện lỗi giao diện (UI) thông qua thử thách đào tạo thị giác.

* **Thứ hạng:** <span style="color: #e5e4e2; font-weight: bold;">MASTER</span> (Perfect ?)
* **Tổng điểm:** 8,130
* **Thời gian hoàn thành:** 04:26

### Minh chứng kết quả:
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/a9286dda-b56d-4987-b1c1-1beb80826be3" />

---

## 2. Phân tích & Bài học rút ra
Việc đạt mức điểm Master cho thấy em đã rèn luyện được các kỹ năng kiểm thử giao diện quan trọng:

1.  **Kiểm thử Pixel-Perfect:** Phát hiện sự sai lệch về khoảng cách (margin/padding) dù chỉ 1-2 pixel.
2.  **Kiểm thử Typography:** Nhận diện sự không đồng nhất về font chữ, độ đậm (weight) và khoảng cách dòng.
3.  **Kiểm thử tính nhất quán (Consistency):** Đảm bảo các thành phần giao diện tuân thủ quy tắc thiết kế chung (Design System).


# Student Analyzer – Unit Testing with JUnit Standalone

## 1. Mô tả bài toán
Bài tập yêu cầu xây dựng một chương trình Java để phân tích dữ liệu điểm số của học sinh, đồng thời viết các ca kiểm thử đơn vị (unit test) bằng JUnit nhằm đảm bảo tính đúng đắn của chương trình.

Chương trình gồm lớp `StudentAnalyzer` với hai chức năng chính:
* **Đếm số lượng học sinh đạt loại Giỏi**: Dựa trên các tiêu chí điểm số hợp lệ.
* **Tính điểm trung bình**: Chỉ tính trên các giá trị điểm nằm trong khoảng cho phép (0 - 10).

---

## 2. Các chức năng chính

### 2.1. `countExcellentStudents(List<Double> scores)`
* **Mô tả**: Đếm số học sinh có điểm **>= 8.0**.
* **Xử lý logic**: Bỏ qua các điểm không hợp lệ (< 0 hoặc > 10), bỏ qua giá trị `null`. Trả về **0** nếu danh sách rỗng.

### 2.2. `calculateValidAverage(List<Double> scores)`
* **Mô tả**: Tính điểm trung bình của các điểm hợp lệ (0–10).
* **Xử lý logic**: Loại bỏ điểm không hợp lệ và `null`. Trả về **0** nếu không có điểm hợp lệ nào.

---

## 3. Cấu trúc thư mục dự án
```text
unit-test/
├── lib/
│   └── junit-platform-console-standalone-1.13.0-M3.jar
├── src/
│   └── StudentAnalyzer.java
├── test/
│   └── StudentAnalyzerTest.java
└── README.md

```

* `lib/`: Chứa các thư viện bên ngoài cần thiết cho dự án.
* `src/`: Chứa mã nguồn thực thi chính của chương trình.
* `test/`: Chứa các kịch bản kiểm thử đơn vị bằng JUnit 5.

---

## 4. Công cụ và công nghệ sử dụng

* **Ngôn ngữ lập trình**: Java (JDK 8 trở lên).
* **Thư viện kiểm thử**: JUnit 5 (sử dụng `junit-platform-console-standalone` để chạy kiểm thử mà không cần Maven/Gradle).
* **Môi trường phát triển**: Visual Studio Code.
* **Quản lý mã nguồn**: Git và GitHub.

---

## 5. Hướng dẫn chạy kiểm thử đơn vị (JUnit)

### 5.1. Yêu cầu môi trường
- Đã cài đặt **Java JDK 8+**
- Đã cấu hình biến môi trường `JAVA_HOME`
- Có file `junit-platform-console-standalone-1.9.x.jar` trong thư mục `lib/`

### 5.2. Biên dịch mã nguồn
Mở terminal tại thư mục gốc của project và chạy:

```bash
javac -cp ".;lib/*" src/*.java test/*.java
```

### 5.3. Chạy kiểm thử đơn vị

Sau khi biên dịch thành công, chạy lệnh sau:

```bash
java -jar lib/junit-platform-console-standalone-1.9.x.jar --class-path . --scan-class-path
```
### 5.4. Kết quả

- Nếu tất cả test **PASS**, JUnit sẽ hiển thị tổng số test thành công
- Nếu có test **FAIL**, hệ thống sẽ hiển thị chi tiết lỗi để sinh viên sửa mã nguồn

### Kết quả kiểm thử thực tế:
<img width="1919" height="1020" alt="Image" src="https://github.com/user-attachments/assets/8bdb023b-f606-4761-867e-00448e291830" />

---

## 6. Danh sách ca kiểm thử

- Danh sách điểm hợp lệ và không hợp lệ
- Danh sách rỗng
- Danh sách chỉ chứa giá trị biên (0 và 10)
- Danh sách chứa điểm âm hoặc lớn hơn 10

---

## 7. Kết luận

Thông qua bài tập này, em đã nắm vững:

* **Thiết kế Test Suite**: Biết cách xây dựng các bộ kiểm thử bao phủ các trường hợp biên và dữ liệu bất thường.
* **Sử dụng JUnit 5**: Thành thạo việc sử dụng các Assertions để xác minh tính đúng đắn của logic.
* **Tổ chức dự án**: Hiểu quy trình tổ chức dự án Java theo cấu trúc `src/test` tiêu chuẩn.
* **Kỹ năng công nghệ**: Biết cách sử dụng Git để quản lý phiên bản mã nguồn và ứng dụng AI hỗ trợ trong quá trình lập trình.
javac -cp ".;lib/junit-platform-console-standalone-1.10.2.jar" src/StudentAnalyzer.java test/StudentAnalyzerTest.java



