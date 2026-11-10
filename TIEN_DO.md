# Bảng tiến độ và bàn giao

Mỗi thành viên tự cập nhật dòng do mình phụ trách. Trạng thái dùng thống nhất: **Chưa bắt đầu**, **Đang làm**, **Chờ duyệt**, **Cần sửa**, **Hoàn thành**.

## Giải thích trạng thái

| Trạng thái | Ý nghĩa | Ai cập nhật? |
| --- | --- | --- |
| **Chưa bắt đầu** | Hạng mục chưa được thực hiện. | Người phụ trách hạng mục |
| **Đang làm** | Đã bắt đầu viết code, tài liệu hoặc kiểm thử nhưng chưa sẵn sàng bàn giao. | Người phụ trách hạng mục |
| **Chờ duyệt** | Người phụ trách đã hoàn thành và tự kiểm thử; sản phẩm đang chờ người ở cột **Người duyệt/nhận** kiểm tra. | Người phụ trách sau khi bàn giao |
| **Cần sửa** | Người duyệt đã phát hiện lỗi hoặc nội dung chưa đạt; sản phẩm phải được sửa trong workspace cá nhân. | Người duyệt, kèm mô tả nội dung cần sửa |
| **Hoàn thành** | Sản phẩm đã đạt yêu cầu, được duyệt và chuyển đến đúng thư mục chung ghi trong cột **Đích đến**. | Người duyệt sau khi kiểm tra lần cuối |

## Luồng chuyển trạng thái

```text
Chưa bắt đầu → Đang làm → Chờ duyệt → Hoàn thành
                              ↓
                           Cần sửa
                              ↓
                           Đang làm → Chờ duyệt
```

Chỉ đánh dấu **Hoàn thành** khi sản phẩm đã được kiểm tra chéo và xuất hiện ở đúng đường dẫn trong cột **Đích đến**.

| Hạng mục | Phụ trách | Đường dẫn đang làm | Người duyệt/nhận | Đích đến | Trạng thái |
| --- | --- | --- | --- | --- | --- |
| Quy ước dữ liệu và CLI | Thiện + Khoa | [`ma_nguon_chung/QUY_UOC_TICH_HOP.md`](./ma_nguon_chung/QUY_UOC_TICH_HOP.md) | Huy + Quân | Chính tệp này | Chờ duyệt |
| Bộ sinh dữ liệu | Thiện | [`Thien/ma_nguon/`](./Thien/ma_nguon/) | Khoa | `ma_nguon_chung/Nhom06_BT03_GenerateData.cpp` | Chưa bắt đầu |
| Merge Sort nội | Huy | [`Huy/ma_nguon/`](./Huy/ma_nguon/) | Khoa | Gộp vào `ma_nguon_chung/Nhom06_BT03_MergeSort.cpp` | Chưa bắt đầu |
| Merge Sort ngoại | Khoa | [`Khoa/ma_nguon/`](./Khoa/ma_nguon/) | Huy + Quân | `ma_nguon_chung/Nhom06_BT03_MergeSort.cpp` | Chưa bắt đầu |
| Công cụ xác minh | Quân | [`Quan/ma_nguon/`](./Quan/ma_nguon/) | Khoa | `kiem_thu/kiem_tra_sap_xep.cpp` | Chưa bắt đầu |
| Test tích hợp | Quân | [`Quan/kiem_thu/`](./Quan/kiem_thu/) | Cả nhóm | [`kiem_thu/`](./kiem_thu/) | Chưa bắt đầu |
| Benchmark | Quân + Khoa | [`Quan/ket_qua/`](./Quan/ket_qua/), [`Khoa/ket_qua/`](./Khoa/ket_qua/) | Huy + Thiện | [`ket_qua_chung/`](./ket_qua_chung/) | Chưa bắt đầu |
| Phần lý thuyết chung | Quân | [`Quan/tai_lieu/`](./Quan/tai_lieu/) | Cả nhóm | [`bao_cao/`](./bao_cao/) | Chưa bắt đầu |
| Phần thuật toán nội | Huy | [`Huy/tai_lieu/`](./Huy/tai_lieu/) | Quân | [`bao_cao/`](./bao_cao/) | Chưa bắt đầu |
| Phần sinh dữ liệu | Thiện | [`Thien/tai_lieu/`](./Thien/tai_lieu/) | Quân | [`bao_cao/`](./bao_cao/) | Chưa bắt đầu |
| Phần sắp xếp ngoại | Khoa | [`Khoa/tai_lieu/`](./Khoa/tai_lieu/) | Quân | [`bao_cao/`](./bao_cao/) | Chưa bắt đầu |
| File Word và gói nộp | Quân | [`bao_cao/`](./bao_cao/) | Cả nhóm | `Nhom06_BT03_MergeSort.zip` | Chưa bắt đầu |
