# Mã nguồn – Thiện

[← Workspace Thiện](../README.md) · [Hướng dẫn chung](../../HUONG_DAN_BAT_DAU.md) · [Tiến độ](../../TIEN_DO.md) · [Quy ước tích hợp](../../ma_nguon_chung/QUY_UOC_TICH_HOP.md)

## Phụ trách và đóng góp

- **Phụ trách:** Nguyễn Ngọc Thiện.
- **Đóng góp:** Khoa xác nhận định dạng đầu vào; Quân xác nhận tham số benchmark.

## Cần viết

Tạo `generate_data.cpp` với các yêu cầu:

- Nhận tên tệp, số phần tử, seed và khoảng giá trị.
- Kiểm tra tham số trước khi tạo tệp.
- Sinh `long double` hữu hạn và ghi tệp ở chế độ binary.
- Ghi theo buffer, không lưu toàn bộ dữ liệu trong RAM.
- Báo seed, số phần tử, dung lượng và thời gian sau khi hoàn tất.
- Trả mã lỗi khác 0 khi không mở/ghi được tệp.

Không commit tệp `.bin` dung lượng lớn vào thư mục này.
