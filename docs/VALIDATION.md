# Kế hoạch kiểm tra

Tài liệu này là danh sách việc cần thực hiện, **không phải báo cáo đã đạt**. Gói chưa có dữ liệu đo hoặc xác nhận hoạt động phần cứng từ người thiết kế.

## Kiểm tra thiết kế

- Compile schematic và xác nhận kết nối schematic–PCB.
- Chạy ERC/DRC trên đúng bản lưu; giữ báo cáo, thời điểm chạy và revision.
- Đối chiếu footprint, cực tính, điện áp/công suất định mức và bản vẽ cơ khí.
- Chốt BOM, DNP và linh kiện/module mua riêng.

## Kiểm tra phần cứng

| Phép kiểm tra | Bằng chứng cần lưu |
| --- | --- |
| Kiểm tra nguồn và Hall | Đo 3V3, HALL_OUT, 3V3_TLV với các trạng thái nam châm và khi mất/cấp lại nguồn. |
| Kiểm tra khô/ướt | Thử đúng loại chất lỏng và bề mặt, thay đổi lượng chất lỏng/khoảng cách, ghi DRY_OUT và điện áp nút cảm nhận. |
| Kiểm tra ngưỡng | Đo VL/VH, thử tín hiệu quanh điểm chuyển và xác nhận trạng thái khi hai ngõ comparator nối chung. |
| Kiểm tra báo nhầm | Thử tiếp xúc, rung, bẩn, độ ẩm và biến động nguồn trong điều kiện sử dụng dự kiến. |

## Nội dung báo cáo kết quả

Ghi hardware revision, ngày đo, sơ đồ đấu nối, thiết bị đo, cấu hình nguồn/tải, mẫu thử, số lần lặp, kết quả, lỗi còn mở và ảnh board thực tế. Chỉ điền kết quả sau khi đã thực hiện; không suy ra PASS chỉ từ schematic hoặc báo cáo cũ.
