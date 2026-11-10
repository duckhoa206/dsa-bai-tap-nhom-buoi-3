# Bài tập nhóm buổi 3 – Merge Sort

> **Vừa pull repo về và chưa biết bắt đầu từ đâu?** Mở [Hướng dẫn bắt đầu](./HUONG_DAN_BAT_DAU.md), chọn đúng tên của mình và làm theo từng bước. Theo dõi tình trạng bàn giao tại [Bảng tiến độ](./TIEN_DO.md).

## Điều hướng nhanh

| Tôi là | Bắt đầu tại                           | Sản phẩm chính                           |
| -------- | ----------------------------------------- | ------------------------------------------- |
| Quân    | [Workspace của Quân](./Quan/README.md)   | Lý thuyết, verifier, benchmark, báo cáo |
| Huy      | [Workspace của Huy](./Huy/README.md)      | Merge Sort nội không đệ quy             |
| Thiện   | [Workspace của Thiện](./Thien/README.md) | Chương trình sinh dữ liệu nhị phân   |
| Khoa     | [Workspace của Khoa](./Khoa/README.md)    | Merge Sort ngoại và tích hợp            |

Trước khi viết phần giao tiếp giữa các chương trình, đọc [Quy ước tích hợp](./ma_nguon_chung/QUY_UOC_TICH_HOP.md).

## Thông tin chung

- **Môn học:** Cấu trúc dữ liệu và Giải thuật (DSA)
- **Bài tập:** Bài tập nhóm buổi 3
- **Chủ đề:** Sắp xếp ngoại bằng Merge Sort theo `run-length`
- **Nhóm thực hiện:** Nhóm 6

## Yêu cầu bài tập

1. Trình bày về bài toán sắp xếp ngoại.
2. Trình bày ý tưởng, mã giả và cài đặt phương pháp sắp xếp trộn theo `run-length`.
3. Cài đặt Merge Sort theo `run-length` không đệ quy, sắp xếp nội.
4. Viết chương trình tạo một tập tin dữ liệu nhị phân chứa các giá trị `long double`, với khoảng 30–50 triệu phần tử.
5. Viết chương trình cài đặt Merge Sort để thực hiện sắp xếp ngoại cho tập tin trên.

## Yêu cầu nộp bài

Nộp 3 tệp:

1. Hai tệp mã nguồn.
2. Một tệp Word trình bày bài làm.

Quy cách đặt tên tệp nén của nhóm: `Nhom06_BT03_MergeSort.RAR` hoặc `Nhom06_BT03_MergeSort.ZIP`. Bên trong tệp nén chứa hai tệp cùng tên theo yêu cầu.

## Thành viên nhóm 6

| STT | Mã số sinh viên | Họ và tên         |
| --: | :----------------: | -------------------- |
|   1 |      25133057      | Nguyễn Hoàng Quân |
|   2 |      24162040      | Châu Kim Huy        |
|   3 |      24126216      | Nguyễn Ngọc Thiện |
|   4 |      24149170      | Phạm Đức Khoa     |

## Bảng phân công

| STT | Mã số sinh viên | Họ và tên         | Nội dung phụ trách                                                                                                                              | Trạng thái     |
| --: | :----------------: | -------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------- |
|   1 |      25133057      | Nguyễn Hoàng Quân | Trình bày sắp xếp ngoại; viết công cụ kiểm tra tệp đã sắp xếp; phụ trách kiểm thử tích hợp, benchmark, báo cáo và gói nộp | Chưa bắt đầu |
|   2 |      24162040      | Châu Kim Huy        | Xây dựng ý tưởng, mã giả và cài đặt Merge Sort nội không đệ quy theo `run-length`                                                 | Chưa bắt đầu |
|   3 |      24126216      | Nguyễn Ngọc Thiện | Viết chương trình sinh tệp nhị phân gồm 30–50 triệu giá trị `long double`                                                            | Chưa bắt đầu |
|   4 |      24149170      | Phạm Đức Khoa     | Cài đặt Merge Sort ngoại, quản lý các run, tệp tạm và đo thời gian thực thi                                                           | Chưa bắt đầu |

### Phối hợp và kiểm thử chéo

1. Nguyễn Ngọc Thiện thống nhất định dạng tệp nhị phân với Phạm Đức Khoa, sau đó bàn giao chương trình sinh dữ liệu và các bộ dữ liệu mẫu.
2. Châu Kim Huy bàn giao hàm Merge Sort nội cùng giao diện đã thống nhất để Phạm Đức Khoa tích hợp khi tạo các run ban đầu.
3. Phạm Đức Khoa bàn giao chương trình Merge Sort ngoại và nhật ký chạy cho Nguyễn Hoàng Quân.
4. Nguyễn Hoàng Quân dùng công cụ kiểm tra độc lập để xác minh tệp kết quả, tổ chức benchmark và ghi nhận lỗi tích hợp.
5. Chính tác giả sửa lỗi trong workspace cá nhân; người kiểm thử chéo xác nhận lại trước khi chuyển sản phẩm vào thư mục dùng chung.

