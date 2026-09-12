# 02 — Group Problem Statement (Bản nộp nhóm)

> Làm chung 1 bản, mỗi thành viên copy vào repo cá nhân. Đi theo Phase 3 → 6 trong `01-worksheet.md`. Nhóm chỉ chọn **candidate problem** ở Phase 3, viết Problem Statement sau khi validate + vẽ workflow.

## Thành viên nhóm

| STT | Họ và tên | Mã học viên | Vai trò trong nhóm (VD: facilitator, workflow, research, writer) |
|-----|-----------|-------------|---------------------------------------------------------------|
| 1   | Nguyễn Văn Huy | 2A202602428 |                          writer, research                       |
| 2   | Hoàng Thái Đạt | 2A202602959 |                         research, facilitator                   |
| 3   | Nguyễn Trọng Phúc | 2A202602552 |                      research, workflow                      |
| 4   | Nguyễn Quốc Đạt | 2A202602369 |                        research, workflow                       |
| 5   | Nguyễn Việt Hùng | 2A202602972 |                       research,facilitator                     |

**Candidate problem nhóm chọn (1 câu):**

Tài xế Xanh SM và chủ sở hữu xe điện VinFast gặp khó khăn trong việc duy trì lựa chọn trạm sạc phù hợp khi mức pin, giao thông và trạng thái trụ thay đổi trong lúc di chuyển, đặc biệt khi nhiều xe cùng có nhu cầu sạc.

---

## Phase 3 — Group Convergence: từ 9-12 candidates về 1

### 3.1. Trình bày top 3 mỗi người (mỗi candidate 1-2 phút)

| # | Người đưa ra | Candidate problem | Người gặp vấn đề | Điểm nghẽn | Cảm nhận nhanh của nhóm |
|---|---|---|---|---|---|
| 1 | Nguyễn Văn Huy | Điều chuyển hàng giữa các cửa hàng khi một chi nhánh sắp thiếu hàng | Nhân viên vận hành chuỗi, quản lý cửa hàng | Phải kiểm tra tồn nhiều chi nhánh, tốc độ bán, safety stock và khoảng cách trước khi chọn cửa hàng nguồn và số lượng điều chuyển | Cùng bối cảnh vận hành chuỗi; workflow rõ, impact dễ đo; có thể benchmark Rule trước Workflow/AI |
| 2 | Nguyễn Văn Huy | Đề xuất lượng bổ sung tồn kho cho từng cửa hàng | Nhân viên vận hành / merchandise planner, quản lý cửa hàng | Khó xác định lượng replenishment phù hợp vì nhu cầu khác nhau theo SKU, cửa hàng, ngày và chương trình khuyến mãi | Cùng domain inventory; phù hợp so sánh min/max, moving average với forecasting/AI; cần dữ liệu lịch sử đủ tốt |
| 3 | Nguyễn Văn Huy | Phát hiện và tìm nguyên nhân chênh lệch tồn kho | Nhân viên kho, quản lý cửa hàng, vận hành | Khi tồn thực tế lệch hệ thống phải lần lại giao dịch bán, nhập, trả và điều chuyển để tìm nguyên nhân | Bottleneck/output rõ; Rule reconciliation xử lý case rõ ràng, AI có thể hỗ trợ case khó |
| 4 | Hoàng Thái Đạt | Đối soát các giao dịch online | Nhân viên kế toán | Phải thu thập và đối chiếu nhiều giao dịch thủ công | Có nhu cầu thực tế nhưng cần làm rõ workflow, baseline và khác biệt với công cụ hiện có |
| 5 | Hoàng Thái Đạt | Tìm kiếm và xuất video gói hàng | Chủ shop bán hàng online | Khó tìm lại đúng video gói hàng khi cần đối soát/khiếu nại | Có nhu cầu nhưng cần xác định dữ liệu video, mapping với đơn hàng và tần suất xảy ra |
| 6 | Hoàng Thái Đạt | Check quy hoạch tính pháp lý của sổ đỏ | Người mua bán / nhân viên BĐS | Phải tra cứu nhiều nguồn và đối chiếu thông tin pháp lý | Giá trị cao nhưng rủi ro pháp lý lớn; AI chỉ nên hỗ trợ, không tự quyết định |
| 7 | Nguyễn Trọng Phúc | App VinFast khó tìm trạm sạc phù hợp, dữ liệu thay đổi theo thời gian và điều phối xe chưa tốt | Tài xế Xanh SM, chủ sở hữu xe VinFast | Quyết định chọn trạm có thể mất hiệu lực khi giao thông, mức pin hoặc trạng thái trụ thay đổi | Pain trực tiếp với người dùng cuối; cần kiểm chứng tính năng hiện tại, dữ liệu real-time và API |
| 8 | Nguyễn Trọng Phúc | Team QA Xanh SM phải nghe ghi âm hủy chuyến và note tài xế thủ công để phân loại lý do | Team QA Xanh SM | Điểm nghẽn ở bước nghe ghi âm và phân loại thủ công, khiến insight chậm | Workflow và metric rõ; cần Speech-to-Text tiếng Việt đủ tốt |
| 9 | Nguyễn Trọng Phúc | CSKH VinFast phải phân tích thủ công lỗi từ mô tả tiếng Việt của khách | CSKH VinFast | Phải hiểu mô tả sai chính tả/thiếu ý rồi phân loại trước khi xử lý | Khả thi với NLP/LLM nhưng tác động chủ yếu nội bộ |
| 10 | Nguyễn Quốc Đạt | Hiểu một task mới từ nhiều Slack thread, ticket và tài liệu | Developer | Mất thời gian gom nhiều nguồn để hiểu đủ context trước khi bắt đầu | Actor và bottleneck rõ; cần định nghĩa “hiểu đủ” và baseline |
| 11 | Nguyễn Quốc Đạt | Tìm người phụ trách đúng việc khi task bị vướng | Developer / thành viên nhóm | Không biết đúng owner nên bị chuyển tiếp nhiều lần | Có thể đo số lần chuyển tiếp và thời gian chờ; cần owner list chuẩn |
| 12 | Nguyễn Việt Hùng | Tìm nguyên nhân và sửa lỗi trong hệ thống | Developer | Phải đọc code, log và thử nhiều hướng để tìm root cause | Xảy ra thường xuyên nhưng cần thu hẹp loại bug để metric rõ |

