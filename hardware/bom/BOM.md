# Danh sách linh kiện tham khảo

Trích từ schematic đã lưu khi đóng gói ngày 15/10/2026, gồm **27 designator**. Bảng này phục vụ xem thiết kế, chưa phải BOM mua hàng hoặc BOM lắp ráp đã duyệt.

Giá trị lấy từ Comment; nếu Comment là `=Value1` thì đọc parameter Value1. Các trường chưa khai báo được giữ rõ là chưa có dữ liệu. Không dùng các placeholder `SET_VALUE`/`SET_VOLTAGE` để suy ra thông số linh kiện.

Footprint lấy từ PCB đã lưu. Cột Case là parameter trên schematic, chưa phải xác nhận kích thước thực tế. MPN chỉ lấy từ trường dữ liệu đã khai báo; không tự chọn mã thay thế. Các symbol module/header không mặc định bao gồm module hoặc kit tương ứng trong đơn mua hàng.

| Designator | Giá trị / chức năng | Footprint PCB | Case / Package khai báo | MPN khai báo | Trạng thái |
| --- | --- | --- | --- | --- | --- |
| C1 | 100nF | C0402L | 0402 | Chưa khai báo | Chưa chốt lắp ráp |
| C2 | 100nF | C0402L | 0402 | Chưa khai báo | Chưa chốt lắp ráp |
| C3 | 2.2nF | C0402L | 0402 | Chưa khai báo | Chưa chốt lắp ráp |
| C4 | 100nF | C0402L | 0402 | Chưa khai báo | Chưa chốt lắp ráp |
| C5 | DNP | C0402L | 0402 | Chưa khai báo | DNP |
| H1 | 5xPOGO_PIN | PAD POGOPIN | Chưa khai báo | Chưa khai báo | Chưa chốt lắp ráp |
| Q1 | AO3401A | SOT23-3 | SOT-23 | AO3401A | Chưa chốt lắp ráp |
| R1 | 1M | R0402L1 | 0402 | Chưa khai báo | Chưa chốt lắp ráp |
| R2 | 10k | R0402L1 | 0402 | Chưa khai báo | Chưa chốt lắp ráp |
| R3 | 1.5M | R0402L1 | 0402 | Chưa khai báo | Chưa chốt lắp ráp |
| R4 | 330K | R0402L1 | 0402 | Chưa khai báo | Chưa chốt lắp ráp |
| R5 | 330K | R0402L1 | 0402 | Chưa khai báo | Chưa chốt lắp ráp |
| R6 | 267K | R0402L1 | 0402 | Chưa khai báo | Chưa chốt lắp ráp |
| R7 | 100K | R0402L1 | 0402 | Chưa khai báo | Chưa chốt lắp ráp |
| R8 | 100K | R0402L1 | 0402 | Chưa khai báo | Chưa chốt lắp ráp |
| R9 | 1M | R0402L1 | 0402 | Chưa khai báo | Chưa chốt lắp ráp |
| R10 | 10k | R0402L1 | 0402 | Chưa khai báo | Chưa chốt lắp ráp |
| R11 | 0R | R0402L1 | 0402 | Chưa khai báo | Chưa chốt lắp ráp |
| R12 | 0R | R0402L1 | 0402 | Chưa khai báo | Chưa chốt lắp ráp |
| R13 | 100k | R0402L1 | 0402 | Chưa khai báo | Chưa chốt lắp ráp |
| R14 | DNP | R0402L1 | 0402 | Chưa khai báo | DNP |
| R15 | DNP | R0402L1 | 0402 | Chưa khai báo | DNP |
| TP1 | TP_? | TP_SMD_1P50 | Chưa khai báo | Chưa khai báo | Testpoint; xác nhận có cần linh kiện rời |
| TP2 | TP_? | TP_SMD_1P50 | Chưa khai báo | Chưa khai báo | Testpoint; xác nhận có cần linh kiện rời |
| TP3 | TP_? | TP_SMD_1P50 | Chưa khai báo | Chưa khai báo | Testpoint; xác nhận có cần linh kiện rời |
| U1 | DRV5032FADBZR | DBZ0003A-MFG | Chưa khai báo | DRV5032FADBZR | Chưa chốt lắp ráp |
| U2 | TLV9022DR.A | D0008A-MFG | Chưa khai báo | Chưa khai báo | Chưa chốt lắp ráp |

## Trước khi đặt linh kiện

- Chốt MPN, nhà sản xuất, dung sai, điện áp/công suất và package theo linh kiện thực tế.
- Đối chiếu schematic model với footprint PCB và bản vẽ linh kiện.
- Chốt linh kiện lắp, DNP, module mua riêng và yêu cầu connector.
- DNP đọc được từ schematic: C5, R14, R15.
