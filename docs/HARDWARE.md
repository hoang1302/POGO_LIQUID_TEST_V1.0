# Giao tiếp phần cứng POGO_LIQUID_TEST_V1.0

Tài liệu ghi lại kết nối đã lưu, chưa xác nhận hiệu năng phát hiện nước/chất lỏng. Pinout lấy từ net/pad PCB; chưa thay thế compile/ERC/ECO.

## Các khối chức năng

- H1 là cụm năm pogo pin: hai chân GND, một chân cảm nhận và hai chân net +12.
- U2 TLV9022DR.A có hai kênh comparator, dùng các net tham chiếu VL/VH để so sánh điện áp tại nút cảm nhận.
- R3 = 1,5 MΩ nối chân cảm nhận tới nút có R1 = 1 MΩ, R4 = 330 kΩ và C3 = 2,2 nF.
- U1 DRV5032FADBZR tạo HALL_OUT; HALL_OUT đi qua R10 để điều khiển gate Q1 AO3401A, liên quan tới cấp rail 3V3_TLV.
- OUT1/OUT2 của U2 đi qua R11/R12 = 0 Ω và nối chung thành DRY_OUT. R2 = 10 kΩ kéo lên 3V3_TLV, R13 = 100 kΩ kéo xuống GND.

Các mô tả trên là kết nối, chưa kết luận cực tính logic khô/ướt, trạng thái đóng/ngắt theo nam châm hoặc thời gian phát hiện. Cần xác nhận biến thể Hall sensor và loại ngõ ra comparator trước khi chốt hoạt động.

## Nguồn và connector H1

| Chân | Net trên PCB |
| --- | --- |
| 1 | GND |
| 2 | GND |
| 3 | NetH1_3 |
| 4 | +12 |
| 5 | +12 |

Net +12 và 3V3 là hai rail riêng. Không đưa +12 vào 3V3. Vị trí chân là số chân điện của footprint, chưa thay thế bản vẽ xác định chiều nhìn cụm pogo.

## Testpoint

| Testpoint | Net | Vai trò theo kết nối |
| --- | --- | --- |
| TP1 | HALL_OUT | Quan sát tín hiệu Hall |
| TP2 | DRY_OUT | Quan sát kết quả comparator |
| TP3 | 3V3 | Điểm truy cập rail 3V3 |

Cách đấu nguồn và lấy tín hiệu sang hệ thống ngoài cần được xác nhận theo board thực tế; schematic chưa có connector hệ thống đầy đủ cho mọi tín hiệu.

## Điện áp tham chiếu danh định

Theo các điện trở trong schematic:

```text
VL = 3V3_TLV × 100 kΩ / (330 kΩ + 100 kΩ)
VH = 3V3_TLV × 100 kΩ / (267 kΩ + 100 kΩ)
```

Nếu 3V3_TLV đúng 3,3 V, mô hình lý tưởng cho VL ≈ 0,76744 V và VH ≈ 0,89918 V, khớp ghi chú trên schematic PDF. Đây chưa phải ngưỡng nước đã đo: dung sai, dòng rò, nhiệt độ, rail nguồn và độ dẫn của chất lỏng đều cần kiểm tra.

## Linh kiện tùy chọn

R14, R15 và C5 đang ghi DNP. Giữ nguyên trạng thái này khi thử bản hiện tại; không tự lắp các vị trí DNP nếu chưa có phương án được xác nhận. [BOM tham khảo](../hardware/bom/BOM.md) ghi riêng trạng thái từng linh kiện.

## Các điểm cần hoàn tất

- Đo trạng thái khô/ướt bằng đúng loại chất lỏng, bề mặt và khoảng cách pogo dự kiến.
- Xác nhận cực tính DRY_OUT, ngưỡng chuyển và tỷ lệ báo nhầm.
- Xác nhận khả năng nối chung hai ngõ ra U2 theo đúng biến thể linh kiện.
- Đo HALL_OUT và 3V3_TLV khi thay đổi nam châm, khi reset hoặc mất nguồn.
- Bổ sung sơ đồ đấu nối hệ thống và bản vẽ cơ khí.
- Chốt MPN, điện áp định mức, package và chạy compile/ERC/DRC.