### 3.2. Gom trùng / cluster (gom 9-12 ý thành 3-4 cụm)

| Cluster | Candidates included | Pattern chung | Ghi chú |
|---|---|---|---|
| A | Nguyễn Văn Huy: điều chuyển hàng, bổ sung tồn kho, điều tra chênh lệch tồn | Vận hành tồn kho trong chuỗi cửa hàng: phát hiện thiếu/dư → quyết định bổ sung/điều chuyển → đối soát | Ba candidate của Huy cùng một bối cảnh retail operations; phù hợp so sánh Rule, Workflow và AI hỗ trợ dự báo/ranking |
| B | Hoàng Thái Đạt: đối soát giao dịch online, tìm video gói hàng, kiểm tra pháp lý | Thu thập dữ liệu từ nhiều nguồn → đối chiếu → kiểm tra → đưa ra kết quả | Có thể dùng Rule/Workflow; bài pháp lý có rủi ro cao và cần human review |
| C | Nguyễn Quốc Đạt, Nguyễn Việt Hùng | Developer mất thời gian tìm context, owner hoặc nguyên nhân lỗi trước khi tiếp tục công việc | Có thể dùng Search/RAG hoặc Workflow hỗ trợ; cần thu hẹp nguồn dữ liệu và đo baseline |
| D (nếu có) | Nguyễn Trọng Phúc | Các vấn đề trong hệ sinh thái VinFast/Xanh SM liên quan vận hành và trải nghiệm khách hàng | Candidate trạm sạc tác động trực tiếp người dùng; candidate QA có workflow/metric rõ; candidate CSKH khả thi nhưng thiên về nội bộ |

### 3.3. Shortlist (giữ 2-3 bài trả lời được 7 câu hỏi worksheet)

| Candidate | Vì sao vào shortlist (2-3 ý) | Rủi ro / điều chưa rõ |
|---|---|---|
| Điều phối lựa chọn trạm sạc VinFast/Xanh SM theo pin, giao thông và trạng thái trụ thay đổi | Tác động trực tiếp người dùng; workflow có nhiều tín hiệu động; có thể so sánh Rule/Workflow/Agent | Chưa có validation thật; chưa rõ API/dữ liệu real-time; cần kiểm chứng chức năng hiện có của VinFast |
| Phân loại lý do hủy chuyến Xanh SM từ ghi âm | Workflow rõ; bottleneck rõ; dễ đo thời gian/case và accuracy | Cần Speech-to-Text tiếng Việt tốt; cần dữ liệu ghi âm và ground truth |
| Phân tích lỗi CSKH VinFast từ mô tả tiếng Việt | Actor/output rõ; có thể đo accuracy; phù hợp NLP/LLM | Tác động chủ yếu nội bộ; cần taxonomy lỗi và dữ liệu gán nhãn |

### 3.4. Score để đồng thuận (chấm 1-5, ép nói rõ vì sao cho 5 / cho 3)

| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A được | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Điều phối lựa chọn trạm sạc VinFast/Xanh SM | 5 | 4 | 2 | 5 | 3 | 5 | 4 | 28 |
| Phân loại lý do hủy chuyến từ ghi âm | 5 | 5 | 3 | 4 | 5 | 4 | 4 | 30 |
| Phân tích lỗi CSKH từ mô tả tiếng Việt | 5 | 4 | 2 | 3 | 4 | 4 | 4 | 26 |

**Candidate nhóm chọn (1 bài duy nhất):**

```text
Điều phối lựa chọn trạm sạc cho tài xế Xanh SM/chủ xe VinFast dựa trên mức pin,
quãng đường, giao thông và trạng thái trụ thay đổi theo thời gian.
```

**Vì sao chọn (4-5 câu):**

```text
Nhóm chọn candidate này vì pain tác động trực tiếp đến người dùng cuối thay vì chỉ tối ưu một workflow nội bộ.
Bài toán có nhiều yếu tố động như mức pin, quãng đường, giao thông và trạng thái trụ nên có giá trị để so sánh Rule, Workflow và Agent.
Trong thảo luận, nhóm còn phát hiện vấn đề xung đột khi nhiều xe cùng được hướng dẫn đến một trụ và khi một xe khác đến sử dụng trụ trước.
Điều này khiến bài toán không chỉ là “tìm trạm gần nhất” mà trở thành bài toán duy trì lựa chọn phù hợp theo thời gian.
Tuy nhiên, nhóm chưa coi đây là pain đã được chứng minh cho đến khi có validation thật.
```

