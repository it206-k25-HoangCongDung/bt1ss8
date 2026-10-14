# ƯỚC LƯỢNG PRODUCT BACKLOG CHO NỀN TẢNG BÁN HÀNG QUA LIVESTREAM

> 👤 **Học viên:** Hoàng Công Dũng | **Mã SV:** PTIT-HCM-009
> 🏫 **Môn học:** it206-k25-HoangCongDung

---

## Nhiệm vụ 1: Kiểm tra dữ liệu trước khi ước lượng

Sau khi đọc kỹ phần yêu cầu User Story và Acceptance Criteria cho LS01 và LS03 (LS02 là Reference Story được giữ nguyên 3 SP), tôi tiến hành đánh giá độ rõ ràng và xác định các điểm cần làm rõ để phục vụ việc ước lượng chính xác:

- LS01: Đủ rõ - Tiêu đề không để trống và trạng thái hiển thị 'Sắp diễn ra' trước giờ bắt đầu đã được quy định rõ ràng trong tiêu chí chấp nhận.
- LS03: Cần làm rõ - Cần xác định rõ hành vi cụ thể của hệ thống khi có hai khách hàng cùng đặt mua sản phẩm cuối cùng gần như đồng thời để tránh tình trạng bán vượt tồn kho.

| Mã Story | Đủ rõ | Cần làm rõ | Thông tin/câu hỏi còn thiếu |
| --- | --- | --- | --- |
| LS01 | X |  |  |
| LS03 |  | X | Khi hai khách cùng đặt sản phẩm cuối cùng cùng lúc, hệ thống xử lý thế nào để không bị vượt tồn kho? |

## Nhiệm vụ 2: Phân tích Planning Poker và chốt Story Point

Dựa vào kết quả vòng Planning Poker và các ý kiến tranh luận của thành viên trong nhóm, tôi tiến hành phân tích chi tiết cho từng User Story như sau:

Đối với LS01: Đa số các thành viên chọn 3 SP, riêng Dev C chọn 5 SP vì lo ngại logic xử lý thời gian bắt đầu và trạng thái phiên. Tuy nhiên, phạm vi của LS01 khá cô lập, chỉ cần hiển thị trạng thái tĩnh 'Sắp diễn ra' trước giờ bắt đầu, không cần tự động chuyển trạng thái phức tạp. Do đó, Story Point cuối cùng được chốt là 3 SP, tương đương với Reference Story LS02.

Đối với LS03: Các phiếu dao động giữa 5 SP và 8 SP. Lý do phiếu 5 SP cho rằng luồng tạo đơn và kiểm tra tồn kho quen thuộc, phạm vi kiểm soát tốt. Lý do phiếu 8 SP nhìn thấy rủi ro đồng thời (concurrency) khi nhiều khách đặt sản phẩm cuối cùng cùng lúc và các quy tắc giảm/hoàn tồn kho cần làm rõ. Sau khi PO làm rõ dữ liệu (đơn giữ số lượng mới thành công, đơn còn lại nhận thông báo hết hàng), độ phức tạp kỹ thuật đã giảm bớt rủi ro mơ hồ. Nhóm thống nhất chốt 5 SP, lớn hơn LS02 (3 SP) do logic nghiệp vụ kho và tạo đơn phức tạp hơn.

| Mã Story | Mức ưu tiên | Kết quả phiếu | SP cuối cùng | Lý do ngắn |
| --- | --- | --- | --- | --- |
| LS01 | 1 | 3 - 3 - 5 - 3 | 3 | Phạm vi tương đương LS02; logic xử lý trạng thái 'Sắp diễn ra' đơn giản, phiếu 5 SP đánh giá quá cao phần thời gian. |
| LS02 | 2 | 3 - 3 - 3 - 3 | 3 | Reference Story; các phiếu đã trùng nhau. |
| LS03 | 3 | 5 - 8 - 8 - 5 | 5 | Phức tạp hơn LS02 do có logic kiểm tra tồn kho và xử lý đơn hàng đồng thời; các phiếu cao đã phản ánh rủi ro kỹ thuật. |

## Nhiệm vụ 3: Phát hiện cách hiểu sai về Story Point

Đề xuất cố định '1 Story Point = 4 giờ' cho mọi User Story là hoàn toàn sai bản chất của phương pháp ước lượng Agile.

Story Point là đơn vị đo lường tương đối phản ánh tổng hợp độ phức tạp, khối lượng công việc và rủi ro của một User Story, chứ không phải là thước đo thời gian tuyệt đối. Việc quy đổi cứng nhắc sang giờ làm việc sẽ làm mất đi ý nghĩa của ước lượng tương đối khi độ khó thực tế của các tính năng là khác nhau.

Thay vì đổi SP sang giờ, nhóm Scrum sẽ sử dụng Velocity (tốc độ hoàn thành tổng số Story Point trong một Sprint trước đó) kết hợp với năng lực thực tế của đội ngũ để dự báo chính xác khối lượng công việc có thể cam kết cho Sprint tiếp theo.

---

## 📁 Danh sách tệp tin nộp bài trong Repository
- 📝 `bt1.docx`: Báo cáo tài liệu phân tích nghiệp vụ hoàn chỉnh.
