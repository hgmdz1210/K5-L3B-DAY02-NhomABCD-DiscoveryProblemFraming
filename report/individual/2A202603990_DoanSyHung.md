# Báo cáo cá nhân — 2A202603990_DoanSyHung

> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).

## 1. Thông tin học viên

- Họ tên: Đoàn Sỹ Hưng
- MSSV: 2A202603990
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: Nhóm ABCD
- Link repo nhóm: https://github.com/hgmdz1210/K5-L3B-DAY02-NhomABCD-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Lặp lại | Khi xong lần chạy eval mỗi tuần, tôi muốn biết các câu sai hỏng vì nguyên nhân gì, để báo cáo và chọn việc sửa trước buổi planning | Hưng, Tech Lead, PM | Tự bấm giờ 2 tuần gần nhất: 125 và 135 phút |
| 2 | Tốn thời gian | Khi cần mở rộng bộ eval, tôi muốn có sẵn cặp câu hỏi và đáp án từ ticket hỗ trợ, để eval sát thực tế | Hưng, support | Khoảng 3 giờ mỗi lần, 1 lần/tháng |
| 3 | Tốn thời gian | Khi nhận PR đổi prompt, tôi muốn thấy thay đổi ảnh hưởng câu nào, để review đúng chỗ | Reviewer | 20–30 phút/PR, 3 PR/tuần |
| 4 | Lặp lại | Khi một experiment kết thúc, tôi muốn ghi cấu hình và kết quả vào bảng so sánh, để không phải tìm lại sau | Cả team | 15 phút/experiment, khoảng 5 experiment/tuần |
| 5 | Cần đọc, tổng hợp | Khi có bài viết mới về chunking hoặc reranking, tôi muốn biết phần nào áp dụng được, để thử đúng thứ | Hưng | Khoảng 1 giờ/tuần, ít khi dùng lại |
| 6 | Pain từ người khác | Khi support báo bot trả lời sai, họ muốn có lời giải thích nhanh, để trả lời khách | Support lead | Tìm trace mất 15 phút/lần, 4 lần/tuần (đếm từ thread Slack) |
| 7 | Pain từ người khác | Khi họp planning, Tech Lead muốn biết tuần này chất lượng đổi vì sao, để chọn việc sửa | Tech Lead | 4/10 tuần gần nhất báo cáo đến sau buổi planning |
| 8 | Tốn thời gian | Khi đổi model hoặc phiên bản API, tôi muốn biết chất lượng có tụt không, để không phát hiện muộn | Hưng, Tech Lead | Chạy lại và so sánh thủ công 40 phút/lần, 2 lần/tháng |
| 9 | Cần đọc, tổng hợp | Khi pipeline thay đổi, tôi muốn cập nhật mô tả (README) nhanh, để tài liệu không lỗi thời | Cả team | 30 phút/lần, hay bị bỏ quên |
| 10 | Lặp lại | Khi tới standup, tôi muốn có sẵn tóm tắt các run chạy qua đêm, để không phải mở từng log | Hưng | 5–10 phút/ngày |

