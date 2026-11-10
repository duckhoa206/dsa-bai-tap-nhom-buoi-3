# Kiểm thử – Huy

[← Workspace Huy](../README.md) · [Hướng dẫn chung](../../HUONG_DAN_BAT_DAU.md) · [Tiến độ](../../TIEN_DO.md) · [Kiểm thử chung](../../kiem_thu/)

## Phụ trách và đóng góp

- **Phụ trách:** Châu Kim Huy.
- **Đóng góp:** Khoa chạy lại các test trước khi tích hợp.

## Ca kiểm thử bắt buộc

- Mảng rỗng; 1 và 2 phần tử.
- Kích thước là lũy thừa của 2 và không phải lũy thừa của 2.
- Tăng dần, giảm dần, tất cả bằng nhau, nhiều giá trị trùng.
- Số âm, số dương và giá trị thập phân.
- Mảng ngẫu nhiên nhiều kích thước, đối chiếu với `std::sort`.

Mỗi test phải kiểm tra cả thứ tự và việc bảo toàn số phần tử.
