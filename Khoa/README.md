# Workspace của Phạm Đức Khoa

**MSSV:** 24149170  
**Vai trò:** thiết kế, cài đặt và tích hợp Merge Sort ngoại.

## Bắt đầu theo thứ tự này

1. Đọc [hướng dẫn chung](../HUONG_DAN_BAT_DAU.md) và cùng Thiện chốt [quy ước tích hợp](../ma_nguon_chung/QUY_UOC_TICH_HOP.md).
2. Đọc [`ma_nguon/README.md`](./ma_nguon/README.md), sau đó tạo `ma_nguon/merge_sort_ngoai.cpp` với khung I/O và quản lý run.
3. Chốt giao diện hàm với Huy và tích hợp `Huy/ma_nguon/merge_sort_noi.cpp` sau khi được bàn giao.
4. Viết tài liệu trong [`tai_lieu/`](./tai_lieu/), test theo [`kiem_thu/`](./kiem_thu/) và ghi log vào [`ket_qua/`](./ket_qua/).
5. Cập nhật [bảng tiến độ](../TIEN_DO.md), bàn giao tệp đầu ra cho Quân xác minh rồi mới tích hợp vào [`../ma_nguon_chung/`](../ma_nguon_chung/).

## Mục tiêu

Sắp xếp tệp nhị phân 30–50 triệu giá trị `long double` mà không nạp toàn bộ tệp vào RAM, dùng các run và các lượt trộn không đệ quy.

## Việc cần làm

- [ ] Thống nhất với Thiện định dạng tệp nhị phân và quy tắc đặt tên tệp đầu vào/đầu ra.
- [ ] Thống nhất với Huy giao diện hàm Merge Sort nội dùng để tạo run ban đầu.
- [ ] Thiết kế luồng xử lý: đọc khối vừa RAM, sắp xếp khối, ghi run, sau đó trộn các run cho đến khi còn một run.
- [ ] Viết `ma_nguon/merge_sort_ngoai.cpp`, không nạp toàn bộ tệp vào bộ nhớ.
- [ ] Cho phép cấu hình kích thước khối/run để thử nghiệm với các giới hạn RAM khác nhau.
- [ ] Xử lý run cuối ngắn hơn, số run lẻ, tệp rỗng, tệp một phần tử và lỗi đọc/ghi.
- [ ] Không ghi đè tệp gốc cho đến khi quá trình sắp xếp thành công; dọn tệp tạm sau khi kết thúc.
- [ ] Ghi lại số phần tử, kích thước run, số lượt trộn, thời gian và đường dẫn tệp kết quả.
- [ ] Bàn giao tệp đã sắp xếp cho Quân xác minh độc lập.

## Đầu vào cần nhận

- Từ Thiện: tệp dữ liệu nhị phân và mô tả định dạng.
- Từ Huy: hàm Merge Sort nội đã qua kiểm thử.
- Từ Quân: kịch bản kiểm thử tích hợp và các mốc benchmark.

## Đầu ra bàn giao

- Chương trình Merge Sort ngoại đã tích hợp phần sắp xếp nội.
- Tài liệu luồng thuật toán, quy tắc quản lý run và hướng dẫn chạy.
- Nhật ký kiểm thử, tệp kết quả và số liệu thời gian cho Quân.

## Tiêu chí hoàn thành

- Quân xác minh tệp đầu ra có đủ số phần tử và không giảm.
- Chương trình xử lý được dữ liệu lớn hơn giới hạn RAM đã cấu hình.
- Không còn tệp tạm sau khi chạy thành công; khi lỗi có thông báo rõ ràng.
- Mã nguồn biên dịch và chạy được theo hướng dẫn bàn giao.

## Cấu trúc workspace

- `ma_nguon/`: chương trình Merge Sort ngoại và mã tích hợp.
- `tai_lieu/`: thiết kế luồng xử lý và hướng dẫn chạy.
- `kiem_thu/`: ca kiểm thử đọc/ghi, run và tích hợp.
- `ket_qua/`: nhật ký chạy và thời gian thực thi.

## Người đóng góp

- Phạm Đức Khoa là người chỉnh sửa chính.
- Châu Kim Huy đóng góp thuật toán sắp xếp nội; Nguyễn Ngọc Thiện đóng góp định dạng và dữ liệu; Nguyễn Hoàng Quân kiểm thử chéo.

## Đường dẫn phụ thuộc và bàn giao

| Cần lấy từ | Đường dẫn | Dùng để |
| --- | --- | --- |
| Thiện | [`../Thien/ma_nguon/`](../Thien/ma_nguon/) và [`../du_lieu/`](../du_lieu/) | Bộ sinh và định dạng dữ liệu |
| Huy | [`../Huy/ma_nguon/`](../Huy/ma_nguon/) | Hàm Merge Sort nội để tạo run |
| Quân | [`../Quan/kiem_thu/`](../Quan/kiem_thu/) | Kịch bản tích hợp và tiêu chí xác minh |
| Khoa bàn giao | [`ket_qua/`](./ket_qua/) | Tệp kết quả và log để Quân xác minh |
| Bản cuối | [`../ma_nguon_chung/`](../ma_nguon_chung/) | File Merge Sort đã tích hợp và duyệt |