**Vì sao KHÔNG chọn các candidate còn lại (mỗi bài 2-3 câu):**

```text
Candidate phân loại lý do hủy chuyến có workflow và metric rõ, thậm chí dễ làm lab hơn, nhưng chủ yếu tối ưu quy trình nội bộ QA.
Nhóm ưu tiên bài toán có tác động trực tiếp đến tài xế/chủ xe và có nhiều yếu tố quyết định động hơn.

Candidate phân tích lỗi CSKH khả thi với NLP/LLM và có thể đo accuracy, nhưng tác động vẫn chủ yếu nằm trong quy trình CSKH.
So với bài toán trạm sạc, nhóm đánh giá phạm vi trải nghiệm người dùng trực tiếp hẹp hơn.
```

**Disagreement (nếu có — ai lo gì, chốt ra sao):**

```text
Ban đầu nhóm chỉ nghĩ đến việc chỉ đường dựa trên lượng pin còn lại và quãng đường tới trạm.
Sau đó nhóm bổ sung điều kiện giao thông và trạng thái trụ sạc theo thời gian thực, vì trạm gần nhất chưa chắc là lựa chọn phù hợp nếu tắc đường hoặc trụ bị sử dụng trong lúc xe đang di chuyển.
Một thành viên đặt vấn đề: nếu hệ thống hướng dẫn hai xe cùng đến một trụ thì xử lý thế nào? Từ đó nhóm mở rộng bài toán sang điều phối real-time dựa trên pin, giao thông và trạng thái trụ.
Một thành viên khác phản biện rằng dù hệ thống đã phân bổ, một xe khác vẫn có thể tự đến sử dụng trụ trước, làm mất chỗ và khiến các hướng dẫn hiện tại phải thay đổi.
Nhóm vì vậy đề xuất cơ chế ưu tiên: xe có pin thấp được ưu tiên các trạm gần, phù hợp và ít bị đổi lộ trình; mức ưu tiên giảm dần khi lượng pin cao hơn.
Cách tính cụ thể giữa pin, độ ưu tiên, quãng đường, traffic và trạng thái trụ chưa được chốt, nên tạm mô tả dưới dạng Priority = f(pin, khoảng cách, ETA, traffic, trạng thái trụ).
```

---

## Phase 4 — Quick Validation + Research

### 4.1. Quick validation (scenario giả định để hoàn thiện bài lab)

> **Lưu ý:** Phần validation dưới đây là **tình huống giả định**, không phải interview/survey đã thực hiện ngoài thực tế. Nhóm dùng scenario này để mô phỏng cách evidence có thể làm thay đổi problem framing.

| Nguồn | Số người / mẫu | Tín hiệu xác nhận (kèm quote nguyên văn trong scenario giả định) | Tín hiệu phản bác | Nhóm sửa problem thế nào |
|---|---:|---|---|---|
| Interview | 3 người dùng xe điện VinFast (giả định: 2 tài xế chạy dịch vụ, 1 chủ xe cá nhân) | 2/3 người cho biết họ thường kiểm tra lại trạm khi pin thấp hoặc hành trình dài. Quote giả định: “Lúc xuất phát thấy trạm còn chỗ nhưng đi gần tới thì tình trạng có thể khác, lúc pin thấp tôi ngại nhất là phải đổi sang trạm khác.” | 1/3 người nói thường sạc ở các trạm quen và ít gặp tình huống phải đổi trạm: “Tôi chủ yếu đi tuyến cố định nên thường biết trước chỗ sạc, không phải lần nào cũng cần hệ thống chọn lại.” | Không mô tả pain là “khó tìm trạm sạc” cho mọi người dùng. Thu hẹp vào các hành trình mà mức pin thấp, tuyến không quen hoặc trạng thái trạm thay đổi trong lúc di chuyển. |
| Survey / poll | 8 người dùng xe điện (giả định) | 5/8 từng ít nhất một lần phải kiểm tra lại hoặc cân nhắc trạm khác trong hành trình; 4/8 cho rằng mức pin còn lại và khả năng có chỗ sạc quan trọng hơn việc chỉ chọn trạm gần nhất | 3/8 cho biết tính năng tìm trạm/chỉ đường hiện tại đã đủ cho phần lớn nhu cầu; 2/8 ưu tiên tự chọn trạm quen thay vì nhận đề xuất tự động | Chuyển mục tiêu từ “AI tự chọn trạm tốt nhất” sang “hệ thống hỗ trợ phát hiện khi phương án hiện tại không còn phù hợp và đề xuất lại có giải thích”. |
| Scenario log | 10 hành trình mô phỏng | Trong 4/10 scenario, phương án chọn ở t0 trở nên kém phù hợp tại t1 do traffic tăng, trụ chuyển sang bận hoặc pin tiêu hao nhanh hơn giả định | 6/10 scenario không cần re-route; nếu hệ thống liên tục tính lại sẽ tạo thêm nhiễu và route churn không cần thiết | Chỉ re-score/re-route khi thay đổi vượt ngưỡng; ưu tiên giữ route ổn định, đặc biệt với xe pin thấp. |

**Insight sau validation (scenario giả định — pain thật nằm ở đâu):**

