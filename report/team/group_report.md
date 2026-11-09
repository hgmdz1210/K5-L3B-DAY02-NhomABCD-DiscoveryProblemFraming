# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> Bản chung của nhóm, viết trên repo do nhóm trưởng fork. Không copy file này sang repo cá nhân.
> Template chi tiết và prompt mẫu: [docs/01-worksheet.md](../../docs/01-worksheet.md). Bài mẫu: [docs/02-deliverable-example.md](../../docs/02-deliverable-example.md).

## 1. Thông tin nhóm

- Tên nhóm:
- Thành viên: xem `TEAM.md`
- Candidate problem được chọn (1 câu):
- Quyết định cuối: Go / Not Yet / No-Go

---

## 2. Hội tụ nhóm (CP3)

### 2.1. Pitch

| # | Người đưa ra | Candidate (Job Story ngắn) | Actor | Bottleneck | Câu hỏi phản biện nhận được (ai hỏi) |
|---:|---|---|---|---|---|
| 1 | Bảo | Khi cần một con số từ database, tôi muốn hỏi bằng ngôn ngữ tự nhiên, để không phải chờ team data | Nhân viên marketing, không biết SQL | Chờ analyst nhận việc và hỏi đi hỏi lại 2–3 câu làm rõ: trung bình 2 ngày từ lúc gửi yêu cầu tới lúc nhận số, trong khi analyst chỉ mất 10–15 phút để viết query | "Nếu AI viết sai query mà người dùng không biết SQL để kiểm tra thì sao? Số sai còn tệ hơn chờ 2 ngày." (Ly) |
| 2 | Bảo | Khi có hàng trăm bình luận và tin nhắn về sản phẩm, tôi muốn biết khách đang khen và phàn nàn điều gì, để điều chỉnh nội dung và báo lại cho team sản phẩm | Nhân viên marketing phụ trách fanpage và quảng cáo | Đọc và gắn nhãn khen/chê bằng tay: 300+ bình luận/tuần, khoảng 90 phút, dễ bỏ sót hoặc gắn nhãn không nhất quán giữa các tuần | "Công cụ social listening có sẵn đã phân loại cảm xúc rồi, sao phải tự xây?" (Hưng) |
| 3 | Bảo | Khi quản lý duyệt nội dung, họ muốn thấy bản nháp đã đúng quy tắc thương hiệu, để không phải sửa cùng một lỗi nhiều lần | Nhân viên marketing (người viết), quản lý marketing (người duyệt) | Vòng duyệt lặp lại: 40% bài bị trả lại vì sai tone hoặc thiếu thông tin bắt buộc, mỗi lần trả lại mất thêm nửa ngày và làm trễ lịch đăng | "Một checklist quy tắc thương hiệu dài 1 trang có giải quyết được không? Tại sao cần AI?" (Anh) |
| 4 |Hưng |Khi xong eval hằng tuần, tôi muốn biết các câu sai hỏng vì nguyên nhân gì, để báo cáo và chọn việc sửa trước planning |Junior AI Engineer phụ trách đánh giá RAG |Đọc và gán nhãn khoảng 60 câu sai (60/130 phút), nhãn lệch giữa các lần gán |“Chỉ xem metric tổng thì có đủ không?”(Bảo) |
| 5 |Hưng |Khi support báo bot trả lời sai, tôi muốn tái hiện lỗi nhanh, để giải thích cho khách |Kỹ sư AI nhận ticket từ support |Tìm đúng trace và tài liệu nguồn: 15 phút/lần, 4 lần/tuần |“Log hiện tại có lưu đủ trace và đoạn tài liệu truy xuất để tái hiện lỗi không?”(Ly) |
| 6 |Hưng |Khi cần mở rộng bộ eval, tôi muốn có sẵn cặp câu hỏi và đáp án từ ticket, để eval sát thực tế |Kỹ sư AI |Viết lại câu hỏi và đáp án chuẩn, ẩn dữ liệu cá nhân: khoảng 3 giờ/lần |“Ticket có thông tin khách hàng, bạn được phép dùng chưa?”(Anh) |
| 7 |Việt Anh |Khi bắt đầu làm việc trên một project có nhiều module và file code, tôi muốn nhanh chóng hiểu cấu trúc project và luồng xử lý giữa các thành phần, để có thể bắt đầu implement feature mà không phải đọc lại quá nhiều code. |Software Developer, AI Engineer mới tiếp nhận project |Phải đọc nhiều file code, tìm hiểu quan hệ giữa các module và lần theo luồng xử lý để xác định vị trí cần thay đổi |Làm thế nào để xác định những module và file code thực sự liên quan đến feature cần implement mà không phải đọc toàn bộ project? (Hưng) |
| 8 |Việt Anh |Khi thực hiện nhiều thí nghiệm huấn luyện mô hình với các cấu hình khác nhau, tôi muốn tổng hợp và so sánh kết quả của các lần chạy trong cùng một nơi, để xác định mô hình và cấu hình phù hợp nhất |ML Engineer, AI Researcher |Metrics, log, checkpoint và cấu hình của các lần chạy nằm ở nhiều nơi, khiến việc tổng hợp, đối chiếu và so sánh kết quả mất thời gian |Nếu chuẩn hóa việc lưu metrics và sử dụng dashboard để so sánh thì đã giải quyết được vấn đề chưa, hay thực sự cần AI phân tích kết quả experiment? (Ly) |
| 9 |Việt Anh |Khi một thành viên mới tham gia project, tôi muốn họ có thể tự tìm hiểu cấu trúc và quy trình làm việc của project, để không phải liên tục hỏi các thành viên cũ về những thông tin cơ bản |Thành viên mới, Mentor, Team Leader |Kiến thức về cấu trúc project, tài liệu hướng dẫn và quy trình làm việc phân tán hoặc chưa được tài liệu hóa đầy đủ, khiến thành viên mới phải hỏi lại người cũ nhiều lần |Làm thế nào để xác định thành viên mới đã hiểu đủ về project để tự làm việc? Có thể giải quyết bằng cách chuẩn hóa tài liệu onboarding thay vì sử dụng AI không? (Bảo) |
| 10 |Ly |Khi thực hiện nghiên cứu, tôi muốn hệ thống hóa và so sánh các phương pháp từ nhiều paper để lựa chọn hướng tiếp cận phù hợp |Sinh viên, nhà nghiên cứu |Khó đối chiếu phương pháp do paper sử dụng cấu trúc và tiêu chí đánh giá khác nhau | |
| 11 | Ly|Khi đề xuất nghiên cứu mới, tôi muốn xác định những hạn chế và vấn đề chưa được giải quyết để tìm ra Research Gap có cơ sở khoa học |Sinh viên, nghiên cứu viên |Khó tổng hợp hạn chế từ nhiều nghiên cứu và chứng minh tính mới của khoảng trống | |
| 12 | Ly| Khi thực hiện nghiên cứu dài hạn, tôi muốn quản lý các phiên bản tài liệu, mã nguồn và kết quả để tránh nhầm lẫn|Sinh viên, nhóm nghiên cứu |Khó truy xuất phiên bản và liên kết kết quả với cấu hình tương ứng | |

