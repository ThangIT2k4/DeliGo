# DeliGo - Nền tảng đặt món ăn và quản lý đơn hàng thông minh

## Giới thiệu

DeliGo là ứng dụng di động được phát triển trên nền tảng Java, cung cấp giải pháp toàn diện cho việc đặt món ăn và quản lý đơn hàng một cách thông minh và hiệu quả. Ứng dụng kết nối người dùng với các nhà hàng, quán ăn, giúp việc đặt món trở nên dễ dàng và tiện lợi hơn bao giờ hết.

## Tính năng chính

### Dành cho người dùng (khách hàng)
- 🍔 **Đặt món trực tuyến**: Duyệt và đặt món từ hàng trăm nhà hàng
- 🔍 **Tìm kiếm thông minh**: Tìm kiếm món ăn, nhà hàng theo vị trí, loại món
- 📱 **Theo dõi đơn hàng**: Cập nhật trạng thái đơn hàng theo thời gian thực
- 💳 **Thanh toán đa dạng**: Hỗ trợ nhiều phương thức thanh toán
- ⭐ **Đánh giá & Nhận xét**: Đánh giá món ăn và dịch vụ
- 🎁 **Ưu đãi & Khuyến mãi**: Nhận thông báo về các chương trình khuyến mãi

### Dành cho nhà hàng/quán ăn
- 📊 **Quản lý thực đơn**: Thêm, sửa, xóa món ăn dễ dàng
- 📋 **Quản lý đơn hàng**: Xử lý đơn hàng hiệu quả
- 📈 **Thống kê doanh thu**: Xem báo cáo doanh thu chi tiết
- 🔔 **Thông báo đơn hàng mới**: Nhận thông báo ngay lập tức
- 👥 **Quản lý khách hàng**: Theo dõi thông tin và lịch sử đặt hàng

### Dành cho người giao hàng
- 🛵 **Nhận đơn giao hàng**: Xem và nhận các đơn hàng cần giao
- 🗺️ **Định vị và dẫn đường**: Tích hợp bản đồ để dẫn đường tối ưu
- 📍 **Cập nhật vị trí**: Cập nhật vị trí theo thời gian thực
- 💰 **Quản lý thu nhập**: Theo dõi thu nhập từ việc giao hàng

## Công nghệ sử dụng

### Ngôn ngữ và Framework
- **Java**: Ngôn ngữ lập trình chính
- **Android SDK**: Phát triển ứng dụng Android native
- **XML**: Thiết kế giao diện người dùng

### Kiến trúc và Design Pattern
- **MVVM (Model-View-ViewModel)**: Kiến trúc ứng dụng
- **Repository Pattern**: Quản lý dữ liệu
- **Dependency Injection**: Quản lý phụ thuộc

### Thư viện và công cụ
- **Retrofit**: Giao tiếp với API RESTful
- **Room Database**: Lưu trữ dữ liệu local
- **Firebase**: Authentication, Cloud Messaging, Analytics
- **Glide/Picasso**: Tải và hiển thị hình ảnh
- **Google Maps API**: Tích hợp bản đồ và định vị
- **Material Design Components**: Thiết kế giao diện hiện đại

## Yêu cầu hệ thống

- **Android**: Phiên bản 6.0 (API level 23) trở lên
- **Java**: JDK 8 trở lên
- **Android Studio**: Phiên bản mới nhất
- **Gradle**: 7.0 trở lên
- **Kết nối Internet**: Bắt buộc cho hầu hết các tính năng

## Cài đặt và Chạy ứng dụng

### Bước 1: Clone repository
```bash
git clone https://github.com/ThangIT2k4/DeliGo.git
cd DeliGo
```

### Bước 2: Mở project trong Android Studio
- Mở Android Studio
- Chọn "Open an Existing Project"
- Chọn thư mục DeliGo vừa clone

### Bước 3: Cấu hình Firebase (nếu có)
- Tạo project trên Firebase Console
- Tải file `google-services.json`
- Đặt file vào thư mục `app/`

### Bước 4: Cấu hình API keys
- Tạo file `local.properties` trong thư mục root
- Thêm các API keys cần thiết:
```properties
MAPS_API_KEY=your_google_maps_api_key
API_BASE_URL=your_backend_api_url
```
**⚠️ Lưu ý bảo mật**: Không bao giờ commit API keys thật vào repository. File `local.properties` đã được thêm vào `.gitignore` để tránh rò rỉ thông tin nhạy cảm.