```text
Pain không nằm chủ yếu ở việc “không tìm được trạm sạc”, vì ứng dụng hiện tại đã hỗ trợ tìm trạm và chỉ đường.
Pain đáng kiểm tra hơn là việc một lựa chọn hợp lý tại t0 có thể trở nên kém phù hợp tại t1 khi pin, traffic hoặc trạng thái trụ thay đổi.
Nhóm vì vậy thu hẹp problem sang hỗ trợ re-evaluate/re-route có điều kiện, thay vì xây một charging assistant tổng quát.
```

Bằng chứng đính kèm: trong bài lab hiện dùng **scenario giả định**; nếu triển khai thật phải thay bằng interview notes/survey/log thật.

---|---:|---|---|---|
| Interview | Chưa thực hiện | Chưa có quote thật | Chưa có | Chưa sửa chính thức; cần phỏng vấn tài xế/chủ xe về lần gần nhất phải đổi hoặc kiểm tra lại trạm sạc |
| Survey / poll | Chưa thực hiện | Chưa có | Chưa có | Có thể dùng làm phương án dự phòng nếu không đủ người interview |
| Log / ticket / review (nếu có) | Chưa có quyền truy cập xác nhận | Chưa có | Chưa có | Chỉ dùng nếu nhóm có nguồn hợp lệ và được phép truy cập |

**Insight sau validation (1-2 câu — pain thật nằm ở đâu):**

```text
Hiện chưa có validation người dùng nên chưa thể kết luận pain thật.
Giả thuyết hiện tại là pain nằm ở việc duy trì lựa chọn trạm phù hợp khi điều kiện thay đổi, chứ không chỉ ở việc tìm trạm ban đầu.
```

Bằng chứng đính kèm (nếu có): `02-group-problem-statement-survey.png`, `...-interview-notes.md`

### 4.2. Research giải pháp đã có (nguồn chính thức, link kiểm được)

| Nguồn / tool / case | Link | Họ giải quyết bước nào? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| VinFast – tính năng Pin và Sạc trên ứng dụng | https://vinfastauto.com/vn_vi/su-dung-tinh-nang-lien-quan-den-pin-tren-ung-dung-vinfast | Theo dõi mức pin; tìm trạm gần; xem đầu sạc khả dụng, thời gian/quãng đường và pin dự kiến khi đến; hỗ trợ “Đặt chỗ” hoặc “Chỉ đường” | Đã giải quyết phần lớn bài toán tìm và đánh giá trạm cơ bản | Không thể từ tài liệu này kết luận rằng mọi thay đổi trong hành trình hoặc bài toán ưu tiên nhiều xe đều đã được xử lý | Không build lại chức năng tìm trạm; tập trung vào trigger re-evaluation và cách ranking khi trạng thái thay đổi |
| VinFast – hướng dẫn sạc và tìm trạm | https://vinfastauto.com/vn_vi/huong-dan-sac-pin-o-to-dien-vinfast | Liệt kê trạm khả dụng/gần xe; cho xem số lượng trụ, khoảng cách, thời gian tiếp cận và chỉ đường | Workflow hiện tại rõ, giúp nhóm xác định baseline thực tế thay vì giả định app không có thông tin trạm | “Khả dụng” tại lúc xem chưa đồng nghĩa phương án chắc chắn vẫn phù hợp khi xe đến | Future workflow phải bổ sung giá trị ở bước theo dõi thay đổi, không phải thay thế toàn bộ workflow hiện tại |
| VinFast – FAQ ứng dụng cho ô tô | https://vinfastauto.com/vn_vi/cau-hoi-thuong-gap/cau-hoi-xe-o-to/san-pham/ung-dung-vinfast | Tìm trạm gần và đề xuất tuyến đường/danh sách trạm phù hợp trên hành trình | Xác nhận VinFast đã có route planning và station discovery | Làm yếu framing cũ “app khó tìm trạm”; cần evidence riêng nếu muốn khẳng định có pain về re-routing/coordination | Problem Statement phải mô tả khoảng trống động, không claim thiếu những chức năng đã tồn tại |
| VinFast – hướng dẫn sử dụng ứng dụng cho ô tô | https://vinfastauto.com/vn_vi/huong-dan-su-dung-ung-dung-vinfast | Bản đồ tìm trạm, gợi ý tuyến; hiển thị thời gian và mức pin còn lại khi tới trạm | Có dữ liệu liên quan trực tiếp tới quyết định chọn trạm | Chưa đủ bằng chứng công khai để khẳng định hệ thống có/không có cơ chế multi-vehicle priority như nhóm giả thuyết | Multi-vehicle coordination chỉ nên giữ là hypothesis cần validation, không trình bày như thiếu sót đã chứng minh |

**Research takeaway (2-3 câu — nên build gì / không build gì):**

```text
Research cho thấy VinFast đã có các chức năng nền tảng: theo dõi pin, tìm trạm khả dụng, xem khoảng cách/thời gian, ước tính pin khi đến, chỉ đường và trong một số luồng có đặt chỗ.
Vì vậy nhóm không nên build lại “AI tìm trạm sạc gần nhất”. Candidate hợp lý hơn là một Workflow hỗ trợ theo dõi thay đổi và chỉ re-score/re-route khi phương án hiện tại vượt ngưỡng rủi ro.
Cơ chế priority/multi-vehicle coordination vẫn là giả thuyết và chỉ nên đưa vào pilot nếu validation thật xác nhận nhu cầu.
```

