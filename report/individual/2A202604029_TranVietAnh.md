# Báo cáo cá nhân — MSSV_HoTen

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Trần Việt Anh
- MSSV: 2A202604029
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: Nhóm 3
- Link repo nhóm: https://github.com/hgmdz1210/K5-L3B-DAY02-NhomABCD-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

|   # | Lăng kính                         | Job Story: Khi… tôi muốn… để…                                                                                                                                                                                               | Ai chịu ảnh hưởng?                            | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng)   |
| --: | --------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------- | ----------------------------------------------------------- |
|   1 | Tốn thời gian                     | Khi bắt đầu làm việc trên một project có nhiều module và file code, tôi muốn nhanh chóng hiểu cấu trúc project và luồng xử lý giữa các thành phần, để có thể bắt đầu implement feature mà không phải đọc lại quá nhiều code | Software Developer, AI Engineer               | Tùy thuộc vào độ lớn của project, nhưng mất ít nhất 2 tiếng |
|   2 | Cần đọc, tổng hợp nhiều thông tin | Khi thực hiện nhiều thí nghiệm huấn luyện mô hình với các cấu hình khác nhau, tôi muốn tổng hợp và so sánh kết quả của các lần chạy trong cùng một nơi, để xác định mô hình và cấu hình phù hợp nhất                        | ML Engineer, AI Researcher                    | 30-60 phút / lần                                            |
|   3 | Tốn thời gian                     | Khi tìm hiểu một thư viện hoặc công nghệ mới phục vụ project, tôi muốn tìm được đúng tài liệu và ví dụ liên quan đến vấn đề đang gặp, để không phải đọc quá nhiều nội dung không cần thiết                                  | Software Developer, AI Engineer, sinh viên IT | 1-2 giờ / lần                                               |
|   4 | Pain từ người khác                | Khi một thành viên mới tham gia project, tôi muốn họ có thể tự tìm hiểu cấu trúc và quy trình làm việc của project, để không phải liên tục hỏi các thành viên cũ về những thông tin cơ bản                                  | Thành viên mới, Mentor, Team Leader           | 1-3 ngày / người                                            |
|   5 | Lặp lại                           | Khi có nhiều deadline học tập và công việc trong cùng một tuần, tôi muốn xác định thứ tự ưu tiên và theo dõi tiến độ các nhiệm vụ, để tránh bỏ sót những công việc quan trọng hoặc hoàn thành trễ hạn                       | Sinh viên, người đi làm                       | 10-15 phút / ngày                                           |
|   6 |                                   |                                                                                                                                                                                                                             |                                               |                                                             |
|   7 |                                   |                                                                                                                                                                                                                             |                                               |                                                             |
|   8 |                                   |                                                                                                                                                                                                                             |                                               |                                                             |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

