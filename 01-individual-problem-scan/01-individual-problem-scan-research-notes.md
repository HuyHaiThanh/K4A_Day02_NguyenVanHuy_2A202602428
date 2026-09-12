# Hồ sơ nghiên cứu 8 vấn đề — Tài liệu hỗ trợ các phase tiếp theo

Ngày tra cứu: **12/09/2026**. Liên quan: [bảng scan Phase 1](individual-report-nguyenvanhuy.md), [worksheet](../01-worksheet.md), [bài mẫu](../02-deliverable-example.md).

Tài liệu này bổ sung chiều sâu cho 8 vấn đề đã scan. Đây là ghi chú nghiên cứu và đề xuất phân tích, chưa phải Problem Card, bài nhóm hoặc quyết định cuối của học viên.

## Cách sử dụng theo phase

| Phase | Lấy gì từ tài liệu này? | Việc học viên/nhóm vẫn cần làm |
|---|---|---|
| 2 — Top 3 Problem Cards | Actor, mô tả vấn đề, workflow nháp, metric, phương án non-AI | Chọn 3 vấn đề hiểu rõ, kiểm tra lại quy trình và tự trình bày |
| 3 — Hội tụ nhóm | Phạm vi pilot, dữ liệu cần có, câu hỏi phản biện | Các thành viên tự pitch/challenge, chấm điểm và ghi lý do chọn/loại |
| 4 — Validation + research | Link case gốc, giới hạn số liệu, câu hỏi kiểm chứng | Phỏng vấn 2–3 người hoặc khảo sát 5–10 người theo worksheet; nghiên cứu thêm giải pháp |
| 5 — Workflow + PS v0 | Sơ đồ trước/sau, actor, bottleneck dự kiến, metric và boundary | Xác minh input/output, thời gian và bàn giao từng bước; viết PS sau khi kiểm chứng |
| 6 — PS v1 + quyết định | So sánh Rule/Workflow/Agent, fallback, điều kiện pilot | Chốt mức phù hợp và Go/Not Yet/No-Go dựa trên bằng chứng của nhóm |
| 7 — Reflection | Những điểm thiếu/mâu thuẫn đã phát hiện khi dùng AI tìm nguồn | Tự viết trải nghiệm và đóng góp thật; không coi gợi ý của AI là trải nghiệm cá nhân |

## Quy ước bằng chứng

- **Thông tin từ nguồn:** số liệu và mô tả do nhà cung cấp công bố về khách hàng. Đây là nguồn gốc của case, nhưng không phải nghiên cứu độc lập hay số đo của học viên.
- **Phân tích đề xuất:** toàn bộ nội dung sau phần giới hạn ở mỗi hồ sơ. Workflow, mục tiêu pilot, boundary và quyết định có điều kiện là gợi ý cho lab; không khẳng định doanh nghiệp trong case đã triển khai đúng như vậy.
- Không suy ra thời gian từng bước từ tổng thời gian. Không tự đổi tháng/năm sang tuần, hoặc một tuần sang 40 giờ công.
- Kết quả của case không phải mục tiêu đã được nhóm chứng minh. Các mục tiêu phần trăm trong pilot bên dưới là đề xuất ban đầu, phải điều chỉnh sau khi đo.
- Mỗi vấn đề hiện có **một case tham khảo**. Chưa đủ thay thế yêu cầu Phase 4 tìm 2–3 giải pháp/pattern và kiểm chứng người dùng.
- Nguồn thứ cấp không chứng minh học viên đã gặp vấn đề trong công việc. Khi viết bài chính, giữ rõ nguồn gốc quan sát.

## Bản đồ 8 vấn đề

| # | Vấn đề | Số liệu hiện trạng nổi bật | Điểm cần làm rõ trước khi chọn |
|---|---|---|---|
| 1 | Regression thủ công | 1 tuần/bộ test; khoảng 362 ca | Giờ công, thời gian chờ và công bảo trì chưa tách |
| 2 | Tra cứu ticket | Khoảng 15 phút/ticket | Cần ticket và kho tài liệu để đánh giá đúng/sai |
| 3 | Ghép khoản thanh toán | 7–30 phút tra cứu/khoản | Cần người hiểu nghiệp vụ và bộ ghép chuẩn |
| 4 | Tóm tắt ứng viên | 5–10 phút/người | Thu hẹp vào dữ kiện, không đánh giá năng lực |
| 5 | Kiểm tra hóa đơn | Ít nhất 3 phút/chứng từ | Chọn loại chứng từ và quy tắc đối chiếu |
| 6 | Đồng bộ dữ liệu tuyển dụng | Hàng chục cập nhật/nhân viên mới | Chưa có baseline thời gian riêng cho bước này |
| 7 | Lập lịch ca | 2–3 giờ/quản lý/lần soạn và công bố | Cần ràng buộc ca rõ, có thể không cần AI |
| 8 | Tác vụ ngân quỹ | Tới một ngày làm việc/tuần | Số liệu gộp nhiều việc, phải tách phạm vi |

Số liệu và nguồn tương ứng nằm trong từng hồ sơ bên dưới.

## 1. Chạy kiểm thử hồi quy thủ công — SafelyYou

### A. Thông tin đã tìm được từ nguồn

Nhóm QA có khoảng 362 test case; chạy một bộ regression thủ công mất một tuần. Nguồn cho biết bảo trì script Selenium chiếm nhiều công sức. SafelyYou chuyển sang testRigor để tạo và chạy test. Không có thời gian chính xác cho một lượt regression tự động. [testRigor — SafelyYou](https://testrigor.com/case-study-safelyyou/)

**Giới hạn khi sử dụng:** Bài có mốc tạo test không nhất quán: 4 tháng và 4 tuần; bảo trì được ghi cả bằng 0 và khoảng 0,5 giờ/tuần. Không dùng các mốc này làm cam kết. Một tuần chạy test không mặc định là 40 giờ công của một người.

### B. Hiểu vấn đề và actor — phân tích đề xuất

**Ai gặp:** QA phụ trách xác nhận các chức năng cũ vẫn hoạt động trước release; developer nhận lỗi; người phụ trách release quyết định phát hành.

**Vấn đề cần đào sâu:** QA phải lặp lại nhiều thao tác kiểm tra trên cùng bộ chức năng, khiến việc xác nhận bản phát hành kéo dài. Cần tách thời gian chạy test, chuẩn bị dữ liệu, phân tích lỗi và sửa script để tìm đúng bước tốn công.

### C. Workflow nháp cho Problem Card — đề xuất, cần xác minh

**Trước cải tiến:**

```text
Nhận bản build → chọn test → chuẩn bị dữ liệu → chạy từng ca → ghi lỗi → kiểm tra lại → bàn giao kết quả
```

**Sau cải tiến:**

```text
QA duyệt bộ test → chạy tự động trong môi trường thử → gom kết quả → QA xác minh lỗi → người phụ trách quyết định release
```

Không gán thời gian riêng cho các bước vì nguồn chưa công bố đủ. Khi vẽ bản nhóm, bổ sung người làm, input, output, thời gian thực đo và điểm bàn giao ở từng bước.

### D. Metric và thử nghiệm nhỏ — đề xuất

- **Dữ liệu cần có:** Một ứng dụng demo, 10–20 test case có kết quả mong đợi, tài khoản test và dữ liệu dựng lại được.
- **Cách đánh giá:** Giờ công QA cho cùng bộ test; thời gian từ bắt đầu đến có kết quả; số test báo sai hoặc chạy không ổn định. Đo riêng công bảo trì, không chỉ thời gian máy chạy.
- **Mục tiêu pilot nháp:** Pilot trên 10–20 test case, đề xuất giảm ít nhất 30% giờ công QA và không bỏ sót lỗi đã cài sẵn. Đây là mục tiêu thử nghiệm, chưa phải kết quả.
- **Cách đo trước/sau:** Cùng bộ đầu vào và tiêu chí chất lượng; ghi riêng thời gian làm, chờ, kiểm tra và sửa. Nếu lặp lại cùng dữ liệu, chú ý hiệu ứng người làm đã nhớ đáp án.

### E. So sánh phương án — giả thuyết để nhóm phản biện

| Mức | Phương án cho phạm vi pilot |
|---|---|
| No AI / Rule | Script có assertion rõ cho luồng ổn định; đây là phương án cần thử trước. |
| Workflow | Chuẩn bị môi trường → chạy bộ test → tổng hợp bằng chứng → QA xác minh; AI có thể hỗ trợ viết bản nháp test hoặc đọc log. |
| Agent | Chỉ có lý do nếu cần chọn bước khám phá theo trạng thái ứng dụng; phải giới hạn môi trường và số thao tác. |

**Boundary:** Không chạy trên dữ liệu production, không cho AI tự sửa tiêu chí pass để làm test xanh, không tự phê duyệt release.

**Fallback và điều kiện dừng:** QA kiểm tra lại ca thất bại bằng tay; khi test không ổn định, tạm loại khỏi cổng chặn release và theo dõi riêng. Dừng pilot để xem lại nếu vượt quyền, mất dấu vết nguồn hoặc kết quả sai không bị phát hiện.

### F. Validation và chuẩn bị Problem Statement

**Câu hỏi cần hỏi người thật:** Lần release gần nhất, mất thời gian ở chạy test hay sửa test? Bao nhiêu test thực sự lặp lại? Ai xác định kết quả đúng? Có môi trường và dữ liệu để chạy lại không?

**Dữ liệu cần ghi vào PS v0:** actor trong phạm vi nhóm chọn; workflow đã xác minh; một bottleneck chính; ảnh hưởng nếu chậm/sai; metric có baseline và cách đo; việc làm và không làm.

**Bổ sung cho PS v1:** điểm can thiệp giữa hai bước; mức tự động hóa được chọn sau so sánh; rủi ro lớn nhất; người kiểm tra và cách kiểm tra.

**Điều kiện quyết định nháp:** Có thể Go cho pilot nếu có ứng dụng demo và bộ test chuẩn. Not Yet nếu chưa định nghĩa được kết quả mong đợi; không suy ra Go cho hệ thống chăm sóc sức khỏe thật.

---


## 2. Tra cứu ngữ cảnh ticket kỹ thuật — ClickUp

### A. Thông tin đã tìm được từ nguồn

Đội hỗ trợ xử lý khoảng 5.000 ticket/tháng. Nhân viên lấy thông tin từ Zendesk và đối chiếu tài liệu trước khi trả lời. Thời gian tra cứu được công bố giảm từ 15 xuống khoảng 4 phút/ticket nhờ hệ thống hỗ trợ bằng AI và Zapier MCP. [Zapier — ClickUp](https://zapier.com/customer-stories/clickup)

**Giới hạn khi sử dụng:** Đây là thời gian tra cứu, không phải tổng thời gian giải quyết ticket. Nguồn không nêu thiết kế đo chi tiết. Mẫu agent công khai trong bài được khái quát hóa, không đồng nhất với triển khai nội bộ ClickUp.

### B. Hiểu vấn đề và actor — phân tích đề xuất

**Ai gặp:** Nhân viên technical support cần đủ bằng chứng để đưa ra bước xử lý; khách hàng chờ phản hồi; chuyên gia kỹ thuật tiếp nhận trường hợp khó.

**Vấn đề cần đào sâu:** Thông tin có thể nằm ở mô tả lỗi, lịch sử trao đổi và tài liệu hướng dẫn khác nhau. Nhân viên phải tự nối chúng trước khi trả lời. Phạm vi nên là chuẩn bị ngữ cảnh cho người hỗ trợ, tránh mở rộng thành giải quyết mọi ticket.

### C. Workflow nháp cho Problem Card — đề xuất, cần xác minh

**Trước cải tiến:**

```text
Đọc ticket → lấy lịch sử → tìm tài liệu → đối chiếu phiên bản → chọn hướng xử lý → soạn và kiểm tra phản hồi
```

**Sau cải tiến:**

```text
Nhận ticket → truy xuất nguồn được phép → AI đề xuất ngữ cảnh kèm dẫn chứng → nhân viên kiểm tra → soạn/gửi phản hồi
```

Không gán thời gian riêng cho các bước vì nguồn chưa công bố đủ. Khi vẽ bản nhóm, bổ sung người làm, input, output, thời gian thực đo và điểm bàn giao ở từng bước.

### D. Metric và thử nghiệm nhỏ — đề xuất

- **Dữ liệu cần có:** 20 ticket đã ẩn danh hoặc mô phỏng, bộ tài liệu nhỏ có phiên bản, đáp án tham chiếu do người hiểu sản phẩm kiểm tra.
- **Cách đánh giá:** Phút từ mở ticket đến đủ ngữ cảnh; tỷ lệ dẫn chứng đúng; số gợi ý sai; thời gian người kiểm tra sửa bản tóm tắt.
- **Mục tiêu pilot nháp:** Đề xuất giảm 30% thời gian chuẩn bị trên cùng bộ ticket, mọi hướng dẫn phải có nguồn truy xuất được. Không mặc định sẽ đạt 4 phút như case.
- **Cách đo trước/sau:** Cùng bộ đầu vào và tiêu chí chất lượng; ghi riêng thời gian làm, chờ, kiểm tra và sửa. Nếu lặp lại cùng dữ liệu, chú ý hiệu ứng người làm đã nhớ đáp án.

### E. So sánh phương án — giả thuyết để nhóm phản biện

| Mức | Phương án cho phạm vi pilot |
|---|---|
| No AI / Rule | Định tuyến theo sản phẩm, phiên bản, mã lỗi; tìm kiếm theo từ khóa có thể đủ cho câu hỏi chuẩn. |
| Workflow | Lấy ticket → tìm tài liệu → tạo bản tóm tắt có nguồn → người duyệt. Đây là giả thuyết ưu tiên để thử. |
| Agent | Cân nhắc khi phải chọn nhiều lượt tìm kiếm tùy thông tin còn thiếu; đặt giới hạn số lượt và quyền chỉ đọc. |

**Boundary:** Không tự gửi câu trả lời, đổi cấu hình khách hàng, cấp quyền hoặc hứa thời gian sửa lỗi. Không truy xuất ticket ngoài quyền được cấp.

**Fallback và điều kiện dừng:** Không tìm thấy bằng chứng hoặc nguồn mâu thuẫn thì trả trạng thái chưa đủ thông tin và chuyển nhân viên tra cứu. Dừng pilot để xem lại nếu vượt quyền, mất dấu vết nguồn hoặc kết quả sai không bị phát hiện.

### F. Validation và chuẩn bị Problem Statement

**Câu hỏi cần hỏi người thật:** Nhân viên dùng những nguồn nào? Vướng ở tìm nguồn hay hiểu nội dung? Tài liệu có lỗi thời không? Một ticket cần mấy lần chuyển người xử lý?

**Dữ liệu cần ghi vào PS v0:** actor trong phạm vi nhóm chọn; workflow đã xác minh; một bottleneck chính; ảnh hưởng nếu chậm/sai; metric có baseline và cách đo; việc làm và không làm.

**Bổ sung cho PS v1:** điểm can thiệp giữa hai bước; mức tự động hóa được chọn sau so sánh; rủi ro lớn nhất; người kiểm tra và cách kiểm tra.

**Điều kiện quyết định nháp:** Go cho pilot chỉ đọc khi có ticket và tài liệu được phép dùng. Not Yet nếu thiếu bộ nguồn hoặc không có người đánh giá tính đúng.

---


## 3. Ghép khoản thanh toán với hóa đơn — EY

### A. Thông tin đã tìm được từ nguồn

EY nhận khoảng 1,5 triệu khoản thanh toán/năm; ban đầu 30% được SAP tự ghép và tất toán. Khoản còn lại cần 7–30 phút tra cứu và 4–25 phút xử lý trong SAP. PowerMatch kết hợp Power Automate, AI Builder và Dataverse để hỗ trợ quy trình. [Microsoft Learn — EY](https://learn.microsoft.com/en-us/power-platform/guidance/case-studies/global-finance)

**Giới hạn khi sử dụng:** Không cộng hai khoảng thành thời gian trung bình. Mục tiêu tăng tự động hóa lên 80% trong phần đầu bài là mục tiêu, không mặc định là kết quả toàn cầu. Không có số giao dịch mỗi tuần.

### B. Hiểu vấn đề và actor — phân tích đề xuất

**Ai gặp:** Kế toán khoản phải thu cần xác định khách đã trả cho hóa đơn nào; người kiểm soát kế toán duyệt xử lý ngoại lệ.

**Vấn đề cần đào sâu:** Khoản tiền về chưa có liên kết chắc chắn với hóa đơn. Cần thu hẹp vào tìm ứng viên hóa đơn và giải thích phép ghép, tránh ôm toàn bộ kế toán hoặc tất toán tự động.

### C. Workflow nháp cho Problem Card — đề xuất, cần xác minh

**Trước cải tiến:**

```text
Nhận giao dịch → tìm thông báo trả tiền → tìm hóa đơn → kiểm tra mã và số tiền → xử lý chênh lệch → nhập kết quả
```

**Sau cải tiến:**

```text
Nhận dữ liệu → rule ghép trường hợp rõ → đề xuất các hóa đơn còn lại → kế toán kiểm tra → xuất bảng kết quả
```

Không gán thời gian riêng cho các bước vì nguồn chưa công bố đủ. Khi vẽ bản nhóm, bổ sung người làm, input, output, thời gian thực đo và điểm bàn giao ở từng bước.

### D. Metric và thử nghiệm nhỏ — đề xuất

- **Dữ liệu cần có:** Bảng hóa đơn và giao dịch giả lập/ẩn danh, gồm trường hợp trả đủ, trả thiếu, trả gộp và thiếu mã; kết quả ghép chuẩn.
- **Cách đánh giá:** Phút tra cứu/khoản; tỷ lệ gợi ý ghép đúng; tỷ lệ chuyển người xử lý; số ghép nhầm. Tách công tra cứu khỏi công ghi nhận kế toán.
- **Mục tiêu pilot nháp:** Đề xuất giảm 30% thời gian tra cứu trong mẫu 20–30 giao dịch, không cho phép ghép sai được ghi nhận tự động.
- **Cách đo trước/sau:** Cùng bộ đầu vào và tiêu chí chất lượng; ghi riêng thời gian làm, chờ, kiểm tra và sửa. Nếu lặp lại cùng dữ liệu, chú ý hiệu ứng người làm đã nhớ đáp án.

### E. So sánh phương án — giả thuyết để nhóm phản biện

| Mức | Phương án cho phạm vi pilot |
|---|---|
| No AI / Rule | Khớp mã hóa đơn, khách hàng, tiền tệ và số tiền trước; không cần AI cho phép khớp chính xác. |
| Workflow | Trích dữ liệu → rule kiểm tra → AI hỗ trợ đọc thông báo tự do → kế toán duyệt ngoại lệ. |
| Agent | Chỉ cân nhắc việc chọn nguồn tra cứu khi một khoản liên quan nhiều chứng từ; chưa cần cho pilot hai bảng. |

**Boundary:** Chỉ tạo gợi ý, không chuyển tiền, xóa công nợ hoặc ghi sổ thật. Giữ nguyên chứng từ gốc và người phê duyệt.

**Fallback và điều kiện dừng:** Không có phép ghép duy nhất thì để chưa ghép, giữ danh sách ứng viên và chuyển kế toán. Dừng pilot để xem lại nếu vượt quyền, mất dấu vết nguồn hoặc kết quả sai không bị phát hiện.

### F. Validation và chuẩn bị Problem Statement

**Câu hỏi cần hỏi người thật:** Thiếu thông tin nào gây tra cứu lâu nhất? Tỷ lệ trả gộp/thiếu mã là bao nhiêu? Có thể xử lý bằng quy định mã chuyển khoản không? Ai chịu trách nhiệm nếu ghép sai?

**Dữ liệu cần ghi vào PS v0:** actor trong phạm vi nhóm chọn; workflow đã xác minh; một bottleneck chính; ảnh hưởng nếu chậm/sai; metric có baseline và cách đo; việc làm và không làm.

**Bổ sung cho PS v1:** điểm can thiệp giữa hai bước; mức tự động hóa được chọn sau so sánh; rủi ro lớn nhất; người kiểm tra và cách kiểm tra.

**Điều kiện quyết định nháp:** Go cho mô phỏng ngoại tuyến khi có đáp án chuẩn. Not Yet cho kết nối sổ thật nếu chưa có chủ quy trình và kiểm soát sai lệch.

---


## 4. Nhập và tóm tắt thông tin ứng viên — JBGoodwin REALTORS

### A. Thông tin đã tìm được từ nguồn

Nhân viên tuyển dụng từng mất 5–10 phút để tạo một bản tóm tắt ứng viên; nhập dữ liệu thủ công chiếm tới 25% thời gian. Case dùng Zapier, HubSpot, Gmail và AI để thu thập, bổ sung, tổng hợp dữ liệu. [Zapier — JBGoodwin REALTORS](https://zapier.com/customer-stories/JBGoodwin-REALTORS)

**Giới hạn khi sử dụng:** Không có số phút sau cải tiến trên mỗi ứng viên. Không coi thay đổi số người tuyển được là tác động riêng của việc tóm tắt. Bài này không phải bằng chứng AI đánh giá năng lực tốt hơn người.

### B. Hiểu vấn đề và actor — phân tích đề xuất

**Ai gặp:** Recruiter cần hồ sơ có cấu trúc để chuẩn bị trao đổi; người phụ trách tuyển dụng đọc bản tóm tắt; ứng viên cung cấp dữ liệu.

**Vấn đề cần đào sâu:** Thông tin đầu vào không thống nhất khiến recruiter phải nhập lại và viết bản tổng hợp. Chọn phạm vi trích xuất dữ kiện và chuẩn bị hồ sơ, không biến thành tự động chọn/loại ứng viên.

### C. Workflow nháp cho Problem Card — đề xuất, cần xác minh

**Trước cải tiến:**

```text
Nhận hồ sơ → đọc → chép thông tin → tìm phần còn thiếu → viết tóm tắt → kiểm tra
```

**Sau cải tiến:**

```text
Nhận hồ sơ → trích trường → đánh dấu thiếu → tạo tóm tắt có dẫn chứng → recruiter duyệt
```

Không gán thời gian riêng cho các bước vì nguồn chưa công bố đủ. Khi vẽ bản nhóm, bổ sung người làm, input, output, thời gian thực đo và điểm bàn giao ở từng bước.

### D. Metric và thử nghiệm nhỏ — đề xuất

- **Dữ liệu cần có:** 10–20 hồ sơ giả lập theo nhiều định dạng, bộ trường cần lấy và bảng đáp án do người kiểm tra lập.
- **Cách đánh giá:** Phút tạo hồ sơ hoàn chỉnh; tỷ lệ trường trích đúng; số thông tin không có trong nguồn; phút sửa bản nháp.
- **Mục tiêu pilot nháp:** Đề xuất giảm 30% tổng thời gian chuẩn bị và kiểm tra; không chấp nhận thêm kinh nghiệm/chứng chỉ không có trong hồ sơ.
- **Cách đo trước/sau:** Cùng bộ đầu vào và tiêu chí chất lượng; ghi riêng thời gian làm, chờ, kiểm tra và sửa. Nếu lặp lại cùng dữ liệu, chú ý hiệu ứng người làm đã nhớ đáp án.

### E. So sánh phương án — giả thuyết để nhóm phản biện

| Mức | Phương án cho phạm vi pilot |
|---|---|
| No AI / Rule | Form có trường bắt buộc và import dữ liệu có thể loại phần lớn việc nhập lại. |
| Workflow | Trích dữ kiện → kiểm tra thiếu → tóm tắt → người duyệt; AI hữu ích với nội dung tự do. |
| Agent | Chưa cần khi dữ liệu nằm trong hồ sơ đã nhận; chỉ cân nhắc điều phối kiểm tra bổ sung khi được cho phép. |

**Boundary:** Không tự chấm điểm, xếp hạng, loại người hoặc suy đoán tính cách. Không tìm dữ liệu cá nhân ngoài bộ hồ sơ được phép.

**Fallback và điều kiện dừng:** Thông tin không rõ được ghi chưa xác định; recruiter đọc lại đoạn gốc hoặc hỏi ứng viên. Dừng pilot để xem lại nếu vượt quyền, mất dấu vết nguồn hoặc kết quả sai không bị phát hiện.

### F. Validation và chuẩn bị Problem Statement

**Câu hỏi cần hỏi người thật:** Recruiter cần những trường nào để chuẩn bị trao đổi? Bao nhiêu thời gian là chép dữ liệu, bao nhiêu là đánh giá? Form chuẩn có đủ giải quyết vấn đề không?

**Dữ liệu cần ghi vào PS v0:** actor trong phạm vi nhóm chọn; workflow đã xác minh; một bottleneck chính; ảnh hưởng nếu chậm/sai; metric có baseline và cách đo; việc làm và không làm.

**Bổ sung cho PS v1:** điểm can thiệp giữa hai bước; mức tự động hóa được chọn sau so sánh; rủi ro lớn nhất; người kiểm tra và cách kiểm tra.

**Điều kiện quyết định nháp:** Go cho bản nháp dữ kiện trên hồ sơ giả lập. Not Yet cho dữ liệu thật nếu chưa rõ quyền sử dụng và người duyệt.

---


## 5. Kiểm tra hóa đơn đính kèm — CATRION

### A. Thông tin đã tìm được từ nguồn

Kế toán phải trả mất ít nhất 3 phút để kiểm tra một hóa đơn đính kèm. CATRION dùng Power Automate và Azure AI Vision để đọc dữ liệu, đối chiếu đơn mua và cập nhật ERP; trường hợp lệch được đánh dấu. Với loại hóa đơn đã huấn luyện, nguồn công bố thời gian dưới 1 phút. [Microsoft — CATRION](https://www.microsoft.com/en/customers/story/24577-catrion-microsoft-power-platform)

**Giới hạn khi sử dụng:** Kết quả chỉ áp dụng cho nhóm định dạng đã huấn luyện. Không có khối lượng/tuần hoặc thời gian xử lý ngoại lệ; chưa rõ mức đo sau bao gồm bao nhiêu công kiểm tra của người.

### B. Hiểu vấn đề và actor — phân tích đề xuất

**Ai gặp:** Nhân viên kế toán phải trả kiểm tra chứng từ; người mua hàng giải thích sai lệch; người có thẩm quyền duyệt thanh toán.

**Vấn đề cần đào sâu:** Đọc hóa đơn và đối chiếu thủ công lặp lại theo từng chứng từ. Cần phân biệt lỗi đọc dữ liệu với sai lệch nghiệp vụ; trích đúng số chưa có nghĩa chứng từ hợp lệ để thanh toán.

### C. Workflow nháp cho Problem Card — đề xuất, cần xác minh

**Trước cải tiến:**

```text
Nhận hóa đơn → đọc trường → tìm đơn mua → đối chiếu → ghi chênh lệch → chuyển kiểm tra
```

**Sau cải tiến:**

```text
Nhận PDF → trích dữ liệu → rule đối chiếu → đánh dấu lệch → kế toán kiểm tra → xuất bảng
```

Không gán thời gian riêng cho các bước vì nguồn chưa công bố đủ. Khi vẽ bản nhóm, bổ sung người làm, input, output, thời gian thực đo và điểm bàn giao ở từng bước.

### D. Metric và thử nghiệm nhỏ — đề xuất

- **Dữ liệu cần có:** 10–20 cặp hóa đơn/đơn mua giả lập, gồm ảnh mờ, sai số tiền, khác đơn vị và hóa đơn trùng; bảng dữ liệu chuẩn.
- **Cách đánh giá:** Phút kiểm tra/chứng từ; tỷ lệ trường đọc đúng; tỷ lệ phát hiện sai lệch; số lỗi bị bỏ sót; phút xử lý ngoại lệ.
- **Mục tiêu pilot nháp:** Đề xuất giảm 30% công kiểm tra trên một loại hóa đơn đã chọn, phát hiện đầy đủ các lỗi chủ động cài vào bộ thử. Không lấy dưới 1 phút làm mặc định.
- **Cách đo trước/sau:** Cùng bộ đầu vào và tiêu chí chất lượng; ghi riêng thời gian làm, chờ, kiểm tra và sửa. Nếu lặp lại cùng dữ liệu, chú ý hiệu ứng người làm đã nhớ đáp án.

### E. So sánh phương án — giả thuyết để nhóm phản biện

| Mức | Phương án cho phạm vi pilot |
|---|---|
| No AI / Rule | Yêu cầu mẫu thống nhất; công thức kiểm tra số tiền, mã đơn, dữ liệu bắt buộc và bản trùng. |
| Workflow | OCR/trích trường → kiểm tra định dạng → đối chiếu → người duyệt. Đường đi rõ nên phù hợp pilot có kiểm soát. |
| Agent | Chỉ có lý do khi cần chọn thêm chứng từ theo loại sai lệch; không cần để so hai tài liệu cố định. |

**Boundary:** Không tự duyệt hoặc thực hiện thanh toán, không sửa chứng từ; chỉ gợi ý dữ liệu và điểm lệch.

**Fallback và điều kiện dừng:** Ảnh mờ, thiếu trang hoặc dữ liệu mâu thuẫn thì chuyển kiểm tra thủ công; không điền đoán. Dừng pilot để xem lại nếu vượt quyền, mất dấu vết nguồn hoặc kết quả sai không bị phát hiện.

### F. Validation và chuẩn bị Problem Statement

**Câu hỏi cần hỏi người thật:** Định dạng nào gặp nhiều nhất? Lỗi thường nằm ở đọc chữ hay điều kiện nghiệp vụ? Chứng từ có bản trùng không? Người duyệt cần bằng chứng gì?

**Dữ liệu cần ghi vào PS v0:** actor trong phạm vi nhóm chọn; workflow đã xác minh; một bottleneck chính; ảnh hưởng nếu chậm/sai; metric có baseline và cách đo; việc làm và không làm.

**Bổ sung cho PS v1:** điểm can thiệp giữa hai bước; mức tự động hóa được chọn sau so sánh; rủi ro lớn nhất; người kiểm tra và cách kiểm tra.

**Điều kiện quyết định nháp:** Go cho một mẫu chứng từ và đầu ra bảng kiểm tra. Not Yet nếu không có đáp án chuẩn hoặc chưa rõ quy tắc đối chiếu.

---


## 6. Cập nhật dữ liệu nhân viên mới ở nhiều bảng — StackAdapt

### A. Thông tin đã tìm được từ nguồn

Kathy Lam gặp tình trạng ATS chưa tích hợp HRIS. Mỗi nhân viên mới cần hàng chục cập nhật thủ công qua Finance, People Ops, Comp, Payroll và FP&A. Zapier chuyển dữ liệu khi ứng viên được đánh dấu đã tuyển. Bài công bố hơn 10 giờ/tuần tiết kiệm từ các quy trình tuyển dụng qua 5 nhóm. [Zapier — StackAdapt, 25/09/2025](https://zapier.com/blog/stackadapt-automates-hiring-with-zapier/)

**Giới hạn khi sử dụng:** Hơn 10 giờ/tuần là mức tiết kiệm của tập hợp quy trình, không phải thời gian ban đầu hoặc mức tiết kiệm riêng của đồng bộ nhân viên. Cần đo baseline mới cho phạm vi hẹp.

### B. Hiểu vấn đề và actor — phân tích đề xuất

**Ai gặp:** Nhân viên vận hành tuyển dụng cập nhật dữ liệu; HR và các nhóm tài chính dùng dữ liệu cho onboarding, lương và dự báo.

**Vấn đề cần đào sâu:** Một sự kiện tuyển mới phải được chép lại ở nhiều nơi. Cập nhật thiếu, chậm hoặc khác phiên bản làm các nhóm dùng dữ liệu không thống nhất. Đây là ứng viên tốt để kiểm tra liệu tích hợp đơn giản đã đủ.

### C. Workflow nháp cho Problem Card — đề xuất, cần xác minh

**Trước cải tiến:**

```text
Xác nhận tuyển → lấy hồ sơ → nhập bảng A → nhập bảng B → thông báo → kiểm tra các bản → sửa lệch
```

**Sau cải tiến:**

```text
Nhận sự kiện → kiểm tra trường bắt buộc → đồng bộ theo mã nhân viên → ghi log → báo ngoại lệ cho owner
```

Không gán thời gian riêng cho các bước vì nguồn chưa công bố đủ. Khi vẽ bản nhóm, bổ sung người làm, input, output, thời gian thực đo và điểm bàn giao ở từng bước.

### D. Metric và thử nghiệm nhỏ — đề xuất

- **Dữ liệu cần có:** 10 hồ sơ giả lập, 2–3 bảng đích có cấu trúc khác nhau, quy tắc ánh xạ trường và tình huống sự kiện gửi lại.
- **Cách đánh giá:** Phút xử lý một nhân viên; số trường sai/thiếu; độ trễ tới khi các bảng nhận đủ; số bản ghi trùng khi chạy lại.
- **Mục tiêu pilot nháp:** Đề xuất giảm 50% thao tác nhập lại; chạy lại cùng sự kiện không sinh bản ghi trùng. Mốc thời gian tuyệt đối phải đo từ mô phỏng.
- **Cách đo trước/sau:** Cùng bộ đầu vào và tiêu chí chất lượng; ghi riêng thời gian làm, chờ, kiểm tra và sửa. Nếu lặp lại cùng dữ liệu, chú ý hiệu ứng người làm đã nhớ đáp án.

### E. So sánh phương án — giả thuyết để nhóm phản biện

| Mức | Phương án cho phạm vi pilot |
|---|---|
| No AI / Rule | Một nguồn dữ liệu chuẩn, trường bắt buộc và import CSV có thể đủ khi số nhân viên mới ít. |
| Workflow | Sự kiện tuyển → kiểm tra → ánh xạ → cập nhật từng nơi → báo lỗi. Ưu tiên luồng xác định, không cần AI nếu dữ liệu có cấu trúc. |
| Agent | Chưa có lý do cho pilot đồng bộ trường cố định; chỉ cân nhắc khi phải điều phối ngoại lệ không có đường xử lý chuẩn. |

**Boundary:** Không tự thay mức lương, thông tin ngân hàng hay quyết định tuyển. Demo dùng dữ liệu giả; quy định rõ ai được xem từng trường.

**Fallback và điều kiện dừng:** Bảng đích lỗi thì lưu trạng thái chờ và thông báo; chạy lại có kiểm tra trùng, không tạo lại mọi bản ghi. Dừng pilot để xem lại nếu vượt quyền, mất dấu vết nguồn hoặc kết quả sai không bị phát hiện.

### F. Validation và chuẩn bị Problem Statement

**Câu hỏi cần hỏi người thật:** Nguồn nào là bản chuẩn? Điều gì xảy ra khi sửa ngày nhận việc? Ai chịu trách nhiệm lỗi đồng bộ? Có tích hợp sẵn thay vì tự xây không?

**Dữ liệu cần ghi vào PS v0:** actor trong phạm vi nhóm chọn; workflow đã xác minh; một bottleneck chính; ảnh hưởng nếu chậm/sai; metric có baseline và cách đo; việc làm và không làm.

**Bổ sung cho PS v1:** điểm can thiệp giữa hai bước; mức tự động hóa được chọn sau so sánh; rủi ro lớn nhất; người kiểm tra và cách kiểm tra.

**Điều kiện quyết định nháp:** Go cho demo 2–3 bảng với dữ liệu giả. No-Go cho phần AI nếu rule và workflow đã giải đủ vấn đề; điều này không có nghĩa bỏ bài toán.

---


## 7. Lập và chỉnh lịch ca bằng Excel — Mud Bay

### A. Thông tin đã tìm được từ nguồn

Quản lý ở 60 địa điểm mất trung bình 2–3 giờ/người để soạn và công bố lịch, cộng dồn 120–180 giờ. Nguồn mô tả thay đổi trong Excel dễ hỏng công thức và khó theo dõi chỉnh sửa giữa các tuần. Mud Bay dùng Deputy để quản lý lịch và giờ công. [Deputy — Mud Bay](https://www.deputy.com/customers/mud-bay)

**Giới hạn khi sử dụng:** Không có số giờ lập lịch sau cải tiến để tạo cặp trước/sau đáng tin. Không coi 120–180 giờ là công của một quản lý; không áp quy mô 60 cửa hàng cho pilot một cửa hàng.

### B. Hiểu vấn đề và actor — phân tích đề xuất

**Ai gặp:** Quản lý cửa hàng phân ca; nhân viên đăng ký thời gian có thể làm; người phụ trách vận hành theo dõi mức phủ ca.

**Vấn đề cần đào sâu:** Mỗi lần sửa lịch có thể kéo theo thiếu người hoặc lệch tổng giờ. Cần làm rõ phần khó là tính lịch thỏa điều kiện hay trao đổi để xác nhận người thay ca.

### C. Workflow nháp cho Problem Card — đề xuất, cần xác minh

**Trước cải tiến:**

```text
Thu đăng ký → xác định nhu cầu → phân ca → kiểm tra giờ → sửa xung đột → công bố → cập nhật thay đổi
```

**Sau cải tiến:**

```text
Chuẩn hóa đăng ký → bộ lập lịch tạo phương án → kiểm tra ràng buộc → quản lý duyệt → phát hành một phiên bản
```

Không gán thời gian riêng cho các bước vì nguồn chưa công bố đủ. Khi vẽ bản nhóm, bổ sung người làm, input, output, thời gian thực đo và điểm bàn giao ở từng bước.

### D. Metric và thử nghiệm nhỏ — đề xuất

- **Dữ liệu cần có:** Danh sách 8–12 nhân viên giả lập, ca trong một tuần, khả năng làm việc, kỹ năng và các giới hạn do bài tập quy định.
- **Cách đánh giá:** Phút lập và chỉnh lịch/tuần; số ca thiếu người; số vi phạm ràng buộc; số vòng quản lý phải sửa.
- **Mục tiêu pilot nháp:** Đề xuất giảm 30% thời gian lập/chỉnh trên cùng dữ liệu và không vi phạm ràng buộc bắt buộc. Không để tốc độ tăng bằng cách bỏ điều kiện.
- **Cách đo trước/sau:** Cùng bộ đầu vào và tiêu chí chất lượng; ghi riêng thời gian làm, chờ, kiểm tra và sửa. Nếu lặp lại cùng dữ liệu, chú ý hiệu ứng người làm đã nhớ đáp án.

### E. So sánh phương án — giả thuyết để nhóm phản biện

| Mức | Phương án cho phạm vi pilot |
|---|---|
| No AI / Rule | Mẫu ca, kiểm tra điều kiện và thuật toán tối ưu có thể giải trực tiếp phần xếp lịch; không mặc định cần mô hình ngôn ngữ. |
| Workflow | Thu đăng ký → tạo lịch bằng bộ giải → kiểm tra → quản lý duyệt; AI chỉ hỗ trợ hiểu yêu cầu tự do hoặc giải thích xung đột. |
| Agent | Chỉ cân nhắc điều phối nhiều phương án thay ca khi phát sinh biến động; vẫn cần người duyệt và giới hạn quyền sửa. |

**Boundary:** Chỉ tạo lịch nháp, không tự gửi cho nhân viên thật; ràng buộc demo không được coi là tư vấn tuân thủ pháp luật lao động.

**Fallback và điều kiện dừng:** Nếu không có lịch hợp lệ, chỉ rõ các điều kiện xung đột để quản lý điều chỉnh; không âm thầm nới giới hạn. Dừng pilot để xem lại nếu vượt quyền, mất dấu vết nguồn hoặc kết quả sai không bị phát hiện.

### F. Validation và chuẩn bị Problem Statement

**Câu hỏi cần hỏi người thật:** Mất công nhiều nhất ở tạo lịch hay đổi lịch? Điều kiện nào bắt buộc, điều kiện nào là ưu tiên? Ai xác nhận lịch cuối? Có mẫu tuần trước dùng lại được không?

**Dữ liệu cần ghi vào PS v0:** actor trong phạm vi nhóm chọn; workflow đã xác minh; một bottleneck chính; ảnh hưởng nếu chậm/sai; metric có baseline và cách đo; việc làm và không làm.

**Bổ sung cho PS v1:** điểm can thiệp giữa hai bước; mức tự động hóa được chọn sau so sánh; rủi ro lớn nhất; người kiểm tra và cách kiểm tra.

**Điều kiện quyết định nháp:** Go cho bài toán một cửa hàng khi ràng buộc rõ. Not Yet nếu yêu cầu mâu thuẫn mà chưa có người quyết định ưu tiên.

---


## 8. Đối soát ngân hàng và công việc ngân quỹ tuần — L&M Fleet Supply

### A. Thông tin đã tìm được từ nguồn

Case mô tả tự động đối soát 25 tài khoản ngân hàng bằng tích hợp SK Global Treasury Automation Suite với Dynamics 365. Nhóm tác vụ ngân quỹ hằng tuần trước đây chiếm tới một ngày của nhân sự cấp cao, sau đó hoàn tất dưới một giờ. [Microsoft — L&M Fleet Supply, 27/08/2025](https://www.microsoft.com/en/customers/story/25084-l-and-m-fleet-supply-dynamics-365-commerce)

**Giới hạn khi sử dụng:** Con số thuộc cả nhóm tác vụ ngân quỹ; chưa biết riêng đối soát chiếm bao nhiêu. Nguồn không định nghĩa một ngày là bao nhiêu giờ. Không nhầm với số liệu thời gian đóng sổ tháng hoặc xử lý hóa đơn ở phần khác của bài.

### B. Hiểu vấn đề và actor — phân tích đề xuất

**Ai gặp:** Nhân viên/người quản lý ngân quỹ so khớp dữ liệu ngân hàng với sổ; người kiểm soát tài chính xem các chênh lệch.

**Vấn đề cần đào sâu:** Dữ liệu nhiều tài khoản làm tăng công thu thập và đối chiếu. Cần xác minh liệu bước nghẽn nằm ở lấy file, chuẩn hóa hay điều tra chênh lệch trước khi thiết kế giải pháp.

### C. Workflow nháp cho Problem Card — đề xuất, cần xác minh

**Trước cải tiến:**

```text
Thu sao kê → lấy sổ → chuẩn hóa → đối chiếu → phân loại lệch → xác minh → hoàn tất kiểm tra tuần
```

**Sau cải tiến:**

```text
Nhận file chuẩn → rule ghép → xuất danh sách chênh lệch → người kiểm tra → lưu kết quả có dấu vết
```

Không gán thời gian riêng cho các bước vì nguồn chưa công bố đủ. Khi vẽ bản nhóm, bổ sung người làm, input, output, thời gian thực đo và điểm bàn giao ở từng bước.

### D. Metric và thử nghiệm nhỏ — đề xuất

- **Dữ liệu cần có:** Sao kê và sổ giả lập cho 2–3 tài khoản, có phí, giao dịch trễ, bản trùng và khoản chưa ghi nhận; bảng đáp án.
- **Cách đánh giá:** Tổng giờ công theo đợt và giờ công từng bước; số chênh lệch phát hiện đúng; số ghép sai; phần tồn đọng cần xác minh.
- **Mục tiêu pilot nháp:** Đề xuất giảm 30% công đối chiếu trong pilot, giữ nguyên khả năng phát hiện lỗi cài sẵn. Đo baseline của pilot thay vì dùng một ngày cho toàn bộ quy trình nhỏ.
- **Cách đo trước/sau:** Cùng bộ đầu vào và tiêu chí chất lượng; ghi riêng thời gian làm, chờ, kiểm tra và sửa. Nếu lặp lại cùng dữ liệu, chú ý hiệu ứng người làm đã nhớ đáp án.

### E. So sánh phương án — giả thuyết để nhóm phản biện

| Mức | Phương án cho phạm vi pilot |
|---|---|
| No AI / Rule | Chuẩn hóa CSV, mã tham chiếu và phép khớp xác định; bảng tính có kiểm tra chéo là phương án non-AI. |
| Workflow | Import → kiểm tra → ghép → báo lệch → người duyệt. AI chỉ có thể hỗ trợ diễn giải nội dung giao dịch không cấu trúc. |
| Agent | Chưa cần cho hai file cố định; cân nhắc nếu phải chọn thêm nguồn chứng từ khi điều tra ngoại lệ. |

**Boundary:** Chỉ đọc và tạo bảng chênh lệch; không truy cập tài khoản ngân hàng thật, chuyển tiền hoặc sửa sổ kế toán.

**Fallback và điều kiện dừng:** Khoản không khớp ở lại danh sách ngoại lệ; file lỗi định dạng bị từ chối và báo rõ thay vì tiếp tục với dữ liệu thiếu. Dừng pilot để xem lại nếu vượt quyền, mất dấu vết nguồn hoặc kết quả sai không bị phát hiện.

### F. Validation và chuẩn bị Problem Statement

**Câu hỏi cần hỏi người thật:** Một ngày trước đây gồm những việc gì? Riêng đối soát tốn bao lâu? Có bao nhiêu tài khoản và định dạng? Ai xác minh chênh lệch? Công cụ hiện có đã hỗ trợ import/ghép chưa?

**Dữ liệu cần ghi vào PS v0:** actor trong phạm vi nhóm chọn; workflow đã xác minh; một bottleneck chính; ảnh hưởng nếu chậm/sai; metric có baseline và cách đo; việc làm và không làm.

**Bổ sung cho PS v1:** điểm can thiệp giữa hai bước; mức tự động hóa được chọn sau so sánh; rủi ro lớn nhất; người kiểm tra và cách kiểm tra.

**Điều kiện quyết định nháp:** Go cho pilot ngoại tuyến với dữ liệu giả. Not Yet nếu nhóm chưa hiểu phân biệt lệch thật với lệch thời điểm.

---

## Gợi ý chọn top 3 — nhận định cho bối cảnh sinh viên CNTT / Software Engineer

Đây là ưu tiên dựa trên khả năng làm pilot nhỏ và đánh giá kết quả, không phải lựa chọn cuối hay điểm số của nhóm.

| Ưu tiên xem xét | Lý do | Điều kiện tối thiểu |
|---|---|---|
| #2 — Tra cứu ticket kỹ thuật | Actor và bước nghẽn rõ; dễ thể hiện AI hỗ trợ hiểu văn bản | Có kho tài liệu nhỏ và người xác nhận gợi ý đúng |
| #1 — Regression thủ công | Gần bối cảnh phần mềm; đo và lặp lại được trên ứng dụng demo | Có test case và kết quả mong đợi ổn định |
| #6 — Đồng bộ dữ liệu tuyển dụng | Dễ mô phỏng bằng bảng dữ liệu; giúp so sánh và thấy khi nào không cần AI | Có quy tắc ánh xạ, xử lý trùng và dữ liệu giả |

Nếu ưu tiên case có thời gian trước/sau theo một tác vụ rõ, có thể cân nhắc #5 thay #6, nhưng cần xác định bộ chứng từ và quy tắc nghiệp vụ. Không chọn chỉ vì số giờ tiết kiệm trong case lớn.

## Checklist nghiên cứu trước khi hoàn thiện bài nhóm

- [ ] Chọn vấn đề mà ít nhất một người hiểu quy trình hoặc tiếp cận được người dùng.
- [ ] Kiểm chứng người dùng theo Phase 4, ghi cả tín hiệu phản bác và điều nhóm đã sửa.
- [ ] Tìm thêm giải pháp để đủ 2–3 tools/patterns; cân nhắc công cụ sẵn có, quy trình chuẩn và cách không dùng AI.
- [ ] Xác định dữ liệu được phép dùng, input/output và owner cho từng bước.
- [ ] Đo baseline của phạm vi pilot; không lấy số của doanh nghiệp lớn làm số của nhóm.
- [ ] Tách thời gian xử lý của máy khỏi tổng công người, gồm kiểm tra, sửa và bảo trì.
- [ ] So sánh chất lượng trước/sau, không chỉ tốc độ.
- [ ] Ghi rõ phần nguồn, phần suy luận và phần chưa biết.
- [ ] Chốt quyết định sau validation; pilot giả lập chưa chứng minh sẵn sàng vận hành thật.