> Phân biệt nguồn: **Quick Validation ở 4.1 là scenario giả định**; các link Research ở 4.2 là nguồn chính thức có thể kiểm tra.

---|---|---|---|---|---|
| VinFast – tính năng liên quan đến pin trên ứng dụng | https://vinfastauto.com/vn_vi/su-dung-tinh-nang-lien-quan-den-pin-tren-ung-dung-vinfast | Hiển thị pin, trạm gần, số đầu sạc khả dụng, khoảng cách/thời gian và pin dự kiến khi đến | Đã giải quyết một phần lớn bước tìm trạm và đánh giá khả năng đến trạm | Chưa đủ để kết luận xử lý tốt mọi thay đổi real-time hoặc xung đột nhiều xe | Không nên build lại chức năng tìm trạm cơ bản; cần tập trung vào khoảng trống động |
| VinFast – hướng dẫn sạc pin ô tô điện | https://vinfastauto.com/vn_vi/huong-dan-sac-pin-o-to-dien-vinfast-chi-tiet | Tìm trạm, xem thông tin và định tuyến đến trạm | Có route planning và thông tin trạm trong hệ sinh thái hiện tại | Cần kiểm chứng pain còn lại ngoài các chức năng đã có | Problem nên thu hẹp sang re-routing/điều phối khi điều kiện thay đổi |
| VinFast – FAQ/đặt chỗ trạm sạc | https://vinfastauto.com/vn_vi/cau-hoi-thuong-gap | Hỗ trợ đặt chỗ trạm sạc trong một số luồng | Có thể giảm xung đột khi nhiều xe cùng hướng tới trạm | Cần hiểu giới hạn reservation và trường hợp xe khác đến trước | Không được giả định “hai xe tranh một trụ” luôn chưa được xử lý |

**Research takeaway (2-3 câu — nên build gì / không build gì):**

```text
VinFast đã có các chức năng nền tảng như tìm trạm, xem trạng thái, định tuyến, ước lượng pin khi đến và đặt chỗ.
Vì vậy nhóm không nên build lại một charging assistant tổng quát; hướng có giá trị hơn là nghiên cứu điều phối/re-routing khi điều kiện thay đổi và cơ chế priority giữa nhiều xe, nếu validation xác nhận pain này thật sự tồn tại.
```

> Lưu ý: không dùng số liệu AI đưa nếu không verify được link chính thức. Ghi rõ giả định chưa chắc.

---

## Phase 5 — Workflow + Problem Statement

### 5.1. Current workflow bản nhóm

Dán workflow hoặc link file: `02-group-problem-statement-workflow.png/pdf/md`

```text
[1 Kiểm tra pin - người lái] → [2 Xem trạm sạc trên app] → [3 So sánh khoảng cách/traffic/trạng thái trụ]
→ [4 Chọn trạm - người lái] → [5 Di chuyển] → [6 Điều kiện thay đổi - bottleneck]
→ [7 Kiểm tra lại và đổi/giữ phương án]
```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú (handoff? bottleneck?) |
|---|---|---|---|---|---|
| 1 | Người lái | Mức pin hiện tại, điểm đến | Xác định có cần sạc hay không | Chưa đo | Cần validation workflow thực tế |
| 2 | Người lái + ứng dụng | Vị trí, danh sách trạm | Danh sách trạm có thể cân nhắc | Chưa đo | App hiện đã hỗ trợ tìm trạm |
| 3 | Người lái + ứng dụng | Khoảng cách, ETA, traffic, tình trạng trạm | So sánh các lựa chọn | Chưa đo | Một phần dữ liệu có thể thay đổi trong lúc di chuyển |
| 4 | Người lái | Các lựa chọn trạm | Trạm được chọn | Chưa đo | Human decision |
| 5 | Người lái | Route đã chọn | Xe di chuyển về trạm | Theo từng lần sạc | Trạng thái có thể thay đổi sau quyết định |
| 6 | Người lái + hệ thống | Traffic mới, pin mới, trạng thái trụ mới, xe khác đến trạm | Phương án cũ có thể mất hiệu lực | Không cố định | **Bottleneck:** quyết định ở t0 có thể không còn phù hợp ở t1 |
| 7 | Người lái | Danh sách/phương án cập nhật | Giữ route hoặc chọn trạm khác | Chưa đo | Có thể gây đổi route nhiều lần |

**Bottleneck chính (2-3 câu):**

```text
Bottleneck chính không nằm ở việc tìm một trạm trên bản đồ mà ở việc duy trì lựa chọn phù hợp khi trạng thái hệ thống thay đổi.
Một quyết định hợp lý tại thời điểm t0 có thể trở nên không phù hợp tại t1 vì traffic, mức pin, trạng thái trụ hoặc xe khác đến trước.
Đặc biệt, việc re-routing liên tục có thể bất lợi cho xe có pin thấp nên cần cơ chế priority và giới hạn đổi lộ trình.
```

### 5.2. Future workflow bản nhóm

Phải nhìn ra 5 thứ: bước nào máy (Rule), bước nào AI, bước nào người, boundary ở đâu, fallback khi AI sai.