### 2.2. Cluster

| Cluster | Các candidate | Pattern chung |
|---|---|---|
| A | | |
| B | | |
| C | | |

### 2.3. Opportunity Solution Tree rút gọn

Gốc là **1 outcome**. Nhánh là **opportunity** (nhu cầu, pain), không phải tính năng hay công cụ.

```text
OUTCOME: 
├── Opportunity A: 
├── Opportunity B: 
└── Opportunity C: 
```

Những ý đã gạch bỏ vì là solution đội lốt opportunity:

-

### 2.4. Chấm điểm shortlist (1–5)

| Candidate | Actor rõ | Quy trình rõ | Pain có bằng chứng | Impact đo được | Vừa sức lab | So sánh được No AI/Rule/Workflow/Agent | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| | | | | | | | | |
| | | | | | | | | |
| | | | | | | | | |

**Candidate được chọn:**

**Vì sao chọn:**

**Vì sao loại các candidate còn lại:**

**Xử lý bất đồng (nếu có):**

---

## 3. Kiểm chứng + research giải pháp đã có (CP4)

### 3.1. Assumption Map

| # | Giả định | Loại (Value / Usability / Feasibility / Viability) | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
|---:|---|---|---:|---:|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |
| 6 | | | | | |

*Điền 4–6 giả định; xóa dòng thừa.*

Giả định nhóm kiểm chứng trong buổi này:

### 3.2. Kiểm chứng

Cách đã dùng: Phỏng vấn / Survey / Log, ticket, review

Interview snapshot (mỗi buổi phỏng vấn một bảng, hoặc đặt file trong `report/assets/cp4-interview-snapshot-N.md`):

| Trường | Nội dung |
|---|---|
| Người được hỏi (vai trò, không ghi tên thật) | |
| Câu nói đáng nhớ nhất (nguyên văn) | |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | |
| Hiện đang xử lý bằng cách nào (workaround)? | |
| Mất bao lâu, bao lần? | |
| Insight / opportunity rút ra | |

Tổng hợp:

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác |
|---|---:|---|---|
| | | | |

**Nhóm đã sửa problem thế nào sau kiểm chứng:**

### 3.3. Research giải pháp đã có

