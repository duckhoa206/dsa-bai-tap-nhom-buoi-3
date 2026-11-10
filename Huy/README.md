# Workspace của Châu Kim Huy

**MSSV:** 24162040  
**Vai trò:** thiết kế, cài đặt và kiểm thử Merge Sort nội không đệ quy theo `run-length`.

## Bắt đầu theo thứ tự này

1. Đọc [hướng dẫn chung](../HUONG_DAN_BAT_DAU.md) và [quy ước tích hợp](../ma_nguon_chung/QUY_UOC_TICH_HOP.md).
2. Trao đổi với Khoa để chốt giao diện hàm, sau đó đọc [`ma_nguon/README.md`](./ma_nguon/README.md) và tạo `ma_nguon/merge_sort_noi.cpp`.
3. Viết mã giả và phân tích trong [`tai_lieu/`](./tai_lieu/).
4. Tự test theo [`kiem_thu/README.md`](./kiem_thu/README.md), ghi kết quả vào [`ket_qua/`](./ket_qua/).
5. Cập nhật [bảng tiến độ](../TIEN_DO.md) và bàn giao hàm cho Khoa tại [`../Khoa/`](../Khoa/).

## Mục tiêu

Xây dựng phần sắp xếp trong RAM dùng cách trộn bottom-up, có thể tích hợp để sắp xếp các khối dữ liệu ban đầu của Merge Sort ngoại.

## Việc cần làm

- [ ] Viết ý tưởng và mã giả cho hàm trộn hai run liền kề.
- [ ] Viết mã giả Merge Sort bottom-up với `runLength` lần lượt là 1, 2, 4, 8, ...
- [ ] Thống nhất với Khoa giao diện hàm, kiểu dữ liệu và cách truyền kích thước mảng.
- [ ] Viết `ma_nguon/merge_sort_noi.cpp`, không sử dụng đệ quy và không dùng hàm sắp xếp có sẵn trong phần cài đặt chính.
- [ ] Xử lý đúng run cuối ngắn hơn `runLength`, số phần tử lẻ, giá trị trùng và số âm.
- [ ] Viết kiểm thử và so sánh kết quả với `std::sort` chỉ trong mã kiểm thử.
- [ ] Ghi phân tích độ phức tạp thời gian, bộ nhớ phụ và nội dung bàn giao cho báo cáo.

## Đầu vào cần nhận

- Từ Thiện: thống nhất kiểu phần tử là `long double`.
- Từ Khoa: giới hạn kích thước khối và giao diện cần dùng khi tích hợp.

## Đầu ra bàn giao

- Hàm Merge Sort nội và hàm trộn đã kiểm thử.
- Mã giả, giải thích thuật toán và phân tích độ phức tạp cho Quân.
- Biên bản kiểm thử và các ca biên.

## Tiêu chí hoàn thành

- Không có lời gọi đệ quy.
- Kết quả trùng với `std::sort` trên toàn bộ ca kiểm thử.
- Không truy cập vượt biên khi kích thước không phải lũy thừa của 2.
- Khoa có thể tích hợp hàm mà không phải viết lại thuật toán.

## Cấu trúc workspace

- `ma_nguon/`: cài đặt Merge Sort nội.
- `tai_lieu/`: ý tưởng, mã giả và phân tích.
- `kiem_thu/`: ca kiểm thử và mã test.
- `ket_qua/`: kết quả test và ghi chú hiệu năng.

## Người đóng góp

- Châu Kim Huy là người chỉnh sửa chính.
- Phạm Đức Khoa phối hợp chốt giao diện và kiểm tra khả năng tích hợp.

## Đường dẫn phụ thuộc và bàn giao

| Quan hệ | Đường dẫn | Dùng để |
| --- | --- | --- |
| Huy tham khảo | [`../ma_nguon_chung/QUY_UOC_TICH_HOP.md`](../ma_nguon_chung/QUY_UOC_TICH_HOP.md) | Dùng đúng kiểu dữ liệu và quy ước chung |
| Khoa nhận bàn giao | [`../Khoa/ma_nguon/`](../Khoa/ma_nguon/) | Tích hợp hàm sắp xếp nội |
| Quân nhận tài liệu | [`../bao_cao/`](../bao_cao/) | Tổng hợp mã giả và phân tích |
| Bản cuối | [`../ma_nguon_chung/`](../ma_nguon_chung/) | Hàm của Huy được gộp vào file Merge Sort chính |
