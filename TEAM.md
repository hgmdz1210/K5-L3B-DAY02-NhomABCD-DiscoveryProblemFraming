# Team

> Điền file này trên repo chung do nhóm trưởng fork. Nhóm điền phần **Thông tin nhóm** và **Thành viên**. Mỗi người tự điền phần của mình trong **Cá nhân**. Không copy file này sang repo khác.

## Thông tin nhóm

- Tên nhóm: ABCD
- Candidate problem nhóm chọn (1 câu): Khi xong eval hằng tuần, Junior AI Engineer phụ trách đánh giá RAG muốn biết các câu sai hỏng vì nguyên nhân gì để báo cáo và chọn việc sửa trước planning, nhưng mất khoảng 60/130 phút chỉ để đọc và gán nhãn khoảng 60 câu sai.
- Quyết định cuối (Go / Not Yet / No-Go): Go (phạm vi nhỏ)

## Thành viên

| STT | Họ và tên | MSSV | Vai trò trong nhóm | Tài khoản GitHub |
|---:|---|---|---|---|
| 1 | Đoàn Sỹ Hưng | 2A202603990 | Trưởng nhóm | hgmdz1210 |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |

Không ghi email hay số điện thoại vào bảng này, vì repo có thể để public.

Gợi ý vai trò (một người có thể giữ nhiều vai): điều phối thời gian, ghi chép, người phản biện chính, phụ trách kiểm chứng (phỏng vấn/survey), phụ trách research, vẽ quy trình, viết Problem Statement.

## Phân công theo checkpoint

| Checkpoint | Người chính | Người hỗ trợ | Sản phẩm |
|---|---|---|---|
| CP3 — Hội tụ nhóm | | Hưng | Cluster, cây OST, bảng chấm điểm |
| CP4 — Kiểm chứng | | Hưng | Assumption map, snapshot hoặc survey |
| CP4 — Research | | Hưng | Bảng research có link |
| CP5 — Quy trình trước/sau | | Hưng | Quy trình + bảng before/after |
| CP5 — Problem Statement v0 | | Hưng | Problem Statement v0 |
| CP6 — Mức can thiệp + Problem Statement v1 | | Hưng | Ma trận, AI Canvas, eval, Problem Statement v1 |
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
