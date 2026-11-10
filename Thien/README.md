# Workspace của Nguyễn Ngọc Thiện

**MSSV:** 24126216  
**Vai trò:** thiết kế định dạng và viết chương trình sinh dữ liệu nhị phân.

## Bắt đầu theo thứ tự này

1. Đọc [hướng dẫn chung](../HUONG_DAN_BAT_DAU.md) và [quy ước tích hợp](../ma_nguon_chung/QUY_UOC_TICH_HOP.md).
2. Xác nhận định dạng tệp với Khoa, sau đó đọc [`ma_nguon/README.md`](./ma_nguon/README.md) và tạo `ma_nguon/generate_data.cpp`.
3. Viết mô tả định dạng và cách chạy trong [`tai_lieu/`](./tai_lieu/).
4. Tự test theo [`kiem_thu/README.md`](./kiem_thu/README.md), ghi kết quả vào [`ket_qua/`](./ket_qua/).
5. Cập nhật [bảng tiến độ](../TIEN_DO.md), bàn giao tài liệu sang [`../du_lieu/`](../du_lieu/) và code cho Khoa kiểm tra.

## Mục tiêu

Tạo được tệp nhị phân thô gồm các giá trị `long double`, hỗ trợ cả dữ liệu nhỏ để test và dữ liệu 30–50 triệu phần tử cho thực nghiệm.

## Việc cần làm

- [ ] Thống nhất với Khoa định dạng: tệp chứa liên tiếp các giá trị `long double`, không có header.
- [ ] Thống nhất tham số chương trình: tên tệp, số phần tử, seed và khoảng giá trị.
- [ ] Viết `ma_nguon/generate_data.cpp` với kiểm tra tham số và thông báo lỗi rõ ràng.
- [ ] Sinh các giá trị hữu hạn, không sinh `NaN` hoặc vô cùng.
- [ ] Ghi theo khối/buffer để không giữ 30–50 triệu phần tử trong RAM.
- [ ] Hiển thị số phần tử, kích thước tệp dự kiến, seed và thời gian sinh dữ liệu.
- [ ] Kiểm thử tính tái lặp: cùng seed và tham số phải sinh cùng dãy trên cùng môi trường.
- [ ] Viết mô tả định dạng tệp và hướng dẫn chạy cho nhóm.

## Đầu vào cần nhận

- Từ Khoa: cách chương trình sắp xếp nhận đường dẫn và yêu cầu về định dạng tệp.
- Từ Quân: các mốc kích thước dữ liệu cần cho benchmark.

## Đầu ra bàn giao

- Chương trình sinh dữ liệu hoàn chỉnh để tích hợp vào file nộp.
- Tài liệu định dạng tệp và hướng dẫn chạy.
- Các tệp mẫu nhỏ và kết quả kiểm tra kích thước tệp.

## Tiêu chí hoàn thành

- Tệp có kích thước đúng bằng `soPhanTu * sizeof(long double)` trên máy chạy.
- Sinh được 30–50 triệu phần tử mà không nạp toàn bộ dữ liệu vào RAM.
- Khoa và Quân đọc được tệp bằng chương trình của họ.
- Không commit các tệp nhị phân lớn lên Git.

## Cấu trúc workspace

- `ma_nguon/`: chương trình sinh dữ liệu.
- `tai_lieu/`: định dạng tệp và hướng dẫn chạy.
- `kiem_thu/`: ca kiểm thử tham số, kích thước và seed.
- `ket_qua/`: nhật ký sinh dữ liệu và thời gian chạy.

## Người đóng góp

- Nguyễn Ngọc Thiện là người chỉnh sửa chính.
- Phạm Đức Khoa phối hợp chốt định dạng; Nguyễn Hoàng Quân xác nhận các mốc benchmark.

## Đường dẫn phụ thuộc và bàn giao

| Quan hệ | Đường dẫn | Dùng để |
| --- | --- | --- |
| Thiện và Khoa cùng chốt | [`../ma_nguon_chung/QUY_UOC_TICH_HOP.md`](../ma_nguon_chung/QUY_UOC_TICH_HOP.md) | Định dạng tệp và CLI |
| Khoa nhận bàn giao | [`../Khoa/`](../Khoa/) | Kiểm tra đọc tệp và tích hợp |
| Tài liệu chung | [`../du_lieu/`](../du_lieu/) | Hướng dẫn tạo và định dạng dữ liệu |
| Bản cuối | [`../ma_nguon_chung/`](../ma_nguon_chung/) | File sinh dữ liệu đã duyệt |
