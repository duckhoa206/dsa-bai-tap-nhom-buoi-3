# Mã nguồn – Khoa

[← Workspace Khoa](../README.md) · [Hướng dẫn chung](../../HUONG_DAN_BAT_DAU.md) · [Tiến độ](../../TIEN_DO.md) · [Quy ước tích hợp](../../ma_nguon_chung/QUY_UOC_TICH_HOP.md)

## Phụ trách và đóng góp

- **Phụ trách:** Phạm Đức Khoa.
- **Đóng góp:** Huy cung cấp Merge Sort nội; Thiện cung cấp định dạng tệp; Quân cung cấp yêu cầu log/kiểm thử.

## Cần viết

Tạo `merge_sort_ngoai.cpp` gồm các phần:

- Phân tích và kiểm tra tệp đầu vào.
- Đọc từng khối vừa bộ nhớ, gọi Merge Sort nội và ghi các run ban đầu.
- Trộn hai run theo luồng, không nạp toàn bộ run vào RAM.
- Lặp các lượt trộn cho đến khi còn một run kết quả.
- Quản lý tệp tạm, xử lý lỗi và dọn dẹp an toàn.
- Ghi thời gian, số lượt trộn và kích thước run/khối.

Tệp gốc không được ghi đè trước khi có kết quả hợp lệ.