**Nếu có dùng AI để gợi ý thêm:** sau khi tự scan 8 ý, Hưng hỏi AI và giữ lại #8 (regression khi đổi model) và #10 (tóm tắt run qua đêm). Bỏ ý "AI tự cải thiện prompt không cần người" và "AI tự gán nhãn toàn bộ dữ liệu huấn luyện" vì quá rộng và không có quy trình thật nào đứng sau.

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Error analysis hằng tuần (#1) | Quy trình rõ, tốn thời gian, có baseline đo thật | Nhãn nguyên nhân "đủ đúng" đo thế nào? AI có gán nhãn nhất quán không? |
| 2 | Tái hiện lỗi support báo (#6) | Pain từ người khác, nhiều người cần | Phụ thuộc logging; trace có thể chứa dữ liệu khách hàng |
| 3 | Tạo eval set từ ticket (#2) | Ảnh hưởng lớn tới chất lượng đo | Ticket chứa thông tin khách hàng, cần quyền truy cập; chỉ làm 1 lần/tháng |

### Problem Card #1 — Error analysis hằng tuần

| Trường | Nội dung |
|---|---|
| Job Story | Khi xong lần chạy eval mỗi tuần, tôi muốn biết các câu sai hỏng vì nguyên nhân gì, để báo cáo và chọn việc sửa trước buổi planning |
| Actor | Junior AI Engineer phụ trách đánh giá một hệ thống RAG, gửi báo cáo cho Tech Lead và PM |
| Thời điểm / bối cảnh | Chiều thứ Hai, trước buổi planning lúc 15h |
| Quy trình hiện tại (3–7 bước) | 1. Chạy eval 300 câu<br>2. Tính metric tổng<br>3. Lọc câu sai<br>4. Đọc từng câu sai và gán nguyên nhân<br>5. Gom nhóm, đếm tỉ lệ<br>6. Viết báo cáo và đề xuất sửa<br>7. Review và gửi |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 4: đọc và gán nhãn khoảng 60 câu sai, mỗi câu khoảng 1 phút, tổng khoảng 60 phút |
| Impact (nếu không giải thì sao) | 130 phút/tuần cho 1 kỹ sư; 2 hệ thống RAG nên khoảng 260 phút/tuần (4,3 giờ); 4/10 tuần gần nhất báo cáo đến sau planning; gán lại 20 câu của tuần trước thì 6/20 câu ra nhãn khác lần đầu |
| Success metric (baseline → target) | Tổng thời gian từ 130 phút xuống dưới 60 phút; nhãn không kém nhất quán hơn hiện tại |
| Phương án không dùng AI | Danh sách nhãn cố định + Google Sheets có dropdown + script lọc và gom nhóm: giảm lỗi gán nhãn lệch và thời gian gom nhóm, chưa giảm thời gian đọc từng câu |
| Giả thuyết về AI (nếu có) | AI gợi ý nhãn nguyên nhân theo danh sách cố định và soạn nháp báo cáo; Hưng duyệt từng nhãn trước khi gửi |
| Cảm nhận nhanh | Workflow |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 130 phút

[1 Chạy eval: 10'] → [2 Tính metric: 10'] → [3 Lọc câu sai: 10']
→ [4 Đọc + gán nhãn ~60 câu: 60'] ← BOTTLENECK
→ [5 Gom nhóm, đếm: 15'] → [6 Viết báo cáo: 20'] → [7 Review + gửi: 5']
```

### Problem Card #2 — Tái hiện lỗi support báo

| Trường | Nội dung |
|---|---|
| Job Story | Khi support báo bot trả lời sai, tôi muốn tái hiện lỗi nhanh, để giải thích cho khách |
| Actor | Kỹ sư AI nhận ticket từ support |
| Thời điểm / bối cảnh | Bất kỳ lúc nào trong tuần khi support chuyển ticket "bot trả lời sai" |
| Quy trình hiện tại (3–7 bước) | 1. Nhận ticket qua Slack<br>2. Tìm trace của hội thoại<br>3. Tìm tài liệu nguồn mà bot đã truy xuất<br>4. Chạy lại câu hỏi để tái hiện<br>5. Giải thích nguyên nhân cho support |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 2–3: tìm đúng trace và tài liệu nguồn, khoảng 15 phút/lần, 4 lần/tuần (khoảng 1 giờ/tuần, đếm từ thread Slack) |
| Impact (nếu không giải thì sao) | Support chờ lâu mới trả lời được khách; kỹ sư bị ngắt việc nhiều lần trong tuần |
| Success metric (baseline → target) | 15 phút → dưới 3 phút/lần |
| Phương án không dùng AI | Script tra trace theo mã hội thoại; template ticket bắt buộc có mã hội thoại |
| Giả thuyết về AI (nếu có) | Chưa rõ cần AI; phần tìm trace có thể giải bằng Rule |
| Cảm nhận nhanh | Rule hoặc Workflow |

Quy trình nháp hiện tại:

```text
[Nhận ticket] → [Tìm trace: ~10'] → [Tìm tài liệu nguồn: ~5'] → [Chạy lại câu hỏi] → [Giải thích cho support]
```

### Problem Card #3 — Tạo eval set từ ticket

| Trường | Nội dung |
|---|---|
| Job Story | Khi cần mở rộng bộ eval, tôi muốn có sẵn cặp câu hỏi và đáp án từ ticket hỗ trợ, để eval sát thực tế |
| Actor | Kỹ sư AI |
| Thời điểm / bối cảnh | Khoảng 1 lần/tháng khi cần bổ sung bộ eval |
| Quy trình hiện tại (3–7 bước) | 1. Xuất ticket từ hệ thống support<br>2. Đọc và chọn ticket phù hợp<br>3. Viết lại câu hỏi, ẩn dữ liệu cá nhân<br>4. Viết đáp án chuẩn<br>5. Thêm vào bộ eval |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3–4: viết lại câu hỏi và đáp án chuẩn, ẩn dữ liệu cá nhân, khoảng 3 giờ/lần |
| Impact (nếu không giải thì sao) | Bộ eval lỗi thời, không phản ánh câu hỏi thật của khách; chất lượng đo sai |
| Success metric (baseline → target) | 3 giờ → 1 giờ/lần |
| Phương án không dùng AI | Template cặp câu hỏi/đáp án và checklist ẩn dữ liệu cá nhân |
| Giả thuyết về AI (nếu có) | AI soạn nháp cặp câu hỏi/đáp án và che thông tin cá nhân, người duyệt |
| Cảm nhận nhanh | Workflow |

Quy trình nháp hiện tại:

```text
[Xuất ticket] → [Chọn ticket] → [Viết lại câu hỏi + ẩn dữ liệu cá nhân] → [Viết đáp án chuẩn: ~3h cho bước 3–4] → [Thêm vào eval]
```

### Card muốn pitch nhất

- Card số: #1 (Error analysis hằng tuần)
- Vì sao: quy trình và bottleneck rõ nhất, có baseline bấm giờ thật, và so sánh được đủ 4 mức No AI / Rule / Workflow / Agent.
- Câu hỏi muốn nhóm phản biện: Nhãn nguyên nhân do AI gợi ý phải trùng người ở mức nào thì mới dùng được? Có team nào chỉ cần metric tổng không?

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Baseline 130 phút chỉ dựa trên trí nhớ | Đồng ý | Bấm giờ thật 2 tuần: 125 và 135 phút |
| Chưa chắc Tech Lead dùng bảng nguyên nhân để quyết định | Đồng ý một phần | Đưa vào danh sách giả định cần kiểm chứng ở CP4 |
| Gợi ý agent tự sửa prompt sau khi phân tích | Không đồng ý | Giữ boundary: AI không tự sửa prompt hay pipeline |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Pitch 3 candidate: error analysis hằng tuần, tái hiện lỗi support báo, tạo eval set từ ticket (#4, #5, #6 trong báo cáo nhóm) | #4 vào shortlist và được nhóm chọn (33/35 điểm) |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: hỏi Việt Anh "Làm thế nào để xác định những module và file code thực sự liên quan đến feature mà không phải đọc toàn bộ project?"; hỏi Ly "Làm thế nào để xác định một Research Gap thực sự tồn tại chứ không chỉ là vấn đề bạn chưa tìm thấy trong các paper đã đọc?" | Hai candidate này được xếp vào cụm B và C, thiếu số liệu bottleneck nên không vào shortlist |
| Nhận phản biện | Câu hỏi tôi nhận được: Bảo hỏi "Chỉ xem metric tổng thì có đủ không?"; Ly hỏi "Log hiện tại có lưu đủ trace và đoạn tài liệu truy xuất không?"; Anh hỏi "Ticket có thông tin khách hàng, bạn được phép dùng chưa?" | Tôi đã sửa: thêm phương án No AI cho team chỉ cần metric tổng; loại #6 (eval set từ ticket) vì rủi ro dữ liệu khách hàng |
| Gom cluster / cây OST | Anh phụ trách | |
| Chọn candidate problem | Hưng phụ trách: chấm điểm shortlist 7 tiêu chí cho #4, #2, #1; chọn #4 (33/35 điểm); viết lý do chọn #4 và lý do loại từng candidate còn lại (#1, #2, #3, #6, cụm B, cụm C) | Nhóm chọn #4 (phân loại nguyên nhân câu sai sau eval RAG hằng tuần) |
| Kiểm chứng / research | Ly phụ trách | |
| Quy trình nhóm | Ly phụ trách | |
| Problem Statement | Bảo phụ trách | |
| Mức can thiệp AI | Anh phụ trách | |
| Quyết định | Hưng phụ trách: đánh giá 4 rủi ro Value/Usability/Feasibility/Viability; kết luận Go phạm vi nhỏ; thiết kế pilot 4 tuần; đặt 4 ngưỡng dừng | Nhóm Go phạm vi nhỏ, pilot 4 tuần (mục 8 báo cáo nhóm) |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Gợi ý thêm problem theo vai trò AI engineer | Nhớ ra #8 (regression khi đổi model) và #10 | Một ý quá rộng ("AI tự cải thiện prompt") | Bỏ ý không có quy trình thật |
| CP2 Problem Card | Đóng vai Tech Lead hoài nghi | Chỉ ra baseline chỉ dựa trên trí nhớ | Gợi ý agent tự sửa prompt sau khi phân tích | Giữ boundary: AI không tự sửa |
| CP4 Research | Tìm công cụ tương tự và tóm tắt tài liệu | Gợi ý Langfuse, Phoenix, Ragas | Nói LangSmith Insights có ở mọi gói; đưa 1 link tài liệu đã đổi địa chỉ | Tự mở từng link, kiểm lại gói: Insights chỉ cho Plus và Enterprise tại thời điểm công bố |
| CP5 Quy trình | Chuyển mô tả sang bảng bước | Nhanh | Gộp "duyệt nhãn" và "soạn báo cáo" thành 1 bước | Tách lại vì bottleneck nằm ở duyệt nhãn |
| CP5–6 Problem Statement | Đề xuất danh sách nguyên nhân lỗi | Có thêm nhãn "đáp án tham chiếu sai" mà tôi chưa nghĩ ra | Đưa 14 nhãn, nhiều nhãn trùng nghĩa | Rút còn 8, kiểm bằng 40 câu thật |
| CP6 Mức can thiệp / quyết định | | | | |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

Nghe top 3 của các bạn, mình thấy cùng một việc có thể được mô tả ở mức rất khác nhau. Câu hỏi của Việt Anh về ticket làm mình nhận ra phải hỏi “mình có được phép dùng dữ liệu này không” ngay từ đầu, vì ticket chứa thông tin khách hàng. Trước đó mình chỉ nghĩ tới việc có làm được hay không.

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

Có. Lúc đầu mình định “xây công cụ tự động phân loại lỗi và vẽ dashboard” khi chưa biết lỗi nào đáng phân loại. Nhóm nhận ra khi Bảo hỏi “chỉ xem metric tổng thì có đủ không?” và mình không có số liệu để trả lời. Nhóm gạch các ý solution khỏi cây Opportunity, rồi đi phỏng vấn trước khi bàn giải pháp.

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

Có. Mình định để AI tự sửa prompt sau khi phân tích lỗi. Sau phản biện và thí nghiệm gán nhãn (LLM trùng với mình 72,5%, sau chỉnh định nghĩa nhãn lên 85%), mình đổi sang AI chỉ gợi ý nhãn, còn người duyệt.

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

Có hai điều. Một người được phỏng vấn chỉ nhìn metric tổng, nên Problem Statement không đúng với mọi team và nhóm phải thu hẹp đối tượng. Ngoài ra, Langfuse, LangSmith và Phoenix đã có sẵn phần giao diện và gom nhóm, nên không cần tự xây.

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

Khó nhất là viết Bottleneck và Impact bằng con số có nguồn. Mình hay viết “mất nhiều thời gian”, nên phải bấm giờ thật (125 và 135 phút) mới viết được “130 phút, riêng đọc và gán nhãn 60 phút”.

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

Mình sẽ hỏi Tech Lead thật trước khi chốt metric, vì hai giả định quan trọng nhất (danh sách nhãn ổn định, Tech Lead dùng bảng nguyên nhân) vẫn chưa kiểm chứng. Mình cũng sẽ phản biện nhóm mạnh hơn ở con số 85%: nó chỉ đến từ 40 câu, nên cần thêm mẫu trước khi dùng nó để chọn Workflow.

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

Problem là Junior AI Engineer mất 130 phút mỗi tuần để phân tích lỗi RAG, trong đó 60 phút là đọc và gán nhãn khoảng 60 câu sai. Quy trình có 7 bước và bước 4 là bottleneck. Metric thành công gồm tổng thời gian dưới 60 phút, AI trùng nhãn cuối của người từ 80%, và số câu hỏi lại của Tech Lead không tăng. Boundary là AI không tự gửi, không tự sửa prompt, không đặt nhãn ngoài danh sách 8 nhãn. Vì các bước cố định nhưng nguyên nhân từng câu cần đọc ngữ cảnh, nhóm chọn mức Workflow và không chọn Agent vì 15% nhãn vẫn sai. Quyết định là Go phạm vi nhỏ, pilot 4 tuần, và dừng nếu người phải sửa hơn 30% nhãn trong hai tuần liên tiếp.

---

## 7. Tài liệu tham khảo

- [Langfuse: annotation queues](https://langfuse.com/docs/evaluation/evaluation-methods/annotation-queues) và [hướng dẫn error analysis](https://langfuse.com/blog/2025-08-29-error-analysis-to-evaluate-llm-applications)
- [LangSmith Insights Agent](https://docs.langchain.com/langsmith/insights)
- [Arize Phoenix](https://phoenix.arize.com)
- [Ragas](https://docs.ragas.io)
