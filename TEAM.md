# Team

> Điền file này trên repo chung do nhóm trưởng fork. Nhóm điền phần **Thông tin nhóm** và **Thành viên**. Mỗi người tự điền phần của mình trong **Cá nhân**. Không copy file này sang repo khác.

## Thông tin nhóm

- Tên nhóm: ABCD
- Candidate problem nhóm chọn (1 câu): Khi xong eval hằng tuần, Junior AI Engineer phụ trách đánh giá RAG muốn biết các câu sai hỏng vì nguyên nhân gì để báo cáo và chọn việc sửa trước planning, nhưng mất khoảng 60/130 phút chỉ để đọc và gán nhãn khoảng 60 câu sai.
- Quyết định cuối (Go / Not Yet / No-Go): Go (phạm vi nhỏ)

## Thành viên

| STT | Họ và tên | MSSV | Vai trò trong nhóm | Tài khoản GitHub |
|---:|---|---|---|---|
| 1 | Đoàn Sỹ Hưng | 2A202603990 | Trưởng nhóm | https://github.com/hgmdz1210 |
| 2 | Trần Việt Anh | 2A202604029 | Phụ trách kiểm chứng | https://github.com/Vietzanh |
| 3 | Từ Huy Bảo| 2A202604021 | Thành viên | [thbao4545](https://github.com/thbao4545) |
| 4 | | | | |

Không ghi email hay số điện thoại vào bảng này, vì repo có thể để public.

Gợi ý vai trò (một người có thể giữ nhiều vai): điều phối thời gian, ghi chép, người phản biện chính, phụ trách kiểm chứng (phỏng vấn/survey), phụ trách research, vẽ quy trình, viết Problem Statement.

## Phân công theo checkpoint

| Checkpoint | Người chính | Người hỗ trợ | Sản phẩm |
|---|---|---|---|
| CP3 — Hội tụ nhóm | Việt Anh | Hưng | Cluster, cây OST, bảng chấm điểm |
| CP4 — Kiểm chứng | | Hưng | Assumption map, snapshot hoặc survey |
| CP4 — Research | | Hưng | Bảng research có link |
| CP5 — Quy trình trước/sau | | Hưng | Quy trình + bảng before/after |
| CP5 — Problem Statement v0 | Bảo | Hưng | Problem Statement v0 |
| CP6 — Mức can thiệp + Problem Statement v1 | Việt Anh | Hưng, Bảo | Ma trận, AI Canvas, eval, Problem Statement v1 |
| CP6 — Quyết định | Hưng | | 4 rủi ro + Go/Not Yet/No-Go |

## Cá nhân

Mỗi thành viên thêm một mục theo mẫu dưới đây, tiêu đề là `HoVaTen-MSSV`.

### DoanSyHung-2A202603990

**Phần việc phụ trách:**

- Chọn candidate problem (CP3).
- Quyết định (CP6): 4 rủi ro và Go / Not Yet / No-Go.

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Pitch 3 candidate (error analysis hằng tuần, tái hiện lỗi support báo, tạo eval set từ ticket); nhận phản biện từ Bảo, Ly, Việt Anh.
- Chấm điểm shortlist #4, #2, #1 theo 7 tiêu chí, chọn #4 (33/35 điểm) và viết lý do loại từng candidate còn lại.
- Đánh giá 4 rủi ro Value / Usability / Feasibility / Viability, kết luận Go phạm vi nhỏ.
- Thiết kế pilot 4 tuần và đặt 4 ngưỡng dừng (sửa trên 30% nhãn AI trong 2 tuần liên tiếp, nhóm top 3 bị gán sai, nhãn đổi quá 2 nhãn/tuần, không được gửi dữ liệu ra API ngoài).

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- `report/team/group_report.md`: mục 2.4 (Chấm điểm shortlist, lý do chọn và loại) và mục 8 (Quyết định).
- `report/individual/2A202603990_DoanSyHung.md`: scan 10 problem, top 3 Problem Cards, reflection.

**Điều mình học được từ phần nhóm:**

- Con số ban đầu (85% trùng nhãn) chỉ từ 40 câu nên chưa đủ để kết luận; vì vậy quyết định chọn Go phạm vi nhỏ kèm ngưỡng dừng thay vì Go toàn phần.
- Cần hỏi sớm về quyền dùng dữ liệu (chính sách gửi nội dung ra API ngoài) trước khi chốt giải pháp.


### TranVietAnh-2A202604029

**Phần việc phụ trách:**

- Gom cluster / cây OST (CP3)
- Mức can thiệp AI (CP6)

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Gom cluster / cây OST (CP3):
  - Tham gia phân nhóm 12 candidate problems thành 4 cluster dựa trên bản chất bottleneck: (A) phân loại và gắn nhãn văn bản hàng loạt, (B) tìm kiếm và nắm ngữ cảnh trong tri thức hoặc code phân tán, (C) tổng hợp và đối chiếu nhiều nguồn hoặc nhiều lần chạy, (D) giảm vòng chờ và kiểm tra lặp lại giữa người không chuyên và người chuyên môn. Xác định vị trí các candidate do mình đề xuất trong hệ thống cluster: #7, #9 thuộc cụm B và #8 thuộc cụm C. Tham gia xây dựng Opportunity Solution Tree, góp phần phân biệt opportunity (nhu cầu và pain thực tế) với solution (công cụ hoặc tính năng được đề xuất).
  - Sản phẩm: Bảng phân nhóm 12 candidates thành 4 clusters và cây OST rút gọn với một outcome cùng 3 opportunities.
- Mức can thiệp AI (CP6):
  - Phân tích độ mơ hồ và độ phức tạp của bài toán phân loại nguyên nhân câu trả lời sai sau eval RAG, xác định bài toán nằm ở mức trung bình trên cả hai trục. Tham gia so sánh 4 mức No AI, Rule, Workflow và Agent theo khả năng giải quyết, điều kiện áp dụng và rủi ro. Đề xuất phân chia trách nhiệm giữa Rule, AI và Human: Rule tính metrics và tổng hợp số liệu; AI gợi ý nhãn nguyên nhân, soạn nháp báo cáo; Khoa kiểm duyệt và đưa ra quyết định cuối cùng.
  - Sản phẩm: Ma trận so sánh 4 mức can thiệp, AI Canvas rút gọn và đề xuất mức Workflow được nhóm lựa chọn.


**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- `report/team/group_report.md`: các mục 2.1 - Pitch, 2.2 - Cluster, 2.3 - OST, 2.4 - Chấm điểm shortlist; các mục trong CP6, bao gồm 6.1 - Ma trận độ mơ hồ × độ phức tạp, 6.2 - So sánh 4 mức, 6.3 - AI Canvas rút gọn, 6.4 - Hai câu hỏi của Google PAIR; đề xuất nội dung muc 9 - Hạn chế và hướng tiếp theo.
- `report/individual/2A202604029_TranVietAnh.md`: scan 5 problem, top 3 Problem Cards, reflection.

**Điều mình học được từ phần nhóm:**

- Qua phần gom cluster và xây dựng OST, mình hiểu rằng các problem có thể xuất phát từ những lĩnh vực khác nhau nhưng vẫn có chung bản chất bottleneck. Việc phân nhóm giúp nhóm nhìn ra những pattern chung và tránh đánh giá các ý tưởng một cách rời rạc.
- Ở CP6, điều quan trọng nhất mình học được là không phải bài toán nào cũng cần sử dụng mức AI can thiệp cao nhất. Cần xác định chính xác phần nào có thể giải quyết bằng quy trình hoặc Rule, phần nào thực sự cần khả năng hiểu ngữ cảnh của AI và phần nào nên giữ con người kiểm soát. Việc nhóm lựa chọn Workflow thay vì Agent cho thấy một giải pháp tốt không nhất thiết phải tự động hóa toàn bộ quy trình, mà cần cân bằng giữa hiệu quả, độ chính xác và khả năng kiểm soát rủi ro.

### TuHuyBao-2A202604021

**Phần việc phụ trách:**

- Pitch Problem Card (CP3).
- Phản biện bài của bạn khác và nhận phản biện.
- Problem Statement 

**Đóng góp cụ thể** (mình đã làm gì, ra sản phẩm gì):

- Pitch 3 candidate (text-to-SQL cho nhân viên marketing, phân tích khen/chê từ bình luận và tin nhắn fanpage, kiểm tra bản nháp theo quy tắc thương hiệu). Mỗi candidate có actor, bottleneck và số liệu đi kèm.
- Nhận phản biện từ Ly, Hưng và Anh. Sửa bằng cách bổ sung phương án No AI/Rule làm baseline cho từng candidate, và thêm cơ chế kiểm chứng cho #1 (giải thích query bằng ngôn ngữ thường, chỉ đọc, bộ câu hỏi test có đáp án từ analyst). Sau đó đồng ý chuyển sang candidate của Hưng vì cả 3 câu hỏi chưa được trả lời đủ chắc.
- Gom 12 candidate thành 4 cụm theo bản chất bottleneck
- Viết Problem Statement v0 (Actor, Quy trình, Bottleneck, Impact, Success Metric, Boundary). Góp ý cho v1: thêm metric chất lượng (nhãn AI trùng nhãn cuối từ 80% trở lên, số câu hỏi lại của Tech Lead và PM không tăng) và giới hạn Actor ở team có từ 20 câu sai/tuần. Tham gia soạn danh sách 8 nhãn nguyên nhân và 4 tiêu chí đánh giá đầu ra của AI. Kết quả: v1 có 3 chỉ số thay vì 1, thêm AI intervention point và cột "Rủi ro và người kiểm tra".

**Bằng chứng** (phần nào trong `group_report.md`, file nào trong `report/assets/`, commit nào):

- `report/team/group_report.md`: mục Problem Card, mục Problem Statement v0/v1 và bảng "Thay đổi so với v0".
- `report/individual/2A202604021_TuHuyBao.md`:

**Điều mình học được từ phần nhóm:**

- Một metric chỉ đo tốc độ là chưa đủ cần thêm metric chất lượng bên cạnh metric thời gian.
- Phản biện là cách kiểm tra ý tưởng của chính mình. Cả 3 candidate của mình đều bị hỏi những điều chưa trả lời chắc (số sai mà người dùng không biết, đã có công cụ có sẵn, checklist có thể đủ). Việc nhận ra điều đó giúp mình đồng ý chọn candidate có actor và số liệu rõ hơn.
- Phải luôn đặt phương án No AI/Rule làm baseline trước khi khẳng định cần AI.

