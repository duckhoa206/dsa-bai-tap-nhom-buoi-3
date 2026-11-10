# Mã nguồn – Huy

[← Workspace Huy](../README.md) · [Hướng dẫn chung](../../HUONG_DAN_BAT_DAU.md) · [Tiến độ](../../TIEN_DO.md) · [Quy ước tích hợp](../../ma_nguon_chung/QUY_UOC_TICH_HOP.md)

## Phụ trách và đóng góp

- **Phụ trách:** Châu Kim Huy.
- **Đóng góp:** Phạm Đức Khoa góp ý giao diện tích hợp.

## Cần viết

Tạo `merge_sort_noi.cpp` gồm:

- Hàm trộn hai run liền kề vào vùng nhớ phụ.
- Vòng lặp `runLength = 1, 2, 4, ...`, không đệ quy.
- Xử lý chỉ số cuối bằng giới hạn thực tế của dữ liệu.
- Giao diện hàm đã thống nhất với Khoa.

Không dùng `std::sort` trong phần cài đặt chính; chỉ được dùng làm oracle trong mã test.
