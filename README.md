# Python Turtle Image Drawer

## Giới thiệu
Công cụ này cho phép bạn chuyển đổi một file ảnh bitmap (như `.jpg`, `.png`, `.bmp`) thành các đường nét SVG và sử dụng thư viện `turtle` của Python để vẽ lại ảnh đó. Công cụ này hỗ trợ giảm số lượng màu sắc để tối ưu hóa quá trình vẽ.

## Yêu cầu
- Python 3.x
- Các thư viện cần thiết:
  - `opencv-python`
  - `beautifulsoup4`
  - `numpy`
  - `pywin32` (chỉ trên Windows)
  - `potrace` (cần cài đặt trên hệ thống)

## Cài đặt
1. Cài đặt các thư viện Python cần thiết:
   ```bash
   pip install opencv-python beautifulsoup4 numpy pywin32
   ```
2. Cài đặt `potrace`:
   - Trên Ubuntu/Debian:
     ```bash
     sudo apt-get install potrace
     ```
   - Trên Windows: Tải và cài đặt từ [trang chủ Potrace](http://potrace.sourceforge.net/).

## Hướng dẫn chạy script
Giả sử file `main.py` và hình ảnh nằm trong folder `C:/Code/Python-Turtle-Image-Drawer/`, bạn có thể chạy script như sau:

1. Mở Command Prompt (Windows) hoặc Terminal (Linux/macOS).
2. Di chuyển đến thư mục chứa script:
   ```bash
   cd C:/Code/Python-Turtle-Image-Drawer
   ```
3. Chạy script với cú pháp sau:
   ```bash
   python main.py path/to/image.jpg [-c COLORS]
   ```
   Trong đó:
   - `path/to/image.jpg`: Đường dẫn đến file ảnh trong thư mục `Python-Turtle-Image-Drawer`. Ví dụ: `images/example.jpg`.
   - `-c COLORS` (tùy chọn): Số lượng màu sắc muốn sử dụng để vẽ (mặc định là 32).

### Ví dụ
Giả sử bạn có file ảnh `example.jpg` trong thư mục `images` của dự án, bạn có thể chạy lệnh sau:
```bash
python main.py images/example.jpg -c 16
```

## Chức năng chính
- **Giảm màu sắc**: Công cụ sẽ giảm số lượng màu sắc trong ảnh để tối ưu hóa quá trình vẽ.
- **Chuyển đổi SVG**: Sử dụng `potrace` để chuyển đổi ảnh bitmap thành các đường nét SVG.
- **Vẽ bằng Turtle**: Sử dụng thư viện `turtle` của Python để vẽ lại ảnh dựa trên các đường nét SVG.

## Lưu ý
- Nếu kích thước ảnh quá lớn, công cụ sẽ tự động điều chỉnh kích thước để phù hợp với màn hình.
- Quá trình vẽ có thể mất nhiều thời gian nếu số lượng màu sắc được chọn quá lớn.

## Hỗ trợ
Nếu bạn gặp bất kỳ vấn đề nào, vui lòng liên hệ qua email hoặc tạo issue trên GitHub.

## Giấy phép
Dự án này được phân phối dưới giấy phép MIT. Xem file `LICENSE` để biết thêm chi tiết.
