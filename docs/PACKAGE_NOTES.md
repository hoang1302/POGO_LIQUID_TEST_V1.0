# Ghi chú đóng gói

Ngày đóng gói: 15/10/2026. Nguồn là các file đã lưu của project POGO_LIQUID_TEST_V1.0. Không thay đổi thiết kế điện, vị trí linh kiện, route hoặc nội dung thư viện.

## Nội dung đã kiểm tra

- Tính toàn vẹn file nguồn và bản sao bằng SHA-256.
- 27 linh kiện schematic và 27 linh kiện trên PCB chính.
- Tham chiếu tài liệu trong bản sao project đều trỏ tới file đi kèm.
- Tên footprint được schematic/PCB sử dụng so với các mục trong PcbLib đi kèm. Đây là kiểm tra tên, chưa xác nhận hình học footprint.
- PDF nguồn có 1 trang, thời điểm tạo theo metadata: 2026-10-15 15:05:58+07:00.

## Thư viện và phần còn mở

- Không thiếu tên footprint đang dùng trong PcbLib đi kèm.
- SourceLibraryName lịch sử là Schlib1.SchLib, trong khi thư viện project hiện tên POGO_LIQUID_TEST_V1.0.SchLib. Khi dùng Update From Libraries, kiểm tra và ánh xạ lại tham chiếu nếu Altium yêu cầu. Không sửa dữ liệu nhúng trong schematic khi đóng gói.
- R14, R15 và C5 là DNP theo giá trị schematic.
- PDF có thời điểm tạo sau schematic trong cùng ngày, nhưng chưa đối chiếu đầy đủ nội dung. Title/Revision/Drawn By chưa điền đầy đủ.

## Phạm vi kiểm tra

Chưa mở/compile bản đóng gói trong Altium, chưa chạy lại ERC/DRC và chưa thử phần cứng. Các báo cáo cũ trong thư mục output không dùng làm bằng chứng bản hiện tại đã đạt. Danh sách linh kiện được tạo để tham khảo; nhiều thông số mua hàng còn thiếu.

Gói không kèm cache, History, log, báo cáo output cũ, Gerber/CPL chưa xác nhận hoặc firmware chưa có. Metadata nguồn thư viện được giữ nguyên; các ghi chú bản quyền của linh kiện/thư viện ngoài không được thay đổi. Chưa gán giấy phép sử dụng mới cho toàn bộ thiết kế.