| Công cụ / case / pattern | Link | Giải bước nào trong quy trình? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| | | | | | |
| | | | | | |
| | | | | | |

---

## 4. Quy trình trước/sau (CP5)

### 4.1. Quy trình hiện tại

Sơ đồ (ASCII, Mermaid hoặc link ảnh trong `report/assets/`):

```text

```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú |
|---:|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |

**Bottleneck chính:**

### 4.2. Quy trình tương lai

Ghi rõ bước nào **Rule**, bước nào **AI**, bước nào **con người**, **boundary** ở đâu, **phương án quay về** khi AI sai.

```text

```

### 4.3. Before / after

| Chỉ số | Trước | Sau (kỳ vọng) | Ghi chú |
|---|---:|---:|---|
| Số bước | | | |
| Tổng thời gian | | | |
| Số bước thủ công | | | |
| Bottleneck chính | | | |
| Rủi ro mới phát sinh | | | |

---

## 5. Problem Statement v0 (CP5)

| Trường | Nội dung |
|---|---|
| **Actor** | |
| **Quy trình** | |
| **Bottleneck** | |
| **Impact** | |
| **Success Metric** (baseline → target, cách đo) | |
| **Boundary** (AI không được làm gì; khi nào cần con người kiểm tra — HITL) | |

Phản biện nhận được (từ AI hoặc nhóm khác) và nhóm có đồng ý không:

-

---

## 6. Mức can thiệp AI (CP6)

### 6.1. Ma trận độ mơ hồ × độ phức tạp

Bài của nhóm nằm ở ô:

Vì sao:

### 6.2. So sánh 4 mức

| Mức | Phương án cho bài của nhóm | Đủ khi nào | Rủi ro | Chọn? |
|---|---|---|---|---|
| **No AI** (sửa quy trình) | | | | |
| **Rule** | | | | |
| **Workflow** | | | | |
| **Agent** | | | | |

**Mức chọn:**

**Vì sao không chọn mức đơn giản hơn:**

### 6.3. AI Canvas rút gọn

| Thành phần | Nội dung |
|---|---|
| **Prediction** — AI dự đoán / tạo ra gì? | |
| **Judgment** — con người cân nhắc, quyết định gì? | |
| **Action** — hành động cuối cùng là gì, ai làm? | |
| **Outcome** — đo kết quả bằng gì? | |
| **Input** — AI cần dữ liệu đầu vào gì mỗi lần chạy? Có sẵn không? | |
| **Feedback** — lấy phản hồi ở đâu để cải thiện? | |

### 6.4. Hai câu hỏi của Google PAIR

- Người dùng muốn **được hỗ trợ (augment)** hay **giao hẳn việc (automate)**? Bằng chứng:
- AI sai kiểu nào tệ hơn, **báo nhầm** hay **bỏ sót**? Vì sao, và thiết kế đã xử lý thế nào:

---

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

| Trường | Nội dung |
|---|---|
| **Actor** | |
| **Quy trình** | |
| **Bottleneck** | |
| **Impact** | |
| **Success Metric** (baseline → target, cách đo) | |
| **Boundary** | |
| **AI intervention point** | |
| **Mức chọn** | No AI / Rule / Workflow / Agent |
| **Rủi ro & người kiểm tra** | |

**Thay đổi so với v0 và lý do:**

| Trường | v0 | v1 | Vì sao đổi |
|---|---|---|---|
| | | | |

**Tiêu chí đánh giá đầu ra của AI (3–5 tiêu chí):**

| # | Tiêu chí | Đạt khi | Không đạt khi |
|---:|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |

---

## 8. Quyết định (CP6)

### 8.1. Bốn rủi ro

| Rủi ro | Câu hỏi | Mức độ rủi ro (Thấp = an toàn / TB / Cao = nguy hiểm) | Lý do / bằng chứng |
|---|---|---|---|
| **Value** | Người dùng có thật sự cần và sẽ dùng không? | | |
| **Usability** | Người dùng có dùng được, có hiểu và sửa được đầu ra của AI không? | | |
| **Feasibility** | Có đủ dữ liệu, công cụ, kỹ năng để làm không? | | |
| **Viability** | Có hợp chi phí, pháp lý, quy định tổ chức không? Ai vận hành? | | |

### 8.2. Kết luận

**Quyết định:** Go / Not Yet / No-Go

**Lý do:**

**Nếu Go — pilot nhỏ nhất:**

**Nếu Not Yet — cần kiểm chứng gì trước:**

**Nếu No-Go — nên làm gì thay AI:**

**Ngưỡng dừng** (nếu sau … mà … thì quay về …):

---

## 9. Hạn chế và hướng tiếp theo

-

## 10. Tài liệu tham khảo

-
