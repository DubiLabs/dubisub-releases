<div align="center">



<a href="https://dubi.ericisme.cloud" target="_blank" rel="noopener noreferrer">

  <picture>

    <source media="(prefers-color-scheme: dark)" srcset="assets/dubisub-logo-dark.svg">

    <source media="(prefers-color-scheme: light)" srcset="assets/dubisub-logo-light.svg">

    <img src="assets/dubisub-logo-light.svg" alt="DubiSub Logo" width="88" height="88">

  </picture>

</a>



# DubiSub



Dịch video, tạo phụ đề và lồng tiếng trên Windows.



[![Release](https://img.shields.io/github/v/release/DubiLabs/dubisub-releases?color=6A4DFF&label=Release)](https://github.com/DubiLabs/dubisub-releases/releases/latest)



**[Tải DubiSub 1.0.8 · Windows x64](https://github.com/DubiLabs/dubisub-releases/releases/download/v1.0.8/DubiSub-Setup-v1.0.8.exe)**  ·  [Release notes](https://github.com/DubiLabs/dubisub-releases/releases/tag/v1.0.8)  ·  [Trang chủ & gói sử dụng](https://dubi.ericisme.cloud)



</div>



## Làm việc với video



- Quy trình tự động, chỉnh sửa thủ công và xử lý hàng loạt.

- Nhận dạng giọng nói, dịch, tạo phụ đề và lồng tiếng theo tài nguyên đã cài.

- Studio / Review & Clips: nhập video từ tệp hoặc dự án, chọn và chia đoạn, dùng các công cụ AI theo tùy chọn/gói.

- Engine CPU, NVIDIA CUDA và OCR được tải theo nhu cầu trong **Gói tài nguyên**.



## Cài đặt



1. Tải **DubiSub-Setup-v1.0.8.exe**, chạy trình cài Inno Setup.

2. Mở app và chọn tài nguyên phù hợp cấu hình. Không cần cài Python, uv, Git hay compiler.

3. Thiết lập tài khoản/gói sử dụng khi cần và bắt đầu dự án.



Bộ cài tự chọn sáng/tối theo Windows và hiển thị rõ phiên bản. Chỉ cần tải **Setup.exe**. Các archive engine và phần `.001`/`.002` trong Releases do ứng dụng tự tải, kiểm hash và ghép; không cần tải thủ công. Model lớn không nằm trong bộ cài. Phạm vi hệ điều hành/phần cứng đã kiểm chứng được ghi trong release notes.



**Bản 1.0.8 chưa ký Authenticode.** Windows có thể hiển thị Unknown publisher/SmartScreen. Tệp `.exe.sha256` đi kèm dùng để đối chiếu bản tải. Sao lưu dữ liệu quan trọng trước khi nâng cấp.



## Dữ liệu và dịch vụ



Video, project, model và API key riêng được lưu trên máy. Server DubiSub quản lý tài khoản, quyền sử dụng, quota và thanh toán. Khi bạn chọn AI cloud hoặc đăng mạng xã hội, dữ liệu cần thiết sẽ được gửi tới nhà cung cấp tương ứng; API bên thứ ba có chính sách phí riêng. Cần mạng khi xác minh quyền và bắt đầu job; vẫn có thể xem/chỉnh/lưu dự án và output khi offline.



## Phân phối và giấy phép



Đây là repository phân phối bộ cài và artifact, không chứa repository source riêng. Các gói chạy vẫn có tài nguyên giao diện và có thể bị phân tích ngược. Thư viện, font, codec và model giữ giấy phép riêng; thông báo đi kèm trong app. Nguồn tương ứng của các thành phần không thay đổi tiếp tục có trong [ThirdPartySources tại v1.0.7](https://github.com/DubiLabs/dubisub-releases/releases/download/v1.0.7/DubiSub-1.0.7-ThirdPartySources.zip).



Checkpoint OmniVoice có điều kiện **CC BY-NC**; việc mua DubiSub không cấp quyền thương mại cho checkpoint này.



Phát triển bởi **DubiLabs · Ericismee**.