- ***

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem                          | Vì sao chọn                                                                                                                                           | Điều còn chưa chắc                                                                                                    |
| ---: | -------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
|    1 | Hiểu cấu trúc project (#1)       | Mất ít nhất 2 giờ cho mỗi lần tiếp cận project mới; ảnh hưởng trực tiếp đến tốc độ bắt đầu implement feature và tiến độ phát triển phần mềm           | Thời gian phụ thuộc nhiều vào quy mô project; chưa rõ tần suất gặp vấn đề và phần thời gian thực sự có thể tiết kiệm  |
|    2 | Tổng hợp kết quả experiment (#2) | Quy trình thực hiện nhiều thí nghiệm ML đòi hỏi đối chiếu nhiều metrics và cấu hình; việc tổng hợp thủ công gây tốn thời gian và khó theo dõi kết quả | Chưa rõ số lượng experiment mỗi lần, metrics quan trọng nhất và công cụ người dùng đang sử dụng                       |
|    3 | Tìm kiếm tài liệu kỹ thuật (#3)  | Mất khoảng 1–2 giờ mỗi lần; ảnh hưởng đến cả Software Developer, AI Engineer và sinh viên IT                                                          | Chưa rõ khó khăn chính nằm ở việc tìm kiếm, đánh giá độ tin cậy của tài liệu hay tìm ví dụ phù hợp với vấn đề thực tế |

### Problem Card #1

| Trường                                    | Nội dung                                                                                                                                                                                                                                                                                                                                            |
| ----------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Job Story                                 | Khi bắt đầu làm việc trên một project có nhiều module và file code, tôi muốn nhanh chóng hiểu cấu trúc project và luồng xử lý giữa các thành phần, để có thể bắt đầu implement feature mà không phải đọc lại quá nhiều code                                                                                                                         |
| Actor                                     | Software Developer, AI Engineer                                                                                                                                                                                                                                                                                                                     |
| Thời điểm / bối cảnh                      | Khi tham gia một project mới, nhận task implement feature hoặc cần sửa một module có nhiều dependency với các thành phần khác                                                                                                                                                                                                                       |
| Quy trình hiện tại (3–7 bước)             | 1. Đọc README và tài liệu mô tả project · 2. Xem cấu trúc thư mục và phân loại các module · 3. Tìm các file khởi tạo, entry point và file cấu hình · 4. Đọc các class/function quan trọng để hiểu chức năng từng module · 5. Lần theo luồng xử lý và mối liên hệ giữa các thành phần · 6. Chạy thử project, debug và ghi chú lại những phần đã hiểu |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 4–5: Đọc code và lần theo luồng xử lý giữa các module, mất khoảng 45–60 phút hoặc hơn tùy độ phức tạp của project. Khó khăn nằm ở việc phải mở nhiều file và tự liên kết các thành phần với nhau                                                                                                                                               |
| Impact (nếu không giải thì sao)           | Developer mất ít nhất 2 giờ trước khi thực sự bắt đầu implement feature. Việc hiểu sai kiến trúc hoặc dependency có thể dẫn đến sửa sai module, phát sinh bug và phải đọc lại code hoặc refactor                                                                                                                                                    |
| Success metric (baseline → target)        | Thời gian tìm hiểu cấu trúc và luồng xử lý project: ít nhất 120 phút → dưới 60 phút                                                                                                                                                                                                                                                                 |
| Phương án không dùng AI                   | Chuẩn hóa README, xây dựng Architecture Diagram, sơ đồ dependency giữa các module và tài liệu mô tả luồng xử lý của những chức năng quan trọng                                                                                                                                                                                                      |
| Giả thuyết về AI (nếu có)                 | AI phân tích source code để tạo sơ đồ kiến trúc, giải thích vai trò của từng module, lần theo luồng gọi giữa các function/class và trả lời câu hỏi về codebase kèm dẫn chiếu đến file và vị trí code liên quan                                                                                                                                      |
| Cảm nhận nhanh                            | Workflow                                                                                                                                                                                                                                                                                                                                            |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — Ít nhất 120 phút

[1 Đọc README: 10']
          ↓
[2 Xem cấu trúc thư mục: 15']
          ↓
[3 Tìm entry point + config: 20']
          ↓
[4 Đọc class/function quan trọng: 25']
          ↓
[5 Lần theo luồng xử lý giữa các module: 35']
          ↑
          BOTTLENECK
          ↓
[6 Chạy thử, debug và ghi chú: 15']

```

### Problem Card #2

| Trường                                    | Nội dung                                                                                                                                                                                                                                                                                                                                                         |
| ----------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Job Story                                 | Khi thực hiện nhiều thí nghiệm huấn luyện mô hình với các cấu hình khác nhau, tôi muốn tổng hợp và so sánh kết quả của các lần chạy trong cùng một nơi, để xác định mô hình và cấu hình phù hợp nhất                                                                                                                                                             |
| Actor                                     | ML Engineer, AI Researcher                                                                                                                                                                                                                                                                                                                                       |
| Thời điểm / bối cảnh                      | Sau khi thực hiện một nhóm experiment với các model, hyperparameters, dataset hoặc phương pháp huấn luyện khác nhau và cần đánh giá để chọn cấu hình tốt nhất                                                                                                                                                                                                    |
| Quy trình hiện tại (3–7 bước)             | 1. Tìm lại log và kết quả của các lần training · 2. Kiểm tra cấu hình tương ứng với từng experiment · 3. Trích xuất các metrics như Accuracy, Precision, Recall, F1-score, mAP hoặc mA · 4. Tổng hợp kết quả vào Excel/Google Sheets hoặc notebook · 5. Đối chiếu metrics và biểu đồ giữa các experiment · 6. Ghi nhận kết quả và lựa chọn cấu hình phù hợp nhất |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 2–4: Tìm cấu hình tương ứng, trích xuất metrics và đưa về cùng một bảng so sánh, mất khoảng 20–30 phút. Đặc biệt bất tiện khi log và checkpoint của các experiment được lưu ở nhiều thư mục hoặc định dạng khác nhau                                                                                                                                        |
| Impact (nếu không giải thì sao)           | Mất khoảng 30–60 phút cho mỗi lần tổng hợp kết quả. Khi số lượng experiment tăng, việc đối chiếu thủ công dễ nhầm lẫn cấu hình, bỏ sót kết quả và khó tái hiện lại experiment tốt nhất                                                                                                                                                                           |
| Success metric (baseline → target)        | Thời gian tổng hợp và so sánh kết quả: 30–60 phút/lần → dưới 15 phút/lần. Các experiment được lưu đầy đủ cấu hình và metrics, đảm bảo có thể truy xuất và tái hiện kết quả                                                                                                                                                                                       |
| Phương án không dùng AI                   | Sử dụng MLflow hoặc Weights & Biases để tracking experiment; chuẩn hóa cách đặt tên experiment, lưu hyperparameters, metrics và checkpoint; xây dựng dashboard để so sánh kết quả tự động                                                                                                                                                                        |
| Giả thuyết về AI (nếu có)                 | AI hỗ trợ đọc và tổng hợp log, tạo báo cáo so sánh giữa các experiment, phát hiện sự thay đổi bất thường của metrics và giải thích sự khác biệt giữa các cấu hình. Việc đánh giá và lựa chọn model cuối cùng vẫn dựa trên metrics và tiêu chí kỹ thuật                                                                                                           |
| Cảm nhận nhanh                            | Workflow                                                                                                                                                                                                                                                                                                                                                         |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — Khoảng 45 phút

[1 Tìm log và kết quả training: 5']
                  ↓
[2 Kiểm tra cấu hình từng experiment: 10']
                  ↓
[3 Trích xuất metrics: 10']
                  ↑
                  BOTTLENECK
                  ↓
[4 Tổng hợp vào Excel/Notebook: 10']
                  ↓
[5 Đối chiếu và so sánh kết quả: 5']
                  ↓
[6 Ghi nhận và lựa chọn cấu hình: 5']

```

### Problem Card #3

| Trường                                    | Nội dung                                                                                                                                                                                                                                                                                                             |
| ----------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Job Story                                 | Khi tìm hiểu một thư viện hoặc công nghệ mới phục vụ project, tôi muốn tìm được đúng tài liệu và ví dụ liên quan đến vấn đề đang gặp, để không phải đọc quá nhiều nội dung không cần thiết                                                                                                                           |
| Actor                                     | Software Developer, AI Engineer, sinh viên IT                                                                                                                                                                                                                                                                        |
| Thời điểm / bối cảnh                      | Khi sử dụng một thư viện/framework mới, gặp lỗi chưa biết cách xử lý, cần tìm hiểu một API hoặc muốn áp dụng một công nghệ vào project hiện tại                                                                                                                                                                      |
| Quy trình hiện tại (3–7 bước)             | 1. Xác định vấn đề hoặc nội dung kỹ thuật cần tìm hiểu · 2. Tìm kiếm trên Google, GitHub, Stack Overflow hoặc documentation chính thức · 3. Đọc và lọc các tài liệu, bài viết có liên quan · 4. Kiểm tra phiên bản thư viện và tính phù hợp của ví dụ · 5. Thử nghiệm code mẫu và điều chỉnh cho phù hợp với project |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3–5: Đọc, đối chiếu nhiều nguồn tài liệu và thử nghiệm các ví dụ để tìm ra cách áp dụng phù hợp, mất khoảng 45–60 phút. Một số hướng dẫn có thể đã lỗi thời                                                                                                                                                     |
| Impact (nếu không giải thì sao)           | Mất khoảng 1–2 giờ cho mỗi lần tìm hiểu. Developer bị gián đoạn công việc chính, dễ sử dụng tài liệu lỗi thời hoặc áp dụng sai cách triển khai, dẫn đến phát sinh lỗi và mất thêm thời gian sửa chữa                                                                                                                 |
| Success metric (baseline → target)        | Thời gian tìm kiếm và tìm hiểu tài liệu: 1–2 giờ/lần → dưới 30 phút/lần. Người dùng tìm được tài liệu chính thống, ví dụ phù hợp với phiên bản đang sử dụng và có thể áp dụng thành công vào project                                                                                                                 |
| Phương án không dùng AI                   | Xây dựng thư viện tài liệu nội bộ, bookmark các nguồn documentation đáng tin cậy, phân loại tài liệu theo công nghệ và phiên bản, tạo bộ ví dụ code mẫu cho những vấn đề thường gặp                                                                                                                                  |
| Giả thuyết về AI (nếu có)                 | AI hỗ trợ tìm kiếm ngữ nghĩa trên nhiều nguồn tài liệu, xác định nội dung phù hợp với vấn đề và phiên bản thư viện, tóm tắt phần cần đọc, đưa ra ví dụ code có dẫn nguồn để người dùng kiểm tra và áp dụng                                                                                                           |
| Cảm nhận nhanh                            | Workflow                                                                                                                                                                                                                                                                                                             |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — Khoảng 90 phút

[1 Xác định vấn đề cần tìm hiểu: 5']
                  ↓
[2 Tìm kiếm tài liệu và ví dụ: 15']
                  ↓
[3 Đọc và lọc các nguồn liên quan: 20']
                  ↑
                  BOTTLENECK
                  ↓
[4 Kiểm tra phiên bản và tính phù hợp: 15']
                  ↓
[5 Thử nghiệm, điều chỉnh code mẫu: 30']
                  ↑
                  BOTTLENECK
                  ↓
[6 Ghi chú kết quả: 5']

```

### Card muốn pitch nhất

- Card số: #1 — Tìm hiểu cấu trúc và luồng xử lý của project
- Vì sao: Đây là vấn đề mình muốn ưu tiên nhất vì có ảnh hưởng trực tiếp đến tốc độ làm việc của Software Developer và AI Engineer. Đây cũng là vấn đề mình từng gặp trong quá trình làm việc thực tế, nên có thể dễ dàng tiếp cận đúng nhóm người dùng để kiểm chứng và đánh giá giải pháp.
- Câu hỏi muốn nhóm phản biện: Liệu việc sử dụng AI để phân tích codebase, tự động tạo sơ đồ kiến trúc và giải thích luồng xử lý giúp developer tiết kiệm thời gian nhưng họ có thực sự hiểu project không?

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra                                                                            | Đồng ý? | Đã sửa gì                                                                                                                  |
| --------------------------------------------------------------------------------------------- | ------- | -------------------------------------------------------------------------------------------------------------------------- |
| Baseline ít nhất 120 phút chỉ dựa trên ước lượng, chưa có dữ liệu đo thời gian thực tế        | Đồng ý  | Giữ 120 phút là baseline giả định ban đầu, bổ sung kế hoạch bấm giờ trong những lần tiếp cận project tiếp theo để xác minh |
| AI có thể giải thích sai code, bỏ sót dependency hoặc không cập nhật khi source code thay đổi | Đồng ý  | Bổ sung yêu cầu AI phải dẫn chiếu đến file và vị trí code liên quan để developer kiểm tra lại thông tin                    |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động                  | Tôi đã làm gì?                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Kết quả / ảnh hưởng tới bài nhóm                                                                                                                                                                                                                                                                                                                                                                                                     |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Pitch Problem Card         | Pitch 3 candidate: (1) hỗ trợ developer hiểu cấu trúc và luồng xử lý của project (#7), (2) tổng hợp và so sánh kết quả các experiment ML (#8), (3) hỗ trợ thành viên mới onboarding và tìm hiểu project (#9). Trong đó, tôi chọn #7 làm card muốn pitch nhất vì đây là vấn đề đã gặp trong quá trình làm việc thực tế                                                                                                                                                                                      | Cả 3 candidate được đưa vào danh sách xem xét của nhóm. Candidate #7 được ưu tiên pitch sâu hơn vì ảnh hưởng trực tiếp đến tốc độ phát triển phần mềm, có đối tượng người dùng tương đối rõ và có tiềm năng ứng dụng AI để phân tích codebase                                                                                                                                                                                        |
| Phản biện bài của bạn khác | Với Hưng (#5): "Log hiện tại có lưu đủ trace và đoạn tài liệu truy xuất để tái hiện lỗi không?". Với Ly (#10): "Các tiêu chí nào được sử dụng để đảm bảo việc so sánh giữa các paper là khách quan?"                                                                                                                                                                                                                                                                                                       | Các câu hỏi giúp tránh lựa chọn problem chỉ dựa trên mô tả nhu cầu mà chưa xác định được điều kiện triển khai thực tế                                                                                                                                                                                                                                                                                                                |
| Nhận phản biện             | Hưng hỏi về #7: "Làm thế nào để xác định những module và file code thực sự liên quan đến feature cần implement mà không phải đọc toàn bộ project?". Ly hỏi về #8: "Nếu chuẩn hóa việc lưu metrics và sử dụng dashboard để so sánh thì đã giải quyết được vấn đề chưa, hay thực sự cần AI phân tích kết quả experiment?". Bảo hỏi về #9: "Làm thế nào để xác định thành viên mới đã hiểu đủ về project để tự làm việc? Có thể giải quyết bằng cách chuẩn hóa tài liệu onboarding thay vì sử dụng AI không?" | Bổ sung tiêu chí đầu ra cụ thể cho #7: xác định entry point, các module chính và luồng xử lý liên quan trực tiếp đến feature cần implement. Bổ sung phương án No AI cho cả 3 candidate: Architecture Diagram và README cho #7, MLflow/W&B cho #8, tài liệu onboarding chuẩn hóa cho #9. Đồng thời, xác định AI chỉ nên hỗ trợ phân tích và tìm kiếm code liên quan, cần có dẫn chiếu đến file và vị trí code để developer kiểm chứng |
| Gom cluster / cây OST      | Tham gia phân nhóm 12 candidate theo bản chất bottleneck. Các candidate của tôi nằm ở hai cụm: (1) tìm kiếm ngữ cảnh trong tri thức hoặc code phân tán (#7, #9); (2) tổng hợp thông tin từ nhiều nguồn hoặc nhiều lần chạy (#8)Qua đó, phân biệt nhu cầu thực tế của người dùng với giải pháp được đề xuất, ví dụ nhu cầu hiểu codebase khác với giải pháp tạo sơ đồ kiến trúc tự động                                                                                                                     | Giúp nhóm nhìn nhận các candidate theo những nhóm vấn đề có cùng bản chất thay vì chỉ phân loại theo đối tượng sử dụng hoặc công nghệ. Các candidate #7–#9 được đặt trong bối cảnh so sánh với những problem khác, từ đó làm rõ phạm vi và giá trị riêng của từng opportunity. Theo hướng OST của nhóm, outcome được tập trung vào việc giảm thời gian phân tích lỗi sau mỗi lần eval mà không bỏ sót nguyên nhân quan trọng         |
| Chọn candidate problem     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Kiểm chứng / research      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Quy trình nhóm             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Problem Statement          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Mức can thiệp AI           | Tham gia phân tích và so sánh 4 mức can thiệp No AI, Rule, Workflow và Agent cho candidate #4 (phân loại nguyên nhân các câu sai sau eval RAG). Đánh giá phần nào có thể xử lý bằng Rule, phần nào cần khả năng hiểu ngữ cảnh của AI và phần nào cần con người kiểm soát. Đồng thời, tham gia xác định AI chỉ nên gợi ý nhãn trong danh sách 8 nhãn cố định, trích dẫn bằng chứng từ trace và soạn nháp báo cáo; người chịu trách nhiệm duyệt nhãn, kiểm tra số liệu và gửi báo cáo                        | Nhóm thống nhất chọn Workflow thay vì Agent hoặc tự động hóa hoàn toàn. Quy trình kết hợp Rule để tính metrics, lọc câu sai và tổng hợp số liệu; AI hỗ trợ gán nhãn nguyên nhân và soạn nháp báo cáo; con người kiểm duyệt và quyết định cuối cùng. Nhóm cũng xác định các boundary, cơ chế Blind Review 10 câu/tuần và phương án fallback về Google Sheets + script nếu AI gán nhãn sai hoặc không đủ bằng chứng                    |
| Quyết định                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                      |

---

## 5. Dùng AI

| Checkpoint                     | Tôi dùng AI để làm gì?                                                                                                                                     | AI hữu ích ở đâu?                                                                                                                                                                                                    | AI sai hoặc hời hợt ở đâu?                                                                                                                                                                                                    | Tôi sửa gì bằng nhận định của mình?                                                                                                                                                                                                                                                         |
| ------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CP1 Scan                       | Nhờ AI ước lượng thời gian cho 5 scan problem, phân tích mức độ ảnh hưởng và gợi ý cách xác định dấu hiệu thực tế                                          | Giúp hình dung thời gian có thể mất cho từng vấn đề, phân biệt thời gian mỗi lần thực hiện với tần suất xảy ra và trình bày các candidate theo cùng một cấu trúc                                                     | Các con số thời gian chủ yếu là ước lượng dựa trên suy luận, chưa có dữ liệu phỏng vấn hoặc bấm giờ thực tế. AI chưa biết chính xác quy mô project và hoàn cảnh làm việc của từng actor                                       | Giữ các con số dưới dạng baseline giả định, lựa chọn Top 3 dựa trên trải nghiệm và mức độ liên quan đến công việc thực tế của Software Developer/AI Engineer                                                                                                                                |
| CP2 Problem Card               | Nhờ AI xây dựng Top 3 problem cards và chi tiết hóa từng card: quy trình hiện tại, bottleneck, impact, success metric, phương án No AI và giả thuyết về AI | AI giúp phân rã một Job Story thành các bước cụ thể, xác định những điểm có thể gây mất thời gian và đề xuất các hướng giải quyết khác nhau để so sánh                                                               | AI có xu hướng tự giả định các bước trong quy trình, thời gian của từng bước và target sau cải tiến. Một số bottleneck chưa chắc phản ánh đúng trải nghiệm thực tế của người dùng                                             | Điều chỉnh nội dung theo đặc thù công việc thực tế; giữ thời gian tổng là ước lượng ban đầu thay vì khẳng định là số liệu đo được. Bổ sung phương án No AI và yêu cầu AI phải dẫn chiếu đến file/vị trí code khi hỗ trợ tìm hiểu project                                                    |
| CP4 Research                   |                                                                                                                                                            |                                                                                                                                                                                                                      |                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                             |
| CP5 Quy trình                  |                                                                                                                                                            |                                                                                                                                                                                                                      |                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                             |
| CP5–6 Problem Statement        |                                                                                                                                                            |                                                                                                                                                                                                                      |                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                             |
| CP6 Mức can thiệp / quyết định | Nhờ AI phân tích ma trận độ mơ hồ × độ phức tạp, so sánh No AI, Rule, Workflow, Agent; xây dựng AI Canvas và trả lời hai câu hỏi của Google PAIR           | Giúp nhìn rõ phần nào nên dùng Rule, phần nào cần khả năng hiểu ngữ cảnh của LLM và phần nào cần giữ con người kiểm soát. AI cũng hỗ trợ xác định các rủi ro như gán nhãn sai, bịa bằng chứng và tự động gửi báo cáo | AI có thể mặc định Agent là hướng phát triển cao hơn và đề xuất tự động hóa quá mức. Việc xếp bài toán vào ma trận và xác định báo nhầm hay bỏ sót nguy hiểm hơn cũng cần dựa trên bối cảnh cụ thể, không thể áp dụng máy móc | Thống nhất lựa chọn Workflow: Rule tính metrics và tổng hợp số liệu, AI gợi ý nhãn và soạn nháp báo cáo, người duyệt và quyết định cuối cùng. Bổ sung 8 nhãn cố định, yêu cầu trích dẫn bằng chứng, nhãn "Không chắc", Blind Review 10 câu/tuần và cơ chế fallback khi AI không đạt yêu cầu |

Qua các checkpoint, tôi nhận thấy AI hữu ích nhất khi hỗ trợ cấu trúc hóa vấn đề, phân rã quy trình, so sánh các phương án và rà soát tính logic của bài toán. Tuy nhiên, AI thường đưa ra các giả định hợp lý về mặt lý thuyết nhưng chưa chắc đúng với bối cảnh thực tế, đặc biệt là thời gian thực hiện, bottleneck và hiệu quả kỳ vọng của giải pháp. Vì vậy, tôi không sử dụng kết quả AI như kết luận cuối cùng mà đối chiếu với trải nghiệm thực tế, dữ liệu của nhóm và các phản biện từ thành viên khác. Điều tôi rút ra là AI nên giúp con người suy nghĩ và ra quyết định tốt hơn, chứ không thay thế việc hiểu đúng problem và kiểm chứng bằng chứng.

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

Khi nghe các candidate của những thành viên khác, tôi nhận ra cùng là những vấn đề liên quan đến AI nhưng bottleneck của mỗi người dùng có thể rất khác nhau. Ví dụ, candidate của Bảo về text-to-SQL không chỉ đơn giản là nhu cầu truy vấn database bằng ngôn ngữ tự nhiên, mà vấn đề thực sự nằm ở thời gian chờ analyst xử lý yêu cầu. Candidate của Hưng về error analysis RAG lại tập trung vào việc phải đọc và gán nhãn thủ công các câu trả lời sai để xác định nguyên nhân. Trong khi đó, các candidate của Ly liên quan nhiều hơn đến việc tổng hợp, đối chiếu thông tin từ các paper và tìm research gap.

Điều tôi học được là không nên chỉ nhìn vào công nghệ hoặc giải pháp được đề xuất mà cần tìm hiểu công việc thực tế phía sau. Một vấn đề nghe có vẻ phù hợp với AI chưa chắc cần AI để giải quyết.

Tôi cũng nhận ra tầm quan trọng của việc đưa ra bằng chứng cho problem. Một candidate có mô tả khá thuyết phục nhưng nếu không xác định được thời gian mất đi, tần suất xảy ra và ảnh hưởng đến công việc thì sẽ khó so sánh với những candidate khác.

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

Tôi nghĩ nhóm có lúc rơi vào solution-first, đặc biệt khi các thành viên trình bày candidate ban đầu. Tôi cũng gặp tình trạng này khi đề xuất bài toán tìm hiểu cấu trúc project. Khi nghĩ đến vấn đề phải đọc nhiều file code và lần theo luồng xử lý, tôi nhanh chóng liên tưởng đến việc sử dụng AI để phân tích codebase, tạo sơ đồ kiến trúc và giải thích mối liên hệ giữa các module. Tuy nhiên, đó mới là một hướng giải pháp, chưa chứng minh được AI là cần thiết.

Các phản biện từ Hưng và Bảo giúp tôi nhìn lại vấn đề. Với candidate tìm hiểu project, cần xác định chính xác developer đang gặp khó khăn ở việc tìm file liên quan, hiểu dependency hay hiểu logic nghiệp vụ. Với candidate onboarding, việc chuẩn hóa README và tài liệu hướng dẫn có thể đã giải quyết được phần lớn nhu cầu mà không cần AI.

Trong quá trình gom cluster và xây dựng OST, nhóm cũng nhận ra một số ý tưởng đang mô tả solution thay vì opportunity, chẳng hạn dashboard tự động phân loại lỗi hay agent tự sửa prompt. Nhóm đã loại các ý tưởng này khỏi nhánh opportunity và tập trung mô tả nhu cầu, pain thực sự của người dùng.

Qua đó, tôi hiểu rằng cần xác định rõ người dùng đang gặp vấn đề gì và tại sao vấn đề đó tồn tại trước khi quyết định sử dụng công nghệ nào để giải quyết.

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

Có. Một ví dụ cụ thể là candidate #2 của tôi về việc tổng hợp và so sánh kết quả các thí nghiệm huấn luyện mô hình. Ban đầu, tôi cho rằng đây là một vấn đề phù hợp để ứng dụng AI vì khi thực hiện nhiều experiment, tôi thường phải tìm log, cấu hình, metrics và checkpoint ở nhiều nơi rồi tổng hợp chúng để so sánh.

Tuy nhiên, Ly đặt câu hỏi: "Nếu chuẩn hóa việc lưu metrics và sử dụng dashboard để so sánh thì đã giải quyết được vấn đề chưa, hay thực sự cần AI phân tích kết quả experiment?". Câu hỏi này khiến tôi nhận ra mình đang gộp hai nhu cầu khác nhau thành một: nhu cầu quản lý và so sánh kết quả experiment, và nhu cầu phân tích để tìm ra nguyên nhân vì sao một cấu hình tốt hơn cấu hình khác.

Nhu cầu đầu tiên hoàn toàn có thể giải quyết bằng các công cụ experiment tracking như MLflow hoặc Weights & Biases, kết hợp với quy ước lưu trữ thống nhất. AI chỉ thực sự cần thiết khi người dùng muốn hỗ trợ giải thích sự khác biệt giữa các lần chạy hoặc tìm ra những yếu tố ảnh hưởng đến kết quả.

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

Điều đáng chú ý nhất trong phần research là nhóm nhận ra các công cụ hiện có đã giải quyết được khá nhiều thành phần của quy trình error analysis RAG. Ví dụ, Ragas hỗ trợ tính các metrics đánh giá RAG, Langfuse hỗ trợ annotation và quản lý trace, còn LangSmith Insights Agent có thể hỗ trợ khám phá các nhóm lỗi. Điều này khiến tôi nhận ra rằng không nhất thiết phải xây dựng một hệ thống AI hoàn chỉnh từ đầu, vì nhiều thành phần đã có giải pháp phù hợp.

Một điểm đáng chú ý khác là việc sử dụng LLM để gán nhãn không có nghĩa kết quả luôn chính xác. Trong thí nghiệm minh họa của report, tỷ lệ trùng nhãn ban đầu là 72,5%, sau khi bổ sung định nghĩa và ví dụ cho từng nhãn tăng lên 85%, nhưng vẫn còn 15% trường hợp không trùng khớp.

Tuy nhiên, tôi cũng nhận thấy cần phân biệt kết quả minh họa với bằng chứng thực tế. Các dữ liệu phỏng vấn, poll và thí nghiệm trong report hiện được ghi rõ là dữ liệu hư cấu để minh họa, nên chưa thể dùng chúng để khẳng định giả thuyết đã được kiểm chứng ngoài thực tế. Nếu thực hiện tiếp, nhóm cần thay thế bằng dữ liệu phỏng vấn và thí nghiệm thực tế.

Bài học tôi rút ra là research không chỉ để tìm công cụ có thể sử dụng mà còn để xác định phần nào đã được giải quyết tốt và phần nào thực sự còn khoảng trống.

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

Theo tôi, khó nhất là chuyển từ một mô tả vấn đề tương đối rộng thành một Problem Statement có phạm vi đủ rõ, có thể kiểm chứng và đo lường được.

Ban đầu, candidate #4 (trong report nhóm) được mô tả là nhu cầu tìm hiểu nguyên nhân các câu trả lời sai sau mỗi lần eval RAG. Tuy nhiên, để viết Problem Statement, nhóm phải xác định cụ thể ai là người gặp vấn đề, họ thực hiện quy trình nào, bước nào thực sự tốn thời gian và hậu quả nếu không giải quyết được vấn đề.

Một khó khăn khác là lựa chọn success metric. Nếu chỉ đo thời gian giảm từ 130 phút xuống dưới 60 phút thì chưa đủ để chứng minh giải pháp tốt hơn. AI có thể gán nhãn nhanh nhưng nếu nhãn sai, team sẽ ưu tiên sửa nhầm nguyên nhân. Vì vậy, nhóm phải bổ sung tiêu chí tỷ lệ nhãn AI gợi ý trùng với nhãn cuối của Khoa tối thiểu 80%, đồng thời kiểm soát số câu hỏi lại từ Tech Lead và PM.

Tôi cũng nhận thấy việc viết boundary rất quan trọng. Nhóm cần xác định rõ AI được phép làm gì và không được phép làm gì, chẳng hạn chỉ gợi ý nhãn trong danh sách cố định, phải trích dẫn bằng chứng và không tự sửa prompt hoặc gửi báo cáo.

Qua phần này, tôi hiểu rằng Problem Statement không đơn thuần là tóm tắt một ý tưởng mà phải mô tả được một vấn đề thực tế với actor, quy trình, impact và tiêu chí thành công rõ ràng.

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

Tôi hiểu mục đích của buổi lab là học cách nhận diện bài toán từ các vấn đề thực tiễn và đánh giá mức độ của bài toán. Tuy nhiên, đầu buổi lab tôi vẫn chưa follow up được 100% nội dung worksheet.

Nếu làm lại từ đầu, tôi sẽ dành nhiều thời gian hơn để thu thập bằng chứng trước khi lựa chọn Top 3 candidate. Với những vấn đề như hiểu cấu trúc project hoặc tổng hợp experiment, tôi sẽ ghi nhận thời gian thực tế qua một số lần thực hiện, thay vì chủ yếu dựa trên ước lượng. Tôi cũng sẽ phỏng vấn thêm những Software Developer và AI Engineer khác để xác định vấn đề có phổ biến hay chỉ xuất phát từ trải nghiệm cá nhân.

Đối với candidate cuối cùng của nhóm, nếu có cơ hội làm lại, tôi sẽ phản biện mạnh hơn về tính ổn định của danh sách nhãn nguyên nhân qua nhiều tuần và khả năng thống nhất giữa những người cùng thực hiện gán nhãn. Đây là giả định quan trọng vì nếu taxonomy thay đổi liên tục hoặc các kỹ sư không thống nhất về định nghĩa nhãn thì AI khó duy trì chất lượng phân loại.

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi _problem → quy trình → metric → boundary → mức can thiệp AI → quyết định_ của bài nhóm mình.

- Bài toán của nhóm là hỗ trợ AI Engineer xác định nguyên nhân các câu trả lời sai sau mỗi lần đánh giá hệ thống RAG hằng tuần, thay vì chỉ nhìn vào các metric tổng.
- Quy trình hiện tại gồm chạy evaluation, tính metrics, lọc câu sai, đọc và gán nhãn nguyên nhân, tổng hợp kết quả rồi viết báo cáo, trong đó bước đọc và gán nhãn khoảng 60 câu sai mất 60 phút là bottleneck chính. Nhóm đặt mục tiêu giảm tổng thời gian từ 130 phút xuống dưới 60 phút mỗi tuần, đồng thời yêu cầu tỷ lệ nhãn AI gợi ý trùng với nhãn cuối của Khoa đạt ít nhất 80%.
- Về boundary, AI chỉ được sử dụng dữ liệu đầu vào đã cung cấp, gợi ý nhãn trong danh sách 8 nhãn cố định và phải trích dẫn bằng chứng từ trace, không được tự tính metrics, sửa prompt hoặc gửi báo cáo.
- Nhóm chọn mức can thiệp Workflow: Rule đảm nhiệm tính metrics và tổng hợp số liệu, AI gợi ý nhãn nguyên nhân và soạn nháp báo cáo, còn Khoa kiểm duyệt và quyết định cuối cùng. Nhóm lựa chọn Workflow vì cách tiếp cận này cân bằng giữa khả năng xử lý ngữ cảnh của AI và khả năng kiểm soát của con người, đồng thời có thể quay về Google Sheets và script thủ công khi AI không đạt yêu cầu.

---

## 7. Tài liệu tham khảo

-
