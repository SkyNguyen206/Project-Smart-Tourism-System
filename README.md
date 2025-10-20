# Đồ Án: Hệ Thống Du Lịch Thông Minh (AI Smart Tour Guide)

Dự án này nhằm mục đích xây dựng một trang web du lịch thông minh, ứng dụng tư duy tính toán và các công nghệ AI cơ bản để giúp người dùng lên kế hoạch du lịch tại Việt Nam một cách cá nhân hóa và hiệu quả.

## 1. Mục Tiêu và Nội Dung Dự Án

### Mục Tiêu Chính
[cite_start]Mục tiêu của hệ thống là phát triển một trang web giúp người dùng tự động tạo ra một kế hoạch du lịch chi tiết dựa trên các yếu tố cá nhân hóa như ngân sách, sở thích, và thời gian[cite: 7, 62]. [cite_start]Hệ thống hướng đến đối tượng khách du lịch tự túc, đặc biệt là người trẻ trong độ tuổi 18-35, đi một mình hoặc theo nhóm nhỏ[cite: 15, 16, 79].

### Các Chức Năng Dự Kiến
Dự án sẽ tập trung vào việc xây dựng 4 trang chính với các chức năng cụ thể:

* **Trang Chủ (Home):** Giao diện giới thiệu tổng quan về dự án và các tính năng chính.
* **Trang Dịch Vụ (Service):** Đây là chức năng cốt lõi của hệ thống.
    * [cite_start]**Tiếp nhận đầu vào:** Người dùng cung cấp thông tin về điểm đến, ngân sách, thời gian, loại hình du lịch (thiên nhiên, mạo hiểm,...) và sở thích (ẩm thực, chụp ảnh,...)[cite: 18, 22, 23, 83].
    * [cite_start]**Xử lý và gợi ý:** Hệ thống sẽ phân tích thông tin đầu vào để đề xuất một lịch trình tối ưu[cite: 9, 11].
    * [cite_start]**Hiển thị bản đồ tương tác:** Lịch trình gợi ý, bao gồm các điểm tham quan, nhà hàng, và khách sạn, sẽ được hiển thị trực quan trên bản đồ[cite: 10, 46]. Bản đồ có khả năng lấy vị trí GPS hiện tại của người dùng để cá nhân hóa lộ trình.
* **Trang Người Dùng (User):** Quản lý thông tin tài khoản, lịch sử các chuyến đi đã tạo.
* **Trang Cài Đặt (Setting):** Cho phép người dùng tùy chỉnh các cài đặt của tài khoản.

## 2. Công Nghệ và Ngôn Ngữ Sử Dụng

Dự án sẽ được phát triển dưới dạng một trang web, sử dụng các công nghệ sau:

* [cite_start]**Ngôn Ngữ Lập Trình:** **Python** là ngôn ngữ chính cho phần backend[cite: 34, 101].
* **Backend Framework:** **Flask** sẽ được sử dụng để xây dựng web server, xử lý logic và định tuyến các trang.
* **Frontend:** Giao diện người dùng sẽ được xây dựng bằng **HTML** và **CSS** cơ bản.
* **Thư Viện Hỗ Trợ (Python):**
    * [cite_start]**`folium`**: Để tạo và hiển thị bản đồ tương tác[cite: 36, 105].
    * [cite_start]**`pandas`**, **`numpy`**: Để xử lý và phân tích dữ liệu đầu vào của người dùng và thông tin các địa điểm[cite: 38, 105].
    * [cite_start]**`geopy`**: Để xử lý các tác vụ liên quan đến vị trí địa lý, như tính toán khoảng cách[cite: 36, 105].

## 3. Cấu Trúc Dự Án

Dự án sẽ được tổ chức theo cấu trúc chuẩn của một ứng dụng Flask để đảm bảo tính rõ ràng và dễ bảo trì:

```
/smart-tourism-project/
|
|-- app.py                  # File Python chính của Flask, chứa logic backend
|
|-- /templates/             # Thư mục chứa các file HTML
|   |-- base.html           # Template cơ sở (chứa navbar, footer)
|   |-- home.html           # Giao diện trang chủ
|   |-- service.html        # Giao diện trang dịch vụ (chứa bản đồ)
|   |-- user.html           # Giao diện trang người dùng
|   `-- setting.html        # Giao diện trang cài đặt
|
`-- /static/                # Thư mục chứa các file tĩnh
    |-- /css/
    |   `-- style.css       # File CSS để tùy chỉnh giao diện
    `-- /images/
        `-- banner-image.jpg # Nơi lưu trữ hình ảnh
```