### Bước 5: Build và Run
- Sync project với Gradle
- Chạy ứng dụng trên emulator hoặc thiết bị thật

```bash
./gradlew build
./gradlew installDebug
```

## Cấu trúc Project

```
DeliGo/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   └── com/deligo/
│   │   │   │       ├── model/          # Data models
│   │   │   │       ├── view/           # Activities, Fragments
│   │   │   │       ├── viewmodel/      # ViewModels
│   │   │   │       ├── repository/     # Data repositories
│   │   │   │       ├── api/            # API services
│   │   │   │       ├── database/       # Local database
│   │   │   │       ├── adapter/        # RecyclerView adapters
│   │   │   │       └── utils/          # Utility classes
│   │   │   ├── res/
│   │   │   │   ├── layout/            # XML layouts
│   │   │   │   ├── drawable/          # Images, icons
│   │   │   │   ├── values/            # Strings, colors, styles
│   │   │   │   └── menu/              # Menu resources
│   │   │   └── AndroidManifest.xml
│   │   └── test/                      # Unit tests
│   └── build.gradle
├── gradle/
├── build.gradle
├── settings.gradle
└── README.md
```

## Hướng dẫn sử dụng

### Đối với người dùng
1. **Đăng ký/Đăng nhập**: Tạo tài khoản mới hoặc đăng nhập
2. **Tìm kiếm nhà hàng**: Duyệt danh sách hoặc tìm kiếm theo vị trí
3. **Chọn món**: Thêm món ăn vào giỏ hàng
4. **Đặt hàng**: Xác nhận thông tin và đặt hàng
5. **Thanh toán**: Chọn phương thức thanh toán phù hợp
6. **Theo dõi**: Theo dõi trạng thái đơn hàng

### Đối với nhà hàng
1. **Đăng ký tài khoản doanh nghiệp**
2. **Cập nhật thông tin nhà hàng**
3. **Thêm/Chỉnh sửa thực đơn**
4. **Quản lý đơn hàng**: Xác nhận, chuẩn bị, hoàn thành
5. **Xem báo cáo thống kê**

## Đóng góp

Chúng tôi rất hoan nghênh mọi đóng góp cho dự án DeliGo. Nếu bạn muốn đóng góp:

1. Fork repository
2. Tạo branch mới (`git checkout -b feature/TenTinhNang`)
3. Commit thay đổi (`git commit -m 'Thêm tính năng X'`)
4. Push lên branch (`git push origin feature/TenTinhNang`)
5. Tạo Pull Request

### Quy tắc đóng góp
- Tuân thủ coding conventions của Java và Android
- Viết code rõ ràng, có comment đầy đủ
- Thêm unit tests cho các tính năng mới
- Cập nhật documentation khi cần thiết

## Báo lỗi và Hỗ trợ

Nếu bạn gặp bất kỳ vấn đề nào hoặc có đề xuất, vui lòng:
- Tạo issue trên GitHub
- Mô tả chi tiết vấn đề và các bước tái hiện
- Đính kèm screenshots nếu có thể

## Roadmap

- [ ] **Phase 1**: Phát triển các tính năng cơ bản
  - Đăng ký/đăng nhập
  - Duyệt và tìm kiếm nhà hàng
  - Đặt món và thanh toán cơ bản
  
- [ ] **Phase 2**: Tính năng nâng cao
  - Tích hợp định vị và bản đồ
  - Tracking đơn hàng real-time
  - Hệ thống đánh giá và nhận xét
  
- [ ] **Phase 3**: Tối ưu và mở rộng
  - AI recommendations
  - Chatbot hỗ trợ khách hàng
  - Loyalty program
  - Multi-language support

## License

Dự án này được phân phối dưới giấy phép [MIT License](LICENSE). Xem file `LICENSE` để biết thêm chi tiết.

## Tác giả

- **ThangIT2k4** - *Initial work* - [GitHub Profile](https://github.com/ThangIT2k4)

## Liên hệ

- GitHub: [@ThangIT2k4](https://github.com/ThangIT2k4)
- Project Link: [https://github.com/ThangIT2k4/DeliGo](https://github.com/ThangIT2k4/DeliGo)

---

**DeliGo** - Mang đến trải nghiệm đặt món ăn thông minh và tiện lợi! 🍕🚀