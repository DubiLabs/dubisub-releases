# Cài tài nguyên phù hợp với máy

[Hướng dẫn](README.md) · [Cài đặt](install.vi.md) · [Trợ giúp](support.vi.md)

Mở **Cài đặt → Gói tài nguyên**. Trang này hiển thị cấu hình máy, bộ khuyến nghị,
dung lượng cần tải, dung lượng trống cần giữ và hướng dẫn khắc phục theo từng gói.

## Bắt đầu

1. Chờ đọc xong CPU, RAM và GPU. Bấm **Kiểm tra lại** nếu vừa giải phóng VRAM hoặc bổ sung runtime.
2. Xem lý do ở **Khuyến nghị cho bạn**, kiểm tra kho tài nguyên và dung lượng trống.
3. Bấm **Cài bộ khuyến nghị**. Runtime còn thiếu được đưa vào hàng đợi; runtime dùng chung chỉ cài một lần.
4. Muốn dùng gói khác, chọn **Tất cả gói**. OCR, Demucs và trình duyệt Douyin là tùy chọn.

Cài tài nguyên không tự đổi chế độ xử lý hoặc model đang chọn cho dự án. Chọn CPU/GPU,
model nhận dạng, model dịch và giọng đọc ở phần thiết lập xử lý tương ứng.

## Cách chọn bộ khuyến nghị

- Chưa đọc xong phần cứng: chờ kiểm tra; không mặc định coi máy là thiếu GPU.
- Chưa đạt ngưỡng core: ít nhất 16 GiB RAM lắp đặt và 8 GiB Windows sử dụng được; chưa đề xuất model AI cục bộ.
- CPU hoặc GPU còn dưới 2 GiB VRAM trống: Whisper Small, HY-MT2 CPU Q4, VieNeu.
- NVIDIA đủ điều kiện, còn từ 2 GiB VRAM: ưu tiên bộ nhẹ, có runtime CUDA để dùng Whisper Small trên GPU.
- GPU từ 8 GiB, còn từ 5 GiB: đề xuất Whisper Turbo; giữ dịch Q4 trên CPU.
- GPU từ 12 GiB, còn từ 8 GiB: đề xuất Whisper Turbo và HY-MT2 GPU.

Đây là khuyến nghị thận trọng theo cấu hình và VRAM tại lúc kiểm tra, không thay thế kiểm tra
bộ nhớ lúc chạy và không chặn lựa chọn nâng cao mà chính sách core vẫn hỗ trợ.
Ví dụ GPU 8 GiB vẫn có thể chọn HY-MT2 GPU thủ công nếu đáp ứng điều kiện hiện hành.

## Tránh lỗi khi cài

Trước khi tải mỗi gói cùng runtime phụ thuộc, DubiSub kiểm tra:

- Có nguồn model hoặc archive runtime đúng phiên bản.
- Dung lượng cho tải, giải nén, lắp ghép archive nhiều phần, khôi phục và 2 GiB dự phòng.
- Thư mục nằm trên ổ cục bộ và tài khoản hiện tại ghi được.

Ước tính trên giao diện dùng thông tin kho được đọc nền. Bước cài kiểm tra dung lượng mới
một lần nữa vì ổ đĩa có thể thay đổi. Kiểm tra này không đảm bảo nguồn mạng luôn hoạt động.
Không có tệp kiểm tra quyền ghi nào được giữ lại sau bước kiểm tra thành công.

## Tự khắc phục

- **Tải ngắt / timeout / 429:** kiểm tra Internet, chờ nếu nguồn giới hạn tải, rồi Tiếp tục hoặc Thử lại.
- **401/403/chứng chỉ:** kiểm tra ngày giờ, nguồn tải và proxy của mạng doanh nghiệp; không bỏ kiểm tra TLS.
- **Ổ đầy:** Chuyển vị trí đến ổ cục bộ đủ chỗ; giữ thêm chỗ giải nén và khôi phục.
- **Không ghi được / tệp bị khóa:** dừng tác vụ dùng model, đóng tệp và chọn thư mục tài khoản có quyền ghi.
- **Thiếu runtime:** dùng runtime cùng phiên bản, giữ `offline-resources` hoặc vị trí bộ cài đã ghi nhận.
- **Checksum / archive lỗi:** Thử lại hoặc dùng gói chính thức đúng phiên bản. Không sửa checksum để ép cài.
- **Windows Application Control:** xem Protection history, kiểm tra nguồn bộ cài và nhờ quản trị viên duyệt
  nếu là máy quản lý tập trung; giữ các lớp bảo vệ hoạt động.
- **Hết RAM/VRAM:** đóng ứng dụng nặng, xử lý từng tác vụ; chuyển sang bộ nhẹ nếu cần.
- **Model đã cài nhưng lỗi:** menu **⋯ → Kiểm tra và sửa**. Gói và file đã hợp lệ được tái sử dụng khi cơ chế gói hỗ trợ.

Bấm **Hướng dẫn khắc phục** ở gói bị lỗi để xem các bước cùng chi tiết thông báo có thể chọn/sao chép.
Nếu cần hỗ trợ, gửi tên gói, phiên bản DubiSub và chi tiết lỗi; không gửi credential hay API key.
