# Quy ước tích hợp

Tệp này là hợp đồng chung giữa mã của Thiện, Huy, Khoa và Quân. Nếu cần đổi một quy ước, phải cập nhật tệp này trước khi các thành viên sửa code liên quan.

## 1. Định dạng dữ liệu

- Tệp nhị phân chứa liên tiếp các giá trị `long double`.
- Không có header, metadata hoặc dấu phân cách trong tệp.
- Kích thước tệp phải chia hết cho `sizeof(long double)` trên máy chạy.
- Bộ sinh chỉ tạo giá trị hữu hạn, không tạo `NaN` hoặc vô cùng.
- Các tệp dữ liệu lớn chỉ lưu cục bộ và không commit lên Git.

## 2. Giao diện dòng lệnh dự kiến

### Sinh dữ liệu

```text
Nhom06_BT03_GenerateData <output.bin> <so-phan-tu> <seed> [min] [max]
```

- `output.bin`: tệp cần tạo.
- `so-phan-tu`: số nguyên không âm; bộ dữ liệu chính nằm trong khoảng 30–50 triệu.
- `seed`: số nguyên dùng để tái lặp.
- `min`, `max`: khoảng sinh tùy chọn; giá trị mặc định sẽ được Thiện ghi rõ trong hướng dẫn.

### Sắp xếp ngoại

```text
Nhom06_BT03_MergeSort <input.bin> <output.bin> <so-phan-tu-moi-khoi>
```

- Không ghi đè `input.bin` trong khi đang xử lý.
- `so-phan-tu-moi-khoi` phải lớn hơn 0 và phù hợp với RAM.
- Tệp đầu ra phải có cùng số phần tử với tệp đầu vào.

### Xác minh kết quả

```text
kiem_tra_sap_xep <output.bin>
```

- Trả thành công khi tệp hợp lệ và có thứ tự không giảm.
- Trả lỗi và báo vị trí sai đầu tiên nếu kết quả không hợp lệ.

## 3. Mã thoát và thông báo

- Mã thoát `0`: thành công.
- Mã thoát khác `0`: tham số sai, lỗi mở tệp, lỗi đọc/ghi hoặc dữ liệu không hợp lệ.
- Thông báo phải nói rõ tệp nào, thao tác nào và nguyên nhân gần nhất có thể.

## 4. Tên file trong quá trình làm việc

| Chức năng       | Nơi phát triển                      | Tên tệp khi bàn giao                         |
| ----------------- | -------------------------------------- | ----------------------------------------------- |
| Sinh dữ liệu    | `Thien/ma_nguon/generate_data.cpp`   | `ma_nguon_chung/Nhom06_BT03_GenerateData.cpp` |
| Merge Sort nội   | `Huy/ma_nguon/merge_sort_noi.cpp`    | Gộp vào file Merge Sort chính                |
| Merge Sort ngoại | `Khoa/ma_nguon/merge_sort_ngoai.cpp` | `ma_nguon_chung/Nhom06_BT03_MergeSort.cpp`    |
| Xác minh         | `Quan/ma_nguon/kiem_tra_sap_xep.cpp` | `kiem_thu/kiem_tra_sap_xep.cpp`               |

## 5. Thứ tự tích hợp

1. Thiện và Khoa xác nhận cùng đọc được một tệp mẫu.
2. Huy bàn giao hàm Merge Sort nội cho Khoa.
3. Khoa tích hợp, chạy test nhỏ và tạo tệp đầu ra.
4. Quân xác minh tệp đầu ra và ghi kết quả.
5. Cả nhóm duyệt hai file trong `ma_nguon_chung/` trước khi đóng gói.
