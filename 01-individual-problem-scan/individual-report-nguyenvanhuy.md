# 01 — Individual Problem Scan

> Điền theo Phase 1 + Phase 2 trong `01-worksheet.md`. Tự scan trước, dùng AI sau để phản biện. Không copy ví dụ Weekly Report.

## Thông tin cá nhân

- Họ và tên: Nguyễn Văn Huy
- Mã học viên: 2A202602428
- Vai trò / bối cảnh: Sinh viên năm cuối ngành công nghệ thông tin Trường Đại học Bách khoa - Đại học Đà Nẵng/ Software Engineer 
- Công việc hằng tuần (3-5 gạch đầu dòng để soi problem):

---

## Phase 1 — Scan rộng

Scan 8 problems trong công việc, vượt mức tối thiểu 5.

> Các vấn đề và dấu hiệu dưới đây được tổng hợp từ case study công khai, không phải số đo hay trải nghiệm trực tiếp của học viên. Link nguồn đặt tại từng dòng; ngày tra cứu: 12/09/2026.

| # | Lăng kính | Problem quan sát được | Ai chịu ảnh hưởng? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Tốn thời gian | Chạy thủ công bộ kiểm thử hồi quy mất nhiều thời gian, làm chậm việc kiểm tra sản phẩm | Nhóm QA tại SafelyYou | Khoảng 362 test case; chạy thủ công một bộ regression mất 1 tuần. [Nguồn](https://testrigor.com/case-study-safelyyou/) |
| 2 | AI có thể tốt hơn | Nhân viên hỗ trợ phải tìm và đối chiếu tài liệu ở nhiều nơi trước khi trả lời ticket kỹ thuật | Nhân viên hỗ trợ kỹ thuật tại ClickUp | Khoảng 15 phút tra cứu/ticket, với khoảng 5.000 ticket/tháng. [Nguồn](https://zapier.com/customer-stories/clickup) |
| 3 | Tốn thời gian | Khó tìm hóa đơn tương ứng với khoản tiền khách hàng thanh toán để đối chiếu và xử lý trong SAP | Nhân viên kế toán khoản phải thu tại EY | Các khoản cần xử lý thủ công mất 7–30 phút tra cứu/khoản, thêm 4–25 phút xử lý trong SAP/khoản. [Nguồn](https://learn.microsoft.com/en-us/power-platform/guidance/case-studies/global-finance) |
| 4 | Lặp lại | Nhập và viết tóm tắt thông tin từng ứng viên bằng tay | Nhân viên tuyển dụng tại JBGoodwin REALTORS | Viết tóm tắt mất 5–10 phút/người; nhập dữ liệu thủ công chiếm tới 25% thời gian của recruiter. [Nguồn](https://zapier.com/customer-stories/JBGoodwin-REALTORS) |
| 5 | Lặp lại | Đọc và kiểm tra thủ công từng hóa đơn đính kèm để đối chiếu với đơn mua hàng | Nhân viên kế toán phải trả tại CATRION | Kiểm tra mỗi hóa đơn đính kèm mất ít nhất 3 phút. [Nguồn](https://www.microsoft.com/en/customers/story/24577-catrion-microsoft-power-platform) |
| 6 | Pain từ người khác | Dữ liệu nhân viên mới phải cập nhật lại ở nhiều bảng, gây sai lệch thông tin lương và onboarding | Kathy Lam, phụ trách vận hành tuyển dụng tại StackAdapt, và 5 nhóm nhận dữ liệu | Mỗi nhân viên mới cần hàng chục cập nhật thủ công; dữ liệu phân tán qua Finance, People Ops, Comp, Payroll và FP&A. [Nguồn](https://zapier.com/blog/stackadapt-automates-hiring-with-zapier/) |
| 7 | Pain từ người khác | Quản lý cửa hàng mất công lập và chỉnh lịch ca bằng Excel, dễ hỏng công thức khi thay đổi | Quản lý cửa hàng tại Mud Bay | Trung bình 2–3 giờ/quản lý để soạn và công bố lịch; tổng 120–180 giờ ở 60 địa điểm. [Nguồn](https://www.deputy.com/customers/mud-bay) |
| 8 | Lặp lại | Đối soát nhiều tài khoản ngân hàng và xử lý các tác vụ ngân quỹ hằng tuần tốn thời gian | Nhân sự cấp cao phụ trách ngân quỹ tại L&M Fleet Supply | Các tác vụ ngân quỹ hằng tuần chiếm tới một ngày làm việc; bối cảnh có 25 tài khoản ngân hàng cần đối soát. [Nguồn](https://www.microsoft.com/en/customers/story/25084-l-and-m-fleet-supply-dynamics-365-commerce) |

---

## Phase 2 — Top 3 Problem Cards

> Các card dựa trên nguồn công khai của Phase 1. Actor, workflow chi tiết và bottleneck được diễn giải để làm bài; cần xác minh với người dùng. Success metric và future workflow là **đề xuất chưa thử nghiệm**, không phải kết quả đã đạt. Số đo của doanh nghiệp không phải số đo của học viên.

### 2.1. Chọn top 3

| Rank | Problem (từ bảng scan) | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | #2 — Tra cứu ngữ cảnh ticket kỹ thuật | Actor rõ; có thời gian tra cứu/ticket; gần bối cảnh phần mềm và có thể thu hẹp vào một bộ tài liệu | Có tiếp cận được ticket/tài liệu không? Người nào kiểm tra độ đúng? Tìm kiếm từ khóa đã đủ chưa? |
| 2 | #1 — Chạy kiểm thử hồi quy thủ công | Gần bối cảnh Software Engineer; có bộ test và kết quả mong đợi để đánh giá; so sánh được Rule với AI | Thời gian chủ yếu ở chạy test hay bảo trì? Có ứng dụng demo và dữ liệu chạy lại được không? |
| 3 | #5 — Kiểm tra hóa đơn đính kèm | Actor và đơn vị đo rõ; dễ giới hạn vào một định dạng; tách được đọc dữ liệu, rule và người duyệt | Ai xác định quy tắc nghiệp vụ? Dữ liệu mẫu có đủ ngoại lệ? Công kiểm tra lại có làm mất lợi ích không? |

### 2.2. Problem Cards chi tiết

#### Problem Card #1 — Tra cứu ngữ cảnh trước khi trả lời ticket kỹ thuật

**Problem 1 câu:**  
Nhân viên hỗ trợ kỹ thuật phải tìm và đối chiếu thông tin ở nhiều nguồn trước khi trả lời khách hàng; case ClickUp ghi nhận khoảng 15 phút tra cứu cho mỗi ticket.

**Actor:**  
Nhân viên technical support chịu trách nhiệm tìm đúng hướng dẫn và chuẩn bị phản hồi; khách hàng chờ câu trả lời, chuyên gia kỹ thuật tiếp nhận trường hợp khó.

**Thời điểm / bối cảnh:**  
Khi tiếp nhận ticket mới hoặc cần bổ sung ngữ cảnh. Nguồn ghi khoảng 5.000 ticket/tháng, không xác nhận một buổi xử lý cố định mỗi tuần.

**Current workflow (bản nháp):**

```text
1. Đọc mô tả và xác định sản phẩm, phiên bản, triệu chứng.
2. Lấy lịch sử trao đổi liên quan trong hệ thống hỗ trợ.
3. Tìm tài liệu hướng dẫn và đối chiếu với tình huống của ticket.
4. Ghi lại ngữ cảnh, bằng chứng và bước xử lý phù hợp.
5. Kiểm tra thông tin để sẵn sàng soạn phản hồi.
```

**Bottleneck:**  
Bước 3 — tìm và đối chiếu tài liệu phù hợp. Đây là giả thuyết về bước nghẽn cần kiểm chứng; số 15 phút của nguồn là cả phần tra cứu, không phải riêng bước 3.

**Impact:**  
Công tra cứu lặp lại ở mỗi ticket làm giảm thời gian dành cho xử lý chuyên sâu. Với quy mô hàng nghìn ticket/tháng của case, việc lặp lại này đáng xem xét; chưa có số đo riêng tại nhóm học viên.

**Success metric:**  
Mục tiêu đề xuất: giảm ít nhất 30% thời gian từ mở ticket đến có ngữ cảnh đã kiểm tra, trên cùng bộ 20 ticket thử nghiệm. Đo baseline của bộ thử trước; nếu baseline thực đo là 15 phút thì mục tiêu tương ứng là không quá 10,5 phút. Mỗi gợi ý phải có nguồn truy xuất được; ghi thêm số dẫn chứng sai và thời gian sửa. Không lấy kết quả của doanh nghiệp làm kết quả của nhóm.

**Non-AI alternative:**  
Chuẩn hóa kho tài liệu, gắn nhãn theo sản phẩm/phiên bản, tìm kiếm từ khóa và dùng checklist tra cứu. Cần thử cách này để biết liệu vấn đề chỉ do tài liệu tổ chức kém.

**AI hypothesis:**  
AI đọc ticket, tìm trong bộ tài liệu được phép và tạo bản tóm tắt kèm dẫn chứng; nhân viên kiểm tra trước khi dùng. Không tự gửi phản hồi hoặc thao tác trên tài khoản khách hàng.

**Quick gut:**  
Workflow — các bước truy xuất, tổng hợp và kiểm tra đã rõ; chưa có bằng chứng cần Agent tự lập kế hoạch.

**Nguồn số liệu:** [Zapier — ClickUp](https://zapier.com/customer-stories/clickup). Tương ứng vấn đề #2 trong Phase 1; xem thêm [ghi chú nghiên cứu](01-individual-problem-scan-research-notes.md).

##### Draft current workflow

```text
CURRENT STATE — khoảng 15 phút/ticket cho phần tra cứu (nguồn ClickUp)

[Đọc ticket]
→ [Lấy lịch sử]
→ [Tìm + đối chiếu tài liệu]  <-- bottleneck dự kiến
→ [Ghi ngữ cảnh và hướng xử lý]
→ [Nhân viên kiểm tra]

Nguồn không tách thời gian từng bước.
```

##### Draft future workflow

```text
FUTURE STATE — mục tiêu pilot: không quá 70% baseline thực đo

[Nhận ticket và kiểm tra phạm vi — Rule]
→ [Truy xuất bộ tài liệu được phép — hệ thống]
→ [Tóm tắt ngữ cảnh + dẫn chứng — AI]
→ [Nhân viên kiểm tra/sửa — human boundary]
→ [Bàn giao ngữ cảnh đã duyệt để soạn phản hồi]

Fallback: thiếu nguồn, nguồn mâu thuẫn hoặc gợi ý sai
→ nhân viên tra cứu thủ công; không tự gửi câu trả lời.

Đo cả thời gian chờ, kiểm tra và sửa; chưa có kết quả pilot.
```

---

#### Problem Card #2 — Chạy kiểm thử hồi quy thủ công

**Problem 1 câu:**  
QA phải thực hiện lại nhiều test case để xác nhận chức năng cũ sau thay đổi; case SafelyYou có khoảng 362 test case và mất một tuần để chạy một bộ regression thủ công.

**Actor:**  
QA phụ trách kiểm tra bản build; developer nhận và sửa lỗi; người phụ trách release quyết định phát hành.

**Thời điểm / bối cảnh:**  
Trước khi xác nhận bản phát hành hoặc sau thay đổi cần chạy lại bộ regression. Nguồn đề cập nhịp regression hằng tuần sau tự động hóa, không khẳng định thời gian chạy thủ công một tuần là lịch release hằng tuần.

**Current workflow (bản nháp):**

```text
1. Nhận bản build và danh sách thay đổi.
2. Chọn bộ test cùng kết quả mong đợi.
3. Chuẩn bị môi trường và dữ liệu test.
4. Thực hiện từng test case, lưu kết quả thực tế.
5. Xác minh ca thất bại và ghi lỗi cho developer.
6. Chạy lại ca liên quan sau sửa, bàn giao kết quả kiểm thử.
```

**Bottleneck:**  
Bước 4 — thao tác lặp lại để thực thi từng ca. Cần phân biệt với công chuẩn bị, phân tích lỗi và bảo trì script; nguồn nêu bảo trì Selenium cũng gây khó khăn, nhưng không tách thời gian từng việc.

**Impact:**  
Một lượt regression kéo dài làm chậm phản hồi về chất lượng bản build. Nếu thiếu thời gian, nhóm có thể khó kiểm tra đủ bộ ca đã xác định. Chưa quy đổi một tuần thành giờ công vì nguồn không nêu số người hay số giờ làm.

**Success metric:**  
Mục tiêu đề xuất: giảm ít nhất 30% tổng giờ công QA khi chạy cùng 10–20 test case trên ứng dụng demo, phát hiện đầy đủ lỗi đã cài sẵn và không tự thay đổi tiêu chí pass. Đo riêng thời gian máy chạy, công kiểm tra lỗi và công bảo trì. Baseline của bộ pilot phải đo mới; không áp một tuần của 362 ca cho 10–20 ca.

**Non-AI alternative:**  
Chuẩn hóa checklist và dữ liệu, ưu tiên regression theo rủi ro; viết script với assertion cố định cho luồng ổn định. Đây là phương án cần đánh giá trước khi dùng AI.

**AI hypothesis:**  
AI hỗ trợ bản nháp test hoặc phân tích log, nhưng QA kiểm tra kết quả mong đợi và bằng chứng lỗi. Không cho AI sửa assertion để làm test pass hoặc tự phê duyệt release.

**Quick gut:**  
Rule — ưu tiên script/assertion rõ cho phạm vi nhỏ và ổn định. Workflow điều phối có thể bổ sung; chưa cần Agent khám phá tự do.

**Nguồn số liệu:** [testRigor — SafelyYou](https://testrigor.com/case-study-safelyyou/). Tương ứng vấn đề #1 trong Phase 1; xem thêm [ghi chú nghiên cứu](01-individual-problem-scan-research-notes.md).

##### Draft current workflow

```text
CURRENT STATE — một tuần/bộ regression trong case SafelyYou

[Nhận build]
→ [Chọn test + expected result]
→ [Chuẩn bị môi trường/dữ liệu]
→ [QA thực thi từng ca]  <-- bottleneck dự kiến
→ [Xác minh và ghi lỗi]
→ [Kiểm tra lại + bàn giao]

Khoảng 362 test case trong nguồn; chưa có giờ công từng bước.
```

##### Draft future workflow

```text
FUTURE STATE — mục tiêu pilot: giảm ít nhất 30% giờ công QA

[QA duyệt test + expected result]
→ [Chuẩn bị môi trường demo — script]
→ [Chạy test với assertion cố định — Rule]
→ [Tập hợp log và kết quả — hệ thống]
→ [QA xác minh lỗi — human boundary]
→ [Bàn giao để người phụ trách quyết định release]

Fallback: test không ổn định hoặc kết quả không rõ
→ QA chạy lại thủ công; không tự bỏ qua lỗi.

Pilot chỉ 10–20 ca; đo baseline riêng, chưa có thời gian sau thực đo.
```

---

#### Problem Card #3 — Kiểm tra hóa đơn đính kèm với đơn mua hàng

**Problem 1 câu:**  
Nhân viên kế toán phải đọc hóa đơn và đối chiếu với đơn mua hàng bằng tay; case CATRION ghi nhận ít nhất 3 phút kiểm tra mỗi hóa đơn đính kèm.

**Actor:**  
Nhân viên kế toán phải trả kiểm tra chứng từ; người mua hàng giải thích chênh lệch; người có thẩm quyền duyệt thanh toán.

**Thời điểm / bối cảnh:**  
Mỗi khi nhận hóa đơn PDF hoặc ảnh scan cần xác minh trước khi chuyển xử lý. Nguồn chưa nêu khối lượng hóa đơn hoặc lịch gom xử lý hằng tuần.

**Current workflow (bản nháp):**

```text
1. Nhận hóa đơn và kiểm tra đủ trang, khả năng đọc.
2. Đọc các trường cần đối chiếu trên hóa đơn.
3. Tìm đơn mua hàng tương ứng.
4. So mã hàng, số lượng, số tiền và các trường theo quy tắc đã thống nhất.
5. Ghi điểm lệch hoặc thông tin chưa rõ.
6. Chuyển kết quả cho người kiểm tra/duyệt tiếp.
```

**Bottleneck:**  
Bước 4 — đối chiếu dữ liệu giữa chứng từ là điểm nghẽn dự kiến; đọc dữ liệu ở bước 2 cũng có thể tốn công. Cần đo để phân biệt hai phần. Ít nhất 3 phút là thời gian kiểm tra hóa đơn theo nguồn, không phải số đo riêng bước 4.

**Impact:**  
Công kiểm tra lặp lại theo số chứng từ; sai sót có thể dẫn đến phải kiểm tra và bổ sung lại. Chưa có đủ dữ liệu để tính tổng giờ mỗi tuần hoặc tỷ lệ sai trong bối cảnh học viên.

**Success metric:**  
Mục tiêu đề xuất: giảm ít nhất 30% tổng thời gian kiểm tra trên 10–20 cặp hóa đơn/đơn mua giả lập cùng định dạng, phát hiện đầy đủ sai lệch đã cài sẵn. Đo baseline mới; nếu thực đo là 3 phút thì mục tiêu tương ứng không quá 2,1 phút, gồm công người kiểm tra và sửa. Theo dõi lỗi trích trường, lỗi đối chiếu và ngoại lệ riêng.

**Non-AI alternative:**  
Yêu cầu mẫu hóa đơn thống nhất, dùng dữ liệu có cấu trúc và công thức kiểm tra mã đơn/số tiền/bản trùng. Nếu nhận được dữ liệu chuẩn, có thể không cần AI đọc chứng từ.

**AI hypothesis:**  
AI/OCR trích dữ liệu từ PDF hoặc ảnh; rule đối chiếu với đơn mua; kế toán xem dữ liệu gốc và duyệt điểm lệch. Không tự sửa chứng từ hoặc phê duyệt thanh toán.

**Quick gut:**  
Workflow — chuỗi đọc dữ liệu, kiểm tra theo luật và người duyệt khá rõ; chưa cần Agent tự chọn hành động.

**Nguồn số liệu:** [Microsoft — CATRION](https://www.microsoft.com/en/customers/story/24577-catrion-microsoft-power-platform). Tương ứng vấn đề #5 trong Phase 1; xem thêm [ghi chú nghiên cứu](01-individual-problem-scan-research-notes.md).

##### Draft current workflow

```text
CURRENT STATE — ít nhất 3 phút/hóa đơn đính kèm (nguồn CATRION)

[Nhận chứng từ]
→ [Đọc các trường]
→ [Tìm đơn mua]
→ [Đối chiếu dữ liệu]  <-- bottleneck dự kiến
→ [Ghi điểm lệch]
→ [Chuyển kiểm tra/duyệt]

Không có thời gian từng bước; cần kiểm chứng bước nghẽn.
```

##### Draft future workflow

```text
FUTURE STATE — mục tiêu pilot: không quá 70% baseline thực đo

[Nhận hóa đơn + đơn mua]
→ [Trích trường kèm vị trí trên chứng từ — AI/OCR]
→ [Kiểm tra + đối chiếu — Rule]
→ [Kế toán xem dữ liệu gốc và sửa — human boundary]
→ [Xuất bảng kết quả kiểm tra]

Fallback: ảnh mờ, thiếu trang hoặc dữ liệu mâu thuẫn
→ giữ trạng thái chưa xác minh và chuyển kiểm tra thủ công.
Không tự duyệt hoặc thực hiện thanh toán; chưa có kết quả pilot.
```

---

### 2.3. Card muốn pitch nhất (chuẩn bị 2 phút)

**Card đề xuất để pitch:**  
Card #1 — Tra cứu ngữ cảnh trước khi trả lời ticket kỹ thuật.

**Vì sao (gợi ý để học viên xem lại):**  
Vấn đề có actor cụ thể và số đo thời gian tra cứu theo ticket. Phạm vi có thể thu hẹp vào việc chuẩn bị ngữ cảnh từ một bộ tài liệu, với nhân viên kiểm tra trước khi phản hồi. Cách làm này cho phép so sánh tìm kiếm từ khóa với Workflow có AI mà chưa cần tự động giải quyết toàn bộ ticket.

**Câu hỏi đề xuất để nhóm challenge:**

1. Nếu chuẩn hóa kho tài liệu và tìm theo từ khóa đã đủ, AI còn giảm được phần công nào?
2. Nhóm lấy bộ ticket và đáp án tham chiếu ở đâu để đo cả tốc độ lẫn độ đúng, tránh chỉ tạo ra bản tóm tắt nghe hợp lý?

> Đây là lựa chọn và câu hỏi do AI đề xuất theo yêu cầu soạn bài, chưa phải lời trình bày hoặc ý kiến đã được học viên xác nhận. Khi pitch, học viên tự diễn đạt theo hiểu biết của mình.

**AI phản biện Card:**
- Điểm yếu đã chỉ ra: dễ nhầm thời gian cả tác vụ với thời gian một bước; chưa có baseline pilot, người xác minh và quyền dùng dữ liệu; có thể chọn AI trước khi thử cách đơn giản.
- Nội dung đã chỉnh trong bản nháp: ghi bottleneck là giả thuyết; giữ nguyên đơn vị/phạm vi nguồn; dùng mục tiêu có điều kiện dựa trên baseline đo mới; thêm non-AI alternative, điểm người kiểm tra và fallback.
- Phần học viên cần xác nhận: top 3, card muốn pitch và mức độ hiểu/tiếp cận người dùng của từng vấn đề.

### Self-check nộp phần 01

- [x] Phase 1 có 8 vấn đề, đúng 5 cột của bảng mẫu, mỗi dòng có actor và bằng chứng kèm nguồn.
- [x] Phase 1 chỉ mô tả vấn đề/hiện trạng, không đưa kết quả cải tiến hoặc phương án triển khai.
- [x] Top 3 truy ngược được về các dòng #2, #1, #5 trong Phase 1.
- [x] Cả 3 card đủ field; current workflow có 3–7 bước.
- [x] Mỗi card có workflow trước/sau, bottleneck, metric, non-AI alternative, human boundary và fallback.
- [x] Số liệu nguồn, baseline cần đo và mục tiêu đề xuất được phân biệt.
- [x] Có đề xuất card pitch và câu hỏi challenge.
- [ ] Học viên xác nhận lựa chọn, tự chuẩn bị pitch và đối chiếu với trải nghiệm/người dùng thật.
- [ ] Đo baseline pilot và kiểm chứng các giả thuyết trước khi chốt bài nhóm.
