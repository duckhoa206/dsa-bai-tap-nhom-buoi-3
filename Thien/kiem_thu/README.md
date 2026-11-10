# Kiểm thử – Thiện

[← Workspace Thiện](../README.md) · [Hướng dẫn chung](../../HUONG_DAN_BAT_DAU.md) · [Tiến độ](../../TIEN_DO.md) · [Kiểm thử chung](../../kiem_thu/)

## Phụ trách và đóng góp

- **Phụ trách:** Nguyễn Ngọc Thiện.
- **Đóng góp:** Quân và Khoa đọc chéo các tệp mẫu.

## Ca kiểm thử bắt buộc

- Số phần tử: 0, 1, 2, 10, 1.000 và một bộ dữ liệu lớn.
- Tham số thiếu, số phần tử âm, khoảng giá trị sai và đường dẫn không ghi được.
- Hai lần chạy cùng seed; hai lần chạy khác seed.
- Kích thước tệp bằng `soPhanTu * sizeof(long double)`.
- Mọi phần tử đọc lại được, hữu hạn và nằm trong khoảng yêu cầu.

Không dùng bộ 30–50 triệu phần tử cho mọi lần test nhanh.
