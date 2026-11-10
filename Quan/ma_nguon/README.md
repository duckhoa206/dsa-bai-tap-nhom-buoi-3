# Mã nguồn – Quân

[← Workspace Quân](../README.md) · [Hướng dẫn chung](../../HUONG_DAN_BAT_DAU.md) · [Tiến độ](../../TIEN_DO.md) · [Nơi bàn giao verifier](../../kiem_thu/)

## Phụ trách và đóng góp

- **Phụ trách:** Nguyễn Hoàng Quân.
- **Đóng góp:** Thiện cung cấp định dạng tệp; Khoa cung cấp tệp kết quả để xác minh.

## Cần viết

Tạo `kiem_tra_sap_xep.cpp` với các yêu cầu:

- Nhận đường dẫn tệp nhị phân từ dòng lệnh.
- Kiểm tra kích thước tệp chia hết cho `sizeof(long double)`.
- Đọc tuần tự, không nạp toàn bộ tệp vào RAM.
- Kiểm tra `giaTriTruoc <= giaTriSau`; báo chỉ số và hai giá trị tại lỗi đầu tiên.
- Báo số phần tử, min, max, trạng thái hợp lệ và thời gian xác minh.
- Coi `NaN`, vô cùng hoặc lỗi đọc tệp là dữ liệu không hợp lệ.

Không đặt file biên dịch hoặc dữ liệu lớn trong thư mục này.