```text
[1 Máy lấy pin + vị trí + traffic + trạng thái trụ]
→ [2 Rule loại các trạm không khả thi/an toàn]
→ [3 Workflow tính Priority Score và xếp hạng xe-trạm]
→ [4 AI hỗ trợ đánh giá các trade-off khi nhiều lựa chọn gần tương đương]
→ [5 Người lái review/xác nhận - boundary]
→ [6 Máy theo dõi thay đổi real-time]
→ [7 Nếu vượt ngưỡng thì re-score/re-route, ưu tiên hạn chế đổi route của xe pin thấp]

Fallback: nếu dữ liệu thiếu/trễ hoặc AI không chắc chắn, quay về Rule + danh sách trạm gốc và để người lái tự chọn.
```

**Before/after impact:**

| Metric | Trước | Sau kỳ vọng | Cách đo |
|---|---:|---:|---|
| Tổng thời gian | Chưa có baseline | Giảm thời gian phải tự so sánh/đổi trạm | Đo từ lúc mở luồng chọn trạm đến lúc xác nhận |
| Số bước | Khoảng 7 bước trong workflow giả thuyết | Giữ tương đương nhưng tự động hóa phần lọc/xếp hạng | Đếm bước trước/sau |
| Số bước thủ công | Người lái phải tự xem, so sánh, kiểm tra lại và đổi trạm | Giảm ở bước lọc, xếp hạng và theo dõi thay đổi | Quan sát pilot |
| Bottleneck chính | Phải tự đánh giá lại khi điều kiện thay đổi | Hệ thống tự phát hiện thay đổi và chỉ yêu cầu review khi cần | Đo số lần user phải tự kiểm tra lại |
| Risk mới | Chưa có | Dữ liệu sai/trễ, priority không công bằng, re-routing sai | Log lỗi, tỷ lệ override, tình huống rollback |

### 5.3. Problem Statement v0 (mỗi field 2-3 câu)

| Field | Nội dung |
|---|---|
| **Actor** | Tài xế Xanh SM và chủ sở hữu xe điện VinFast cần chọn điểm sạc trong hành trình. Họ là người chịu ảnh hưởng trực tiếp nếu lựa chọn trạm không còn phù hợp khi điều kiện thay đổi. |
| **Workflow** | Người lái kiểm tra pin → xem danh sách trạm → so sánh khoảng cách/traffic/trạng thái → chọn trạm → di chuyển → kiểm tra lại nếu điều kiện thay đổi. Hiện phần đánh giá lại và đổi phương án vẫn cần nhiều quyết định thủ công. |
| **Bottleneck** | Lựa chọn tại thời điểm t0 có thể mất hiệu lực ở t1 khi traffic, pin hoặc trạng thái trụ thay đổi. Khi nhiều xe cùng có nhu cầu, việc re-routing còn phải cân bằng mức pin, khoảng cách và mức ưu tiên của từng xe. |
| **Impact** | Có thể làm tăng thời gian ra quyết định, số lần đổi route và rủi ro xe pin thấp phải thay đổi phương án nhiều lần. Chưa có baseline thực tế nên chưa lượng hóa chính xác. |
| **Success Metric** | Thời gian chọn/đổi trạm; số lần phải re-route; tỷ lệ user override; tỷ lệ phương án vẫn hợp lệ khi xe gần đến trạm. Các metric cần baseline từ validation/pilot. |
| **Boundary** | Chỉ hỗ trợ lọc, xếp hạng, cập nhật và đề xuất trạm. Không tự điều khiển xe, không tự quyết định thay người lái và không cam kết giữ chỗ nếu hệ thống reservation không hỗ trợ. |

**Câu hỏi AI phản biện v0 (nếu có):**
- Field nào mơ hồ: Pain có thực sự nằm ở re-routing/điều phối hay đã được app/reservation hiện tại xử lý đủ tốt; chưa có baseline và validation người dùng.
- Tôi sửa gì: Thu hẹp từ “app khó tìm trạm” sang “duy trì lựa chọn trạm phù hợp khi điều kiện thay đổi và nhiều xe cạnh tranh tài nguyên”, đồng thời giữ đây là giả thuyết cho đến khi có validation.

---

## Phase 6 — Rule / Workflow / Agent + Decision

### 6.0. Ma trận độ phù hợp (suy nghĩ nhanh, không thay quyết định cuối)

- Độ mơ hồ: [ ] Thấp (có đúng/sai rõ) / [x] Cao (nhiều cách trả lời vẫn OK) — Vì sao: nhiều trạm có thể đều khả thi nhưng có trade-off khác nhau giữa pin, quãng đường, traffic và độ ổn định route.
- Độ phức tạp: [ ] Thấp (1-2 bước) / [x] Cao (3+ bước/nguồn, phụ thuộc nhau) — Vì sao: phải kết hợp nhiều nguồn dữ liệu và cập nhật quyết định khi trạng thái thay đổi.

**Bài toán nhóm nằm ở ô nào:**

```text
Mơ hồ cao + phức tạp cao.
```

**Vì sao (2-3 câu):**

```text
Không có một trạm duy nhất luôn là đáp án đúng vì lựa chọn phụ thuộc nhiều biến thay đổi theo thời gian.
Tuy nhiên, phần lớn luồng xử lý vẫn có thể mô tả trước bằng Rule + Workflow; độ phức tạp cao chưa đủ để kết luận bắt buộc phải dùng Agent.
```

### 6.1. So sánh Rule / Workflow / Agent (so trên cùng 1 bài)

