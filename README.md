[README.md](https://github.com/user-attachments/files/30437007/README.md)
# TamThai Smart PWA — Sprint 01

Sprint 01 cung cấp khung Progressive Web App (PWA) mobile-first cho **Trợ lý số UBND xã Tam Thái**. Bản này chạy hoàn toàn bằng dữ liệu mẫu, không lưu hoặc gửi dữ liệu người dùng.

## Có trong Sprint 01

- Splash, Welcome và Trang chủ theo Material Design 3.
- Điều hướng SPA bằng hash router, không tải lại trang.
- Bottom navigation, component dùng lại, trạng thái màn hình trống cho các sprint sau.
- Light/dark theme lưu trên thiết bị.
- PWA manifest, service worker và app shell offline.
- Các điểm tích hợp được chuẩn bị trong `assets/js/config.js`.

## Chạy thử trên máy tính

Không mở `index.html` trực tiếp vì service worker cần một web server. Trong thư mục `tamthai-smart-pwa`, chạy một web server tĩnh (ví dụ Live Server trong VS Code), sau đó mở địa chỉ localhost được cung cấp.

## Chạy thử trên điện thoại

1. Đưa thư mục này lên một hosting HTTPS (GitHub Pages, Firebase Hosting hoặc Apps Script Web App).
2. Mở URL bằng Chrome trên Android hoặc Safari trên iPhone.
3. Chọn **Thêm vào màn hình chính / Add to Home Screen** để cài như ứng dụng.

Chi tiết triển khai có trong [DEPLOYMENT.md](./DEPLOYMENT.md).

## Cấu trúc

```text
tamthai-smart-pwa/
├── assets/
│   ├── css/                 # Design token và giao diện
│   ├── icons/               # Biểu trưng ứng dụng
│   └── js/                  # Router, component, màn hình, cấu hình
├── index.html               # App shell
├── manifest.json            # Khai báo PWA
├── service-worker.js        # Offline cache
└── DEPLOYMENT.md            # Hướng dẫn đưa lên web
```

## Lộ trình kết nối

- **Sprint 02:** Apps Script REST API; Google Sheets cho tin tức, thông báo, lịch và thủ tục.
- **Sprint 03:** Claude AI + RAG; màn hình chat và lịch sử hội thoại.
- **Sprint 04:** Zalo OA, webhook và broadcast.

Không đưa API key, token Zalo, App Secret hoặc Sheet ID vào frontend. Các bí mật chỉ nằm trong Script Properties của Google Apps Script.
