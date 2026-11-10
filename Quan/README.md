# Workspace của Nguyễn Hoàng Quân

**MSSV:** 25133057  
**Vai trò:** lý thuyết, kiểm tra độc lập, benchmark, báo cáo và kiểm tra gói nộp.

## Bắt đầu theo thứ tự này

1. Đọc [hướng dẫn chung](../HUONG_DAN_BAT_DAU.md) và [quy ước tích hợp](../ma_nguon_chung/QUY_UOC_TICH_HOP.md).
2. Đọc yêu cầu code trong [`ma_nguon/README.md`](./ma_nguon/README.md), sau đó tạo `ma_nguon/kiem_tra_sap_xep.cpp`.
3. Viết phần lý thuyết theo [`tai_lieu/README.md`](./tai_lieu/README.md) song song với code.
4. Tự test theo [`kiem_thu/README.md`](./kiem_thu/README.md) và ghi số liệu theo [`ket_qua/README.md`](./ket_qua/README.md).
5. Cập nhật dòng của Quân trong [bảng tiến độ](../TIEN_DO.md), sau đó bàn giao verifier sang [`../kiem_thu/`](../kiem_thu/).

## Mục tiêu

Quân không chỉ tổng hợp báo cáo mà còn phụ trách một công cụ kỹ thuật độc lập để xác minh tính đúng đắn của kết quả sắp xếp.

## Việc cần làm

- [ ] Viết phần lý thuyết về bài toán sắp xếp ngoại, lý do phải dùng bộ nhớ ngoài và quy trình tạo/trộn run.
- [ ] Viết `ma_nguon/kiem_tra_sap_xep.cpp` để đọc tuần tự tệp `long double` và kiểm tra thứ tự không giảm.
- [ ] Công cụ kiểm tra phải báo tổng số phần tử, giá trị nhỏ nhất/lớn nhất và vị trí sai đầu tiên nếu dữ liệu chưa được sắp xếp.
- [ ] Thiết kế kiểm thử tích hợp cho dữ liệu rỗng, 1 phần tử, trùng lặp, đã tăng, giảm dần, số lượng lẻ và dữ liệu ngẫu nhiên.
- [ ] Tổ chức benchmark và ghi thời gian sinh dữ liệu, sắp xếp, xác minh; kích thước tệp; cấu hình máy.
- [ ] Tổng hợp nội dung Word, đối chiếu mã nguồn và kiểm tra đủ 3 tệp trước khi nén.

## Đầu vào cần nhận

- Từ Thiện: định dạng tệp và các tệp dữ liệu mẫu.
- Từ Huy: mã giả, phân tích và kết quả kiểm thử Merge Sort nội.
- Từ Khoa: tệp đã sắp xếp, thời gian chạy và mô tả Merge Sort ngoại.

## Đầu ra bàn giao

- Công cụ `kiem_tra_sap_xep.cpp` được chuyển sang `kiem_thu/` dùng chung.
- Phần lý thuyết và file Word hoàn chỉnh trong `bao_cao/`.
- Bảng benchmark và biên bản xác minh trong `ket_qua_chung/`.

## Tiêu chí hoàn thành

- Công cụ xác minh đọc tệp theo luồng, không nạp toàn bộ dữ liệu vào RAM.
- Phát hiện đúng tệp hợp lệ, tệp sai thứ tự và tệp có kích thước không hợp lệ.
- Mỗi số liệu trong báo cáo truy vết được về một lần chạy trong `ket_qua_chung/`.

## Cấu trúc workspace

- `ma_nguon/`: công cụ xác minh.
- `tai_lieu/`: lý thuyết và bản nháp báo cáo.
- `kiem_thu/`: kịch bản kiểm thử tích hợp.
- `ket_qua/`: benchmark và biên bản kiểm tra.

## Người đóng góp

- Nguyễn Hoàng Quân là người chỉnh sửa chính.
- Huy, Thiện và Khoa cung cấp đầu vào, xác nhận nội dung liên quan đến phần việc của mình.

## Đường dẫn phụ thuộc và bàn giao

| Cần lấy từ | Đường dẫn | Dùng để |
| --- | --- | --- |
| Thiện | [`../Thien/tai_lieu/`](../Thien/tai_lieu/) | Hiểu định dạng tệp |
| Huy | [`../Huy/tai_lieu/`](../Huy/tai_lieu/) | Lấy mã giả và phân tích thuật toán |
| Khoa | [`../Khoa/ket_qua/`](../Khoa/ket_qua/) | Lấy tệp kết quả và log sắp xếp |
| Quân bàn giao | [`../kiem_thu/`](../kiem_thu/) | Verifier và kịch bản tích hợp |
| Quân bàn giao | [`../ket_qua_chung/`](../ket_qua_chung/) | Benchmark đã xác minh |
| Quân bàn giao | [`../bao_cao/`](../bao_cao/) | File Word hoàn chỉnh |