| Mức | Phương án cho bài toán nhóm | Khi nào đủ | Rủi ro | Chọn? (Dùng cho bước nào?) |
|---|---|---|---|---|
| **Rule** | Loại trạm xe không đủ pin để đến; áp buffer pin; loại trạng thái không phù hợp; đặt ngưỡng priority cứng | Khi tiêu chí rõ và chỉ cần filter/ranking đơn giản | Cứng nhắc khi nhiều trade-off thay đổi | Có, dùng cho safety filter và điều kiện loại trừ |
| **Workflow** | Lấy dữ liệu → filter → tính priority → rank/phân bổ → user confirm → monitor → re-score khi cần | Khi các bước chính có thể xác định trước, dù có một số nhánh | Phụ thuộc data; workflow có thể phức tạp khi ngoại lệ tăng | **Chọn làm mức chính cho pilot** |
| **Agent** | Tự lập kế hoạch, gọi tool/API, quan sát thay đổi và quyết định hành động tiếp theo | Chỉ khi Workflow cố định không đủ và cần planning linh hoạt | Khó kiểm soát/debug; rủi ro cao nếu tự thay đổi route | Chưa chọn; chỉ cân nhắc sau pilot |

**5 câu hỏi chốt (trả lời câu đầy đủ):**
1. Rule có giải được 70-80% case không?  
   Chưa có dữ liệu để khẳng định tỷ lệ 70-80%, nhưng Rule có thể xử lý phần lớn điều kiện an toàn và loại trừ cơ bản như pin không đủ, trạm không khả dụng hoặc vượt ngưỡng khoảng cách.
2. Các bước có đi thẳng một đường không hay phải rẽ nhánh?  
   Luồng chính khá tuyến tính nhưng sẽ rẽ nhánh khi trạng thái trụ, giao thông hoặc mức pin thay đổi, hoặc khi Priority Score khiến hệ thống cần re-route.
3. Có thật sự cần Agent tự lập kế hoạch + gọi tool không?  
   Chưa. Workflow có khả năng gọi API, cập nhật dữ liệu và re-score theo điều kiện rõ ràng vẫn đủ cho pilot đầu tiên.
4. Nếu AI sai, ai phát hiện đầu tiên và sửa trong bao lâu?  
   Người lái là người review quyết định cuối cùng; hệ thống phải cho phép bỏ qua đề xuất ngay và quay về Rule + danh sách trạm gốc.
5. Có hạ được từ Agent → Workflow → Rule không?  
   Có. Nhóm nên bắt đầu bằng Workflow + Rule, chỉ nâng lên Agent nếu pilot chứng minh workflow cố định không xử lý được các trường hợp quan trọng.

**Mức chọn:**

```text
Workflow
```

**Vì sao chọn (3-4 câu):**

```text
Bài toán cần nhiều bước và nhiều nguồn dữ liệu, đồng thời phải cập nhật khi trạng thái thay đổi nên Rule thuần túy có thể quá cứng.
Tuy nhiên, luồng chính vẫn mô tả được trước: lấy dữ liệu → filter → tính priority → xếp hạng → user confirm → monitor → re-score.
Workflow vì vậy đủ linh hoạt cho pilot nhưng vẫn dễ test, debug và kiểm soát hơn Agent.
Rule vẫn được dùng bên trong Workflow cho các constraint an toàn và điều kiện loại trừ.
```

**Vì sao không chọn mức đơn giản hơn (2-3 câu):**

```text
Rule thuần túy có thể xử lý các điều kiện cứng nhưng khó cân bằng các trade-off động giữa pin, quãng đường, traffic, trạng thái trụ và độ ổn định route.
Dù vậy, nếu validation cho thấy pain thực tế đơn giản hơn giả thuyết hiện tại, nhóm nên hạ tiếp về Rule thay vì giữ Workflow một cách không cần thiết.
```

### 6.2. Problem Statement v1 (v0 sửa chặt hơn + 3 field cuối)

| Field | Nội dung |
|---|---|
| **Actor** | Tài xế Xanh SM và chủ sở hữu xe VinFast đang cần lựa chọn một trạm sạc trong hành trình thực tế. |
| **Workflow** | Người lái kiểm tra pin → xem các trạm → so sánh khoảng cách/ETA/traffic/trạng thái → chọn trạm → di chuyển → theo dõi thay đổi → giữ hoặc đổi phương án. |
| **Bottleneck** | Quyết định chọn trạm có thể mất hiệu lực khi điều kiện thay đổi; khi nhiều xe cùng có nhu cầu, re-routing phải cân bằng pin, khoảng cách, ETA, trạng thái trụ và độ ưu tiên. |
| **Impact** | Có thể tăng thời gian quyết định, số lần đổi route và khiến xe pin thấp phải thay đổi phương án nhiều lần. Mức độ ảnh hưởng chưa được lượng hóa vì chưa có baseline thật. |
| **Success Metric** | Giảm thời gian chọn/đổi trạm; giảm số lần re-route không cần thiết; giảm tỷ lệ user override; tăng tỷ lệ lựa chọn vẫn hợp lệ khi gần đến trạm. |
| **Boundary** (làm / không làm) | Làm: lọc, xếp hạng, tính priority, theo dõi thay đổi và đề xuất re-route. Không làm: tự lái, tự quyết định thay người lái, cam kết giữ chỗ ngoài hệ thống reservation hoặc bỏ qua constraint an toàn. |
| **AI intervention point** (can thiệp sau bước nào, trước bước nào) | Sau bước Rule loại các trạm không khả thi/an toàn và trước bước người lái xác nhận lựa chọn cuối; AI chỉ hỗ trợ khi cần đánh giá trade-off giữa nhiều lựa chọn gần tương đương. |
| **Mức chọn** (Rule / Workflow / Agent + 1 câu vì sao) | Workflow — vì bài toán có nhiều bước và cần cập nhật trạng thái, nhưng vẫn có thể thiết kế luồng xử lý xác định trước mà chưa cần Agent tự lập kế hoạch. |
| **Rủi ro & người thật kiểm tra** (rủi ro lớn nhất + ai kiểm tra bằng cách nào) | Rủi ro lớn nhất là dữ liệu pin/trạm/traffic sai hoặc trễ dẫn đến re-route không phù hợp. Người lái phải nhìn thấy dữ liệu và lý do đề xuất, đồng thời có quyền override ngay. |