## Cấu trúc thư mục

```text
.
├── README.md              # Yêu cầu, phân công và quy tắc chung
├── HUONG_DAN_BAT_DAU.md  # Điểm bắt đầu sau khi pull repo
├── TIEN_DO.md             # Trạng thái công việc và bàn giao
├── Quan/                 # Lý thuyết, verifier, benchmark và báo cáo
│   ├── ma_nguon/
│   ├── tai_lieu/
│   ├── kiem_thu/
│   └── ket_qua/
├── Huy/                  # Merge Sort nội không đệ quy
│   ├── ma_nguon/
│   ├── tai_lieu/
│   ├── kiem_thu/
│   └── ket_qua/
├── Thien/                # Sinh và kiểm tra dữ liệu nhị phân
│   ├── ma_nguon/
│   ├── tai_lieu/
│   ├── kiem_thu/
│   └── ket_qua/
├── Khoa/                 # Merge Sort ngoại và tích hợp
│   ├── ma_nguon/
│   ├── tai_lieu/
│   ├── kiem_thu/
│   └── ket_qua/
├── ma_nguon_chung/       # Mã nguồn đã tích hợp và kiểm thử
├── bao_cao/              # Báo cáo Word và tài liệu chung
├── kiem_thu/             # Kịch bản và công cụ kiểm thử
├── du_lieu/              # Hướng dẫn và dữ liệu dùng chung
└── ket_qua_chung/        # Kết quả chạy và sản phẩm đã chốt
```

## Quy tắc làm việc

1. Mỗi thành viên chỉ phát triển bản nháp trong workspace mang tên mình.
2. Không tự ý sửa hoặc xóa tệp trong workspace của thành viên khác.
3. Mã nguồn chỉ được chuyển vào `ma_nguon_chung/` sau khi đã kiểm thử và được thành viên liên quan thống nhất.
4. Tài liệu, mã nguồn và kết quả trong thư mục dùng chung phải ghi rõ người phụ trách và người đóng góp trong README của thư mục.
5. Không commit tệp nhị phân dung lượng lớn, tệp biên dịch hoặc các run tạm lên Git.
6. Không dùng `git add -f` để bỏ qua `.gitignore` nếu chưa trao đổi với nhóm.
7. Gói `.zip`/`.rar` cuối cùng được tạo cục bộ để nộp, không lưu trùng trong Git.

### Quy tắc commit tệp

| Nên commit                                                            | Không commit                                                     |
| ---------------------------------------------------------------------- | ----------------------------------------------------------------- |
| Mã nguồn `.cpp`, `.h`, `.hpp`                                  | Tệp biên dịch `.o`, `.obj`, `.exe`, `.out`             |
| `Makefile`, `CMakeLists.txt` và cấu hình build dùng chung      | Thư mục `build/`, cache CMake và thư viện đã biên dịch |
| README, tài liệu, file Word chính thức                             | Thiết lập IDE cá nhân, file tạm của Word/hệ điều hành   |
| Kết quả nhỏ dạng `.md`, `.txt`, `.csv` dùng trong báo cáo | Dữ liệu `.bin`, `.dat`, run tạm và core dump              |
| Cấu hình IDE thực sự dùng chung như VS Code `tasks.json`       | Gói nén `.zip`, `.rar` được tạo lại từ nội dung repo |

## Kế hoạch thực hiện

1. **Thống nhất giao diện:** chốt định dạng tệp nhị phân, tham số dòng lệnh, tên tệp và cách ghi nhật ký.
2. **Phát triển độc lập:** mỗi thành viên hoàn thành mã nguồn, tài liệu và kiểm thử trong workspace của mình.
3. **Tích hợp:** ghép bộ sinh dữ liệu, Merge Sort nội và Merge Sort ngoại; kiểm thử bằng dữ liệu nhỏ.
4. **Kiểm thử quy mô lớn:** chạy lần lượt với 1 triệu, 10 triệu và 30–50 triệu phần tử; xác minh tệp đầu ra bằng công cụ độc lập.
5. **Chốt sản phẩm:** đưa mã đã duyệt vào `ma_nguon_chung/`, kết quả vào `ket_qua_chung/`, hoàn thiện file Word và kiểm tra gói nộp.