### 6.3. Final decision

| Câu hỏi | Yes / Not Yet / No | Ghi chú (câu đầy đủ) |
|---|---|---|
| Actor + workflow rõ chưa? | Yes | Actor và workflow đã mô tả được tương đối rõ từ thảo luận nhóm và research. |
| Baseline + metric đo được chưa? | Not Yet | Metric đã xác định nhưng chưa có baseline từ interview, survey hoặc log. |
| Data/input đủ dùng chưa? | Not Yet | Chưa xác nhận quyền truy cập và độ real-time của pin, traffic, trạng thái trụ/reservation. |
| AI sai, hậu quả chấp nhận được không? | Not Yet | Có thể giảm rủi ro bằng Rule + human confirmation, nhưng cần test pilot trước. |
| Có người review/owner không? | Yes | Người lái là người xác nhận quyết định cuối; owner kỹ thuật của data/API vẫn cần xác định. |
| Có cách non-AI đơn giản hơn không? | Yes | Rule + Workflow deterministic phải được thử trước khi cân nhắc Agent. |

**Decision:**

```text
Not Yet
```

**Lý do (3-4 câu dựa trên bằng chứng):**

```text
Nhóm đã xác định được candidate, workflow giả thuyết và hướng giải pháp phù hợp để so sánh Rule/Workflow/Agent.
Tuy nhiên, chưa có interview/survey/log để chứng minh pain, chưa có baseline và chưa xác nhận quyền truy cập dữ liệu cần thiết.
Research còn cho thấy VinFast đã có nhiều chức năng tìm trạm, định tuyến, ước lượng pin và đặt chỗ, nên nhóm phải kiểm chứng chính xác khoảng trống còn tồn tại.
Vì vậy quyết định hiện tại là Not Yet thay vì Go.
```

**Nếu Go — pilot nhỏ nhất (data nào, chạy tay ra sao, đo 3 số nào):**

```text
Sau khi validation đủ: dùng một tập nhỏ hành trình + trạm với dữ liệu được phép sử dụng; chạy Workflow + Rule ở quy mô nhỏ.
Ba số cần đo: (1) thời gian chọn/đổi trạm, (2) số lần user override hoặc re-route, (3) tỷ lệ đề xuất còn hợp lệ khi xe gần đến trạm.
```

**Nếu Not Yet — cần validate gì trước:**

```text
(1) Interview 2-3 tài xế/chủ xe hoặc survey 5-10 người để xác nhận họ có thực sự phải kiểm tra lại/đổi trạm khi đang di chuyển hay không.
(2) Lấy quote thật về lần gần nhất họ gặp tình huống này và nguyên nhân cụ thể.
(3) Kiểm tra chính xác các tính năng hiện có của VinFast, đặc biệt route planning, trạng thái trụ và reservation.
(4) Xác minh khả năng truy cập dữ liệu pin, traffic, trạng thái trụ và độ trễ của dữ liệu.
(5) Đo baseline thời gian chọn/đổi trạm, số lần re-route và số lần user phải tự kiểm tra lại.
```

**Nếu No-Go — làm gì thay AI:**

```text
Dùng Rule + Workflow deterministic để lọc trạm theo phạm vi pin, trạng thái và khoảng cách; hiển thị thông tin minh bạch để người lái tự chọn.
```

**Exit / rollback (khi nào dừng AI, quay về cách cũ):**

```text
Dừng phần AI và quay về Rule + danh sách trạm gốc nếu dữ liệu đầu vào thiếu/trễ, tỷ lệ user override cao,
re-routing gây thay đổi lộ trình quá thường xuyên, hoặc pilot không chứng minh được cải thiện so với workflow hiện tại.
```

---

### Self-check nộp phần 02 (nhóm)
- [x] Có nhật ký hội tụ 9-12 → 1 (cluster + shortlist + score)
- [x] Có Quick Validation dạng scenario giả định + research bằng link chính thức kiểm được (cần thay quote giả định bằng quote thật nếu yêu cầu evidence thực tế)
- [x] Có workflow trước/sau đủ thời gian, handoff, bottleneck, boundary, fallback
- [x] Có PS v0 → v1, metric có trước/sau + cách đo, boundary có làm/không làm
- [x] Có so sánh Rule/Workflow/Agent + Decision Go/Not Yet/No-Go có lý do