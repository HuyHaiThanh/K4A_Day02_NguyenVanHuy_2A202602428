# 02 — Group Problem Statement (Bản nộp nhóm)

> Làm chung 1 bản, mỗi thành viên copy vào repo cá nhân. Đi theo Phase 3 → 6 trong `01-worksheet.md`. Nhóm chỉ chọn **candidate problem** ở Phase 3, viết Problem Statement sau khi validate + vẽ workflow.

## Thành viên nhóm

| STT | Họ và tên         | Mã học viên | Vai trò trong nhóm (VD: facilitator, workflow, research, writer) |
|-----|-------------------|-------------|------------------------------------------------------------------|
| 1   | Nguyễn Văn Huy    | 2A202602428 | writer, research                                                 |
| 2   | Hoàng Thái Đạt    | 2A202602959 | research, facilitator, writer                                    |
| 3   | Nguyễn Trọng Phúc | 2A202602552 | research, workflow                                               |
| 4   | Nguyễn Quốc Đạt   | 2A202602369 | research, workflow                                               |
| 5   | Nguyễn Việt Hùng  | 2A202602972 | research, facilitator                                            |

**Candidate problem nhóm chọn (1 câu):**

Tài xế Xanh SM và chủ sở hữu xe điện VinFast có thể phải đánh giá lại lựa chọn trạm sạc trong hành trình khi mức pin, điều kiện giao thông hoặc trạng thái trụ thay đổi so với thời điểm ban đầu.

------------------------------------------------------------------------

## Phase 3 — Group Convergence: từ 9-12 candidates về 1

### 3.1. Trình bày top 3 mỗi người (mỗi candidate 1-2 phút)

> Nhóm có 5 thành viên nên tổng cộng có 15 candidate (3 candidate/người); nhóm giữ nguyên cấu trúc của template và mở rộng số dòng để không bỏ candidate của thành viên nào.

| \#  | Người đưa ra      | Candidate problem                                                                               | Người gặp vấn đề                           | Điểm nghẽn                                                                                      | Cảm nhận nhanh của nhóm                                                                     |
|-----|-------------------|-------------------------------------------------------------------------------------------------|--------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| 1   | Nguyễn Văn Huy    | Điều chuyển hàng giữa các cửa hàng khi một chi nhánh sắp thiếu hàng                             | Nhân viên vận hành chuỗi, quản lý cửa hàng | Phải kiểm tra tồn nhiều chi nhánh, safety stock, tốc độ bán và khoảng cách trước khi chọn nguồn | Workflow rõ, impact đo được; nên benchmark Rule trước Workflow/AI                           |
| 2   | Nguyễn Văn Huy    | Đề xuất lượng bổ sung tồn kho cho từng cửa hàng                                                 | Nhân viên vận hành / merchandise planner   | Phải biến sales history, tồn kho và promotion thành lượng replenishment                         | Có metric rõ nhưng phụ thuộc chất lượng dữ liệu lịch sử                                     |
| 3   | Nguyễn Văn Huy    | Tìm nguyên nhân chênh lệch tồn kho                                                              | Nhân viên kho, quản lý cửa hàng            | Phải lần transaction bán/nhập/trả/điều chuyển để tìm nguyên nhân                                | Rule reconciliation có thể xử lý nhiều case; AI chỉ nên hỗ trợ case khó                     |
| 4   | Hoàng Thái Đạt    | Đối soát các giao dịch online                                                                   | Nhân viên kế toán                          | Phải thu thập và đối chiếu nhiều giao dịch thủ công                                             | Có nhu cầu thực tế nhưng cần làm rõ workflow, baseline và khác biệt với công cụ hiện có     |
| 5   | Hoàng Thái Đạt    | Tìm kiếm và xuất video gói hàng                                                                 | Chủ shop bán hàng online                   | Khó tìm lại đúng video gói hàng khi cần đối soát/khiếu nại                                      | Có nhu cầu nhưng cần xác định dữ liệu video, mapping với đơn hàng và tần suất xảy ra        |
| 6   | Hoàng Thái Đạt    | Check quy hoạch tính pháp lý của sổ đỏ                                                          | Người mua bán / nhân viên BĐS              | Phải tra cứu nhiều nguồn và đối chiếu thông tin pháp lý                                         | Giá trị cao nhưng rủi ro pháp lý lớn; AI chỉ nên hỗ trợ, không tự quyết định                |
| 7   | Nguyễn Trọng Phúc | App VinFast khó duy trì lựa chọn trạm sạc phù hợp khi dữ liệu thay đổi và điều phối xe chưa tốt | Tài xế Xanh SM, chủ sở hữu xe VinFast      | Quyết định chọn trạm có thể mất hiệu lực khi giao thông, mức pin hoặc trạng thái trụ thay đổi   | Pain trực tiếp người dùng cuối; cần kiểm chứng tính năng hiện tại, dữ liệu real-time và API |
| 8   | Nguyễn Trọng Phúc | Team QA Xanh SM phải nghe ghi âm hủy chuyến và note tài xế thủ công để phân loại lý do          | Team QA Xanh SM                            | Nghe ghi âm và phân loại thủ công khiến insight chậm                                            | Workflow và metric rõ; cần Speech-to-Text tiếng Việt đủ tốt                                 |
| 9   | Nguyễn Trọng Phúc | CSKH VinFast phải phân tích thủ công lỗi từ mô tả tiếng Việt của khách                          | CSKH VinFast                               | Phải hiểu mô tả sai chính tả/thiếu ý rồi phân loại trước khi xử lý                              | Khả thi với NLP/LLM nhưng tác động chủ yếu nội bộ                                           |
| 10  | Nguyễn Quốc Đạt   | Hiểu một task mới từ nhiều Slack thread, ticket và tài liệu                                     | Developer                                  | Mất thời gian gom nhiều nguồn để hiểu đủ context trước khi bắt đầu                              | Actor và bottleneck rõ; cần định nghĩa “hiểu đủ” và baseline                                |
| 11  | Nguyễn Quốc Đạt   | Tìm người phụ trách đúng việc khi task bị vướng                                                 | Developer / thành viên nhóm                | Không biết đúng owner nên bị chuyển tiếp nhiều lần                                              | Có thể đo số lần chuyển tiếp và thời gian chờ; cần owner list chuẩn                         |
| 12  | Nguyễn Quốc Đạt   | Viết weekly update bằng cách gom thông tin thủ công                                             | Developer / thành viên nhóm                | Phải tổng hợp tiến độ từ nhiều nguồn rồi viết lại theo format báo cáo                           | Workflow lặp lại, output rõ; có thể benchmark template/Rule trước AI                        |
| 13  | Nguyễn Việt Hùng  | Tìm nguyên nhân và sửa lỗi trong hệ thống                                                       | Developer                                  | Phải đọc code, log và thử nhiều hướng để tìm root cause                                         | Xảy ra thường xuyên nhưng cần thu hẹp loại bug để metric rõ                                 |
| 14  | Nguyễn Việt Hùng  | Viết và kiểm thử test case cho chức năng mới                                                    | Developer / QA                             | Phải tự xác định coverage, case biên và chạy kiểm tra                                           | Lặp lại nhưng cần baseline về effort và chất lượng test                                     |
| 15  | Nguyễn Việt Hùng  | Tra cứu code, cú pháp và cách sử dụng API                                                       | Developer                                  | Mất thời gian tìm đúng tài liệu và context kỹ thuật                                             | Phù hợp knowledge search; cần giới hạn nguồn và đo search time                              |

### 3.2. Gom trùng / cluster (gom 9-12 ý thành 3-4 cụm)

| Cluster    | Candidates included    | Pattern chung                                                                                           | Ghi chú                                                                   |
|------------|------------------------|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| A          | 1, 2, 3                | Vận hành tồn kho chuỗi: phát hiện thiếu/dư → quyết định replenishment/điều chuyển → đối soát chênh lệch | Cùng một retail context; có thể benchmark Rule với Workflow               |
| B          | 10, 11, 12, 13, 14, 15 | Developer mất thời gian tìm context, owner, viết update, tìm root cause, test case hoặc tài liệu/API    | Phù hợp Search/RAG/Workflow nhưng cần thu hẹp scope cho từng candidate    |
| C          | 4, 5, 6                | Thu thập/đọc dữ liệu → đối chiếu → kiểm tra theo rule → đưa ra kết quả                                  | Có thể dùng Rule/Workflow; bài pháp lý cần human review                   |
| D (nếu có) | 7, 8, 9                | Các vấn đề trong hệ sinh thái VinFast/Xanh SM liên quan vận hành và trải nghiệm khách hàng              | Candidate trạm sạc tác động trực tiếp user; QA/CSKH có workflow nội bộ rõ |

### 3.3. Shortlist (giữ 2-3 bài trả lời được 7 câu hỏi worksheet)

| Candidate                                                                                | Vì sao vào shortlist (2-3 ý)                                                         | Rủi ro / điều chưa rõ                                                                  |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| Duy trì lựa chọn trạm sạc VinFast/Xanh SM khi pin, giao thông và trạng thái trụ thay đổi | Tác động trực tiếp người dùng; nhiều tín hiệu động; so sánh được Rule/Workflow/Agent | Chưa rõ API/data freshness; phải phân biệt với tính năng tìm trạm/route planning đã có |
| Phân loại lý do hủy chuyến Xanh SM từ ghi âm                                             | Workflow/bottleneck rõ; đo được thời gian/case và accuracy                           | Cần Speech-to-Text tiếng Việt tốt; cần audio và ground truth                           |
| Phân tích lỗi CSKH VinFast từ mô tả tiếng Việt                                           | Actor/output rõ; có thể đo accuracy; phù hợp NLP/LLM                                 | Tác động chủ yếu nội bộ; cần taxonomy lỗi và dữ liệu gán nhãn                          |

### 3.4. Score để đồng thuận (chấm 1-5, ép nói rõ vì sao cho 5 / cho 3)

| Candidate                                   | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A được | Nhóm hiểu domain | Tổng |
|---------------------------------------------|---------:|------------:|-----------------:|---------------:|--------------:|-------------------:|-----------------:|-----:|
| Điều phối lựa chọn trạm sạc VinFast/Xanh SM |        5 |           4 |                5 |              5 |             3 |                  5 |                4 |   31 |
| Phân loại lý do hủy chuyến từ ghi âm        |        3 |           5 |                3 |              4 |             3 |                  4 |                4 |   26 |
| Phân tích lỗi CSKH từ mô tả tiếng Việt      |        4 |           4 |                2 |              3 |             4 |                  4 |                4 |   25 |

**Candidate nhóm chọn (1 bài duy nhất):**

``` text
Tài xế Xanh SM/chủ xe VinFast có thể phải đánh giá lại lựa chọn trạm sạc trong hành trình
khi mức pin, giao thông hoặc trạng thái trụ thay đổi so với thời điểm lựa chọn ban đầu.
```

**Vì sao chọn (4-5 câu):**

``` text
Candidate này có điểm hội tụ cao nhất ở Phase 3 và tác động trực tiếp đến trải nghiệm người dùng cuối. Điểm số phản ánh đánh giá tại thời điểm hội tụ; các phase sau vẫn dùng validation/research để kiểm tra lại mức chắc chắn của từng giả định.
Bài toán có nhiều tín hiệu thay đổi theo thời gian như mức pin, ETA và trạng thái trụ nên phù hợp để so sánh Rule, Workflow và Agent.
Nhóm cũng nhận thấy có thể phát sinh xung đột khi nhiều xe cùng hướng tới nguồn lực sạc hữu hạn.
Vì vậy nhóm chọn candidate này để tiếp tục validation và research, đồng thời chưa xem các giả thuyết về điều phối real-time hoặc ưu tiên xe pin thấp là kết luận cuối cùng.
Các giả thuyết đó chỉ được giữ lại nếu evidence ở các phase sau đủ mạnh.
```

**Vì sao KHÔNG chọn các candidate còn lại (mỗi bài 2-3 câu):**

``` text
Phân loại lý do hủy chuyến có workflow và metric rõ, thậm chí dễ pilot hơn, nhưng tác động chính nằm trong quy trình QA nội bộ.
Nhóm ưu tiên candidate có tác động trực tiếp tới trải nghiệm tài xế/chủ xe và có nhiều signal động hơn.

Phân tích lỗi CSKH phù hợp NLP/LLM và có thể đo accuracy, nhưng tác động chủ yếu là tối ưu quy trình nội bộ.
Nhóm cũng hiểu domain này ít hơn candidate trạm sạc.
```

**Disagreement (nếu có — ai lo gì, chốt ra sao):**

``` text
Ban đầu, nhóm xem bài toán chủ yếu là chỉ đường đến trạm sạc dựa trên mức pin còn lại và quãng đường tới trạm.
Sau đó nhóm nhận ra khoảng cách ngắn nhất chưa chắc là lựa chọn phù hợp nếu điều kiện giao thông thay đổi hoặc trạng thái trụ thay đổi theo thời gian thực; ví dụ một trạm chỉ cách 5 km nhưng tuyến đường đang tắc hoặc trụ vừa được người khác sử dụng.

Từ đó, nhóm mở rộng bài toán sang việc cập nhật và điều phối lựa chọn trạm theo mức pin, giao thông và trạng thái trụ.
Một phản biện tiếp theo được đặt ra: nếu hai xe cùng được hệ thống hướng dẫn đến một trụ thì có thể xảy ra xung đột tài nguyên.

Nhóm sau đó cân nhắc cơ chế ưu tiên, trong đó xe có mức pin thấp hơn được ưu tiên các trạm gần, an toàn và ít phải thay đổi lộ trình.
Tuy nhiên, một thành viên tiếp tục phản biện rằng người dùng ngoài hệ thống vẫn có thể tự đến trạm và sử dụng trước, làm trạng thái thay đổi và khiến các hướng dẫn hiện tại phải được tính lại.

Vì vậy, nhóm chốt rằng solution không thể chỉ là một lần “chọn trạm tối ưu”, mà cần monitor và re-evaluate theo thời gian.
Cơ chế priority theo pin, quãng đường, ETA, giao thông và trạng thái trụ được giữ như một hypothesis cần kiểm chứng thêm, chưa được xem là policy cuối cùng.
```

------------------------------------------------------------------------

## Phase 4 — Quick Validation + Research

### 4.1. Quick validation (ít nhất 1 cách: interview 2-3 người hoặc survey 5-10 người)

| Nguồn                          |           Số người / mẫu | Tín hiệu xác nhận (kèm quote nguyên văn)                                                                                                                          | Tín hiệu phản bác                                                                              | Nhóm sửa problem thế nào                                                                                                        |
|--------------------------------|-------------------------:|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Interview                      |           Chưa thực hiện | Chưa có                                                                                                                                                           | Chưa có                                                                                        | Không dùng interview để suy rộng                                                                                                |
| Survey / poll                  |                        6 | “App báo còn trụ sạc nhưng đến nơi thì hết”; “Đến nơi thấy 3 xe đang đợi dù app báo còn 2 trụ trống”; “Pin còn 10% đến nơi trạm lại đang bảo trì, rất hoang mang” | Chưa ghi nhận phản bác trong 6 phản hồi; mẫu nhỏ nên không thể hiểu là không có counter-signal | Thu hẹp pain từ “tìm trạm” sang “trạng thái/lựa chọn có thể mất hiệu lực trong hành trình”; giữ priority/giữ chỗ như hypothesis |
| Log / ticket / review (nếu có) | Chưa có log/ticket riêng | Chưa có                                                                                                                                                           | Chưa có                                                                                        | Không suy rộng ngoài survey hiện có                                                                                             |

**Insight sau validation (1-2 câu — pain thật nằm ở đâu):**

``` text
Pain bước đầu được xác nhận không nằm ở việc chỉ tìm một trạm sạc, mà ở khoảng cách giữa trạng thái/lựa chọn tại thời điểm t0 và tình trạng thực tế tại t1.
Survey cho thấy người lái có thể gặp hết trụ, hàng đợi hoặc bảo trì ngoài kỳ vọng; mức độ thường xuyên và impact định lượng vẫn cần baseline.
```

Bằng chứng đính kèm (nếu có): [Form khảo sát trực tuyến](https://forms.cloud.microsoft/r/GdBDtqSF3U), [Bảng tổng hợp phản hồi chi tiết](https://ptiteduvn-my.sharepoint.com/:x:/g/personal/datht_b22tc027_stu_ptit_edu_vn/IQBVsN6UxPFfTLww10sEMkzNAfPCXt-CzAYu9ZP9XhH9mlI?e=saldHc)

### 4.2. Research giải pháp đã có (ít nhất 2-3 tools/patterns + 1-2 link kiểm được)

| Nguồn / tool / case                                 | Link                                                                                         | Họ giải quyết bước nào?                                                                                 | Điểm mạnh                                                         | Khoảng trống / rủi ro                                                                   | Bài học cho nhóm                                       |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------|--------------------------------------------------------|
| VinFast – tính năng liên quan đến pin trên ứng dụng | <https://vinfastauto.com/vn_vi/su-dung-tinh-nang-lien-quan-den-pin-tren-ung-dung-vinfast>    | Hiển thị pin, trạm gần, đầu sạc khả dụng, khoảng cách/thời gian, pin dự kiến và luồng liên quan đến sạc | Giải quyết phần lớn station discovery và thông tin trước khi chọn | Không đủ bằng chứng để kết luận mọi thay đổi sau khi đã chọn trạm đều được xử lý tối ưu | Không build lại “AI tìm trạm gần nhất”                 |
| VinFast – hướng dẫn sạc pin ô tô điện               | <https://vinfastauto.com/vn_vi/huong-dan-sac-pin-o-to-dien-vinfast-chi-tiet>                 | Tìm trạm, xem thông tin và định tuyến                                                                   | Route planning đã tồn tại                                         | Khoảng trống còn lại phải được chứng minh sau khi tính năng hiện có đã được tính đến    | Tập trung vào re-evaluation/monitoring                 |
| VinFast – FAQ ứng dụng ô tô                         | <https://vinfastauto.com/vn_vi/cau-hoi-thuong-gap/cau-hoi-xe-o-to/san-pham/ung-dung-vinfast> | Xác nhận các chức năng ứng dụng liên quan trạm/hành trình                                               | Nguồn chính thức để tránh giả định sai về sản phẩm hiện có        | Không chứng minh multi-vehicle priority là pain phổ biến                                | Multi-vehicle coordination chỉ là hypothesis cho pilot |

**Research takeaway (2-3 câu — nên build gì / không build gì):**

``` text
Research cho thấy nhóm không nên build lại chức năng tìm trạm hoặc route planning cơ bản vì các bước này đã được hỗ trợ trong hệ sinh thái hiện tại.
Hướng hợp lý hơn là một Workflow nhỏ: lấy signal → Rule safety filter → monitor → trigger re-evaluation → xếp hạng phương án → người lái xác nhận.
Agent chưa cần thiết; AI/ranking chỉ nên được thêm nếu deterministic Rule/score không đạt metric của pilot.
```

> Lưu ý: không dùng số liệu AI đưa nếu không verify được link chính thức. Ghi rõ giả định chưa chắc.

------------------------------------------------------------------------

## Phase 5 — Workflow + Problem Statement

### 5.1. Current workflow bản nhóm

Dán workflow hoặc link file: `02-group-problem-workflow.png`

``` text
[1 Kiểm tra pin - người lái]
→ [2 Xem trạm trên app]
→ [3 So sánh khoảng cách/ETA/trạng thái]
→ [4 Chọn trạm]
→ [5 Di chuyển]
→ [6 Trạng thái/lựa chọn không còn phù hợp - bottleneck]
→ [7 Người lái tự re-check và chọn lại]
```

| Bước | Actor                          | Input                                       | Output                           | Thời gian / tần suất | Ghi chú (handoff? bottleneck?) |
|------|--------------------------------|---------------------------------------------|----------------------------------|----------------------|--------------------------------|
| 1    | Người lái                      | Pin, nhu cầu hành trình                     | Quyết định cần sạc               | Mỗi lần cần sạc      | Human                          |
| 2    | Người lái + app                | Vị trí, dữ liệu trạm                        | Danh sách trạm                   | Mỗi lần tìm          | App hỗ trợ                     |
| 3    | Người lái                      | Khoảng cách, ETA, trạng thái trụ            | So sánh lựa chọn                 | **Chưa đo baseline** | Manual decision                |
| 4    | Người lái                      | Các lựa chọn                                | Trạm được chọn                   | **Chưa đo baseline** | Human decision                 |
| 5    | Người lái                      | Route                                       | Di chuyển                        | Theo hành trình      | Handoff app → thực tế          |
| 6    | Người lái + trạng thái thực tế | Hết trụ / hàng đợi / bảo trì / ETA thay đổi | Nhận ra phương án cũ kém phù hợp | Không cố định        | **Bottleneck**                 |
| 7    | Người lái                      | Pin còn lại + danh sách mới                 | Giữ/đổi trạm                     | **Chưa đo baseline** | Manual re-evaluation           |

**Bottleneck chính (2-3 câu):**

``` text
Bottleneck nằm ở bước re-evaluation sau khi phương án đã được chọn: người lái phải tự phát hiện thay đổi và tự so sánh lại trong khi pin tiếp tục giảm.
Survey cho tín hiệu rằng tình huống này có tồn tại, nhưng nhóm chưa có baseline về thời gian re-check, tần suất xảy ra hay tỷ lệ phải đổi trạm.
Do đó bottleneck đã rõ về vị trí trong workflow nhưng chưa đủ định lượng để Go.
```

### 5.2. Future workflow bản nhóm

Phải nhìn ra 5 thứ: bước nào máy (Rule), bước nào AI, bước nào người, boundary ở đâu, fallback khi AI sai.

``` text
[1 Pull pin + vị trí + traffic + trạng thái trụ - máy]
→ [2 Rule loại trạm không khả thi/an toàn - máy]
→ [3 Tính score/priority baseline - deterministic Workflow]
→ [4 Nếu cần, AI/ranking hỗ trợ trade-off giữa các phương án gần tương đương]
→ [5 Người lái review/xác nhận - human boundary]
→ [6 Điều hướng + monitor trạng thái]
→ [7 Nếu pin/traffic/trạng thái trụ thay đổi vượt ngưỡng → re-score/re-route]

Fallback:
- Nếu dữ liệu thiếu/trễ → bỏ recommendation nâng cao, hiển thị dữ liệu gốc + Rule filter.
- Nếu AI/ranking không chắc hoặc bị override → quay về deterministic score/list.
- Nếu trụ bị người khác sử dụng ngoài dự kiến → cập nhật trạng thái, re-score và yêu cầu người lái xác nhận lại.
```

**Before/after impact:**

| Metric                       |                         Trước |                                                           Sau kỳ vọng | Cách đo                                                               |
|------------------------------|------------------------------:|----------------------------------------------------------------------:|-----------------------------------------------------------------------|
| Tổng thời gian re-evaluation |        `T_baseline` — chưa đo |                                   **Pilot target ≤ 70% × T_baseline** | Cùng scenario, đo từ lúc trigger đến lúc người lái xác nhận           |
| Số bước                      |                             7 |                                                                     7 | Không tối ưu bằng giảm số bước; tối ưu effort ở bước so sánh/re-check |
| Số bước thủ công             |                    Khoảng 4/7 |                                                 2/7: review + confirm | Đếm thao tác cần quyết định của người                                 |
| Bottleneck chính             | Tự phát hiện + tự so sánh lại |                                                 Review recommendation | Quan sát pilot                                                        |
| Risk mới                     |      Không có ranking/AI risk |                                  Stale data, ranking sai, route churn | Log stale-data, override, re-route                                    |
| Chất lượng quyết định        |              Chưa có baseline | Không tăng lựa chọn trạm không khả thi; giảm re-route không cần thiết | Replay cùng scenario và so với baseline                               |

**Bottleneck mới kỳ vọng:** người lái review recommendation. Đây là bottleneck chấp nhận được vì nó giữ human-in-the-loop ở quyết định ảnh hưởng hành trình.

### 5.3. Problem Statement v0 (mỗi field 2-3 câu)

| Field              | Nội dung                                                                                                                                                                                                 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Actor**          | Tài xế Xanh SM và chủ sở hữu xe VinFast cần sạc trong một hành trình đang diễn ra. Tình huống pin thấp có rủi ro cao hơn nên cần được quan sát riêng trong pilot.                                        |
| **Workflow**       | Người lái kiểm tra pin → xem/so sánh trạm → chọn → di chuyển. Khi trạng thái trạm hoặc điều kiện hành trình thay đổi, họ phải tự re-check và quyết định lại.                                             |
| **Bottleneck**     | Bước re-evaluation sau quyết định ban đầu. Dữ liệu dùng tại t0 có thể không còn phản ánh tình trạng ở t1, làm người lái phải tự đánh giá lại nhiều signal.                                               |
| **Impact**         | Survey 6 người ghi nhận tình huống hết trụ, hàng đợi hoặc bảo trì ngoài kỳ vọng. Impact định lượng về thời gian/tần suất chưa có, vì vậy chưa được phép giả định lớn hơn evidence.                       |
| **Success Metric** | Pilot target: giảm median re-evaluation time ít nhất 30% so với manual baseline trên cùng scenario; không tăng lựa chọn trạm không khả thi hoặc re-route không cần thiết; theo dõi tỷ lệ override.       |
| **Boundary**       | Hệ thống chỉ monitor, filter, score/rank và đề xuất. Không tự lái, không tự đổi route, không cam kết reservation, không ưu tiên xe theo rule chưa được validate và không thay người lái quyết định cuối. |

**Câu hỏi AI phản biện v0 (nếu có):** - Field nào mơ hồ: Impact chưa có baseline; multi-vehicle priority chưa được validation; bước ranking có thể giải bằng Rule/optimization thay vì AI. - Tôi sửa gì: Tách validated pain khỏi solution hypothesis; thêm deterministic baseline; AI chỉ là optional intervention sau khi Rule/Workflow được benchmark.

------------------------------------------------------------------------

## Phase 6 — Rule / Workflow / Agent + Decision

### 6.0. Ma trận độ phù hợp (suy nghĩ nhanh, không thay quyết định cuối)

- Độ mơ hồ: \[ \] Thấp (có đúng/sai rõ) / \[x\] Cao (nhiều cách trả lời vẫn OK) — Vì sao: nhiều trạm có thể cùng khả thi nhưng trade-off khác nhau theo pin, ETA, trạng thái và mức ổn định.
- Độ phức tạp: \[ \] Thấp (1-2 bước) / \[x\] Cao (3+ bước/nguồn, phụ thuộc nhau) — Vì sao: cần lấy nhiều signal, lọc, theo dõi, trigger và đánh giá lại theo thời gian.

**Bài toán nhóm nằm ở ô nào:**

``` text
Mơ hồ cao + Phức tạp cao
```

**Vì sao (2-3 câu):**

``` text
Không có một trạm duy nhất luôn là đáp án đúng vì nhiều phương án có thể cùng khả thi và trade-off thay đổi theo thời gian.
Tuy nhiên các bước xử lý chính vẫn mô tả trước được, nên độ phức tạp cao không đồng nghĩa với việc cần Agent.
```

### 6.1. So sánh Rule / Workflow / Agent (so trên cùng 1 bài)

| Mức          | Phương án cho bài toán nhóm                                                                           | Khi nào đủ                                                    | Rủi ro                                                                           | Chọn? (Dùng cho bước nào?)       |
|--------------|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|----------------------------------------------------------------------------------|----------------------------------|
| **Rule**     | Safety filter + ngưỡng trigger + weighted score theo pin, khoảng cách, ETA, traffic và trạng thái trụ | Đủ nếu các tiêu chí/weight ổn định và cho kết quả tốt         | Cứng khi trade-off/ngoại lệ thay đổi; không xử lý tốt mọi thay đổi ngoài dự kiến | Có, bắt buộc làm baseline        |
| **Workflow** | Pull → Rule filter → score/rank → human confirm → monitor → trigger → re-score                        | Hợp khi luồng chính cố định nhưng có nhiều bước/nhánh hữu hạn | Phụ thuộc data freshness; phải quản lý fallback                                  | **Chọn làm mức chính cho pilot** |
| **Agent**    | Agent tự chọn tool/bước, tự lập kế hoạch re-route                                                     | Chỉ khi workflow cố định chứng minh không đủ                  | Khó debug/control; permission và safety risk cao                                 | Không chọn                       |

**5 câu hỏi chốt (trả lời câu đầy đủ):**

1.  Rule có giải được 70-80% case không?  
    Chưa biết; đây là câu hỏi phải đo trong pilot. Nếu Rule + weighted score giải được phần lớn case thì không cần thêm AI.

2.  Các bước có đi thẳng một đường không hay phải rẽ nhánh?  
    Có nhánh giữ route, re-score và fallback, nhưng tất cả đều có thể mô tả trước nên phù hợp Workflow.

3.  Có thật sự cần Agent tự lập kế hoạch + gọi tool không?  
    Không ở giai đoạn này. Workflow đủ để kiểm thử problem và giảm rủi ro.

4.  Nếu AI sai, ai phát hiện đầu tiên và sửa trong bao lâu?  
    Người lái là reviewer cuối. Recommendation có thể bị bỏ ngay trong cùng phiên và hệ thống quay về Rule/list gốc.

5.  Có hạ được từ Agent → Workflow → Rule không?  
    Có. Nhóm đã chủ động hạ xuống Workflow và dùng Rule làm baseline/safety layer; AI là optional, không phải mặc định.

**Mức chọn:**

``` text
Workflow
```

**Vì sao chọn (3-4 câu):**

``` text
Pain nằm trong một chuỗi nhiều bước: lấy signal, filter, theo dõi, trigger và re-evaluate, nên một Rule đơn lẻ không mô tả đủ orchestration.
Workflow phù hợp vì đường đi chính và fallback đều định nghĩa trước được.
Rule vẫn giữ vai trò safety filter và baseline; AI chỉ được phép xuất hiện ở ranking/trade-off nếu chứng minh cải thiện metric.
Agent chưa có giá trị đủ lớn để bù cho complexity và risk.
```

**Vì sao không chọn mức đơn giản hơn (2-3 câu):**

``` text
Nhóm không loại Rule; Rule là phần bắt buộc của solution và là benchmark đầu tiên.
Mức chọn là Workflow vì cần orchestration nhiều bước và monitoring theo thời gian, không phải vì nhất thiết phải dùng AI.
Nếu Workflow deterministic đạt target, nhóm sẽ không thêm AI.
```

### 6.2. Problem Statement v1 (v0 sửa chặt hơn + 3 field cuối)

| Field                                                                          | Nội dung                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Actor**                                                                      | Tài xế Xanh SM và chủ sở hữu xe VinFast cần sạc trong hành trình, đặc biệt ở tình huống pin thấp.                                                                                                              |
| **Workflow**                                                                   | Xem pin → tìm/so sánh trạm → chọn → di chuyển → monitor → trigger re-evaluation khi signal thay đổi → người lái xác nhận giữ/đổi phương án.                                                                    |
| **Bottleneck**                                                                 | Bước re-evaluation sau quyết định ban đầu: trạng thái trụ/ETA có thể thay đổi, khiến lựa chọn tại t0 không còn phù hợp tại t1.                                                                                 |
| **Impact**                                                                     | Survey 6 người xác nhận bước đầu các tình huống hết trụ, hàng đợi hoặc bảo trì ngoài kỳ vọng. Baseline thời gian và tần suất chưa đo nên impact định lượng vẫn là khoảng trống.                                |
| **Success Metric**                                                             | Pilot target: median re-evaluation time giảm ≥30% so với manual baseline cùng scenario; không tăng lựa chọn trạm không khả thi/re-route không cần thiết; ghi nhận override rate.                               |
| **Boundary** (làm / không làm)                                                 | Làm: monitor, Rule filter, score/rank, trigger re-evaluation và đề xuất. Không làm: tự lái, tự quyết định thay người lái, cam kết giữ trụ hoặc coi ưu tiên xe pin thấp là policy chính thức khi chưa validate. |
| **AI intervention point** (can thiệp sau bước nào, trước bước nào)             | Sau Rule safety filter và deterministic scoring, trước human review; AI chỉ hỗ trợ ranking/explanation khi nhiều phương án gần tương đương hoặc Rule không đạt metric pilot.                                   |
| **Mức chọn** (Rule / Workflow / Agent + 1 câu vì sao)                          | Workflow — cần orchestration nhiều bước/nguồn nhưng các bước và fallback vẫn xác định trước.                                                                                                                   |
| **Rủi ro & người thật kiểm tra** (rủi ro lớn nhất + ai kiểm tra bằng cách nào) | Rủi ro lớn nhất là stale/wrong data hoặc ranking sai. Người lái thấy dữ liệu/lý do, xác nhận cuối và có thể override ngay.                                                                                     |

### 6.3. Final decision

| Câu hỏi                               | Yes / Not Yet / No | Ghi chú (câu đầy đủ)                                                                        |
|---------------------------------------|--------------------|---------------------------------------------------------------------------------------------|
| Actor + workflow rõ chưa?             | Yes                | Actor, current workflow và vị trí bottleneck đã đủ rõ để thiết kế pilot.                    |
| Baseline + metric đo được chưa?       | Not Yet            | Metric và target pilot đã định nghĩa, nhưng baseline thời gian/tần suất chưa được thu thập. |
| Data/input đủ dùng chưa?              | Not Yet            | Chưa xác nhận quyền truy cập và freshness của pin, traffic, trạng thái trụ/reservation.     |
| AI sai, hậu quả chấp nhận được không? | Not Yet            | Human confirmation + fallback giảm risk, nhưng chưa có pilot chứng minh.                    |
| Có người review/owner không?          | Yes                | Người lái là reviewer quyết định cuối; owner kỹ thuật data/API còn phải xác định.           |
| Có cách non-AI đơn giản hơn không?    | Yes                | Rule + deterministic scoring/workflow là baseline bắt buộc.                                 |

**Decision:**

``` text
Not Yet
```

**Lý do (3-4 câu dựa trên bằng chứng):**

``` text
Survey 6 người cung cấp tín hiệu rằng lựa chọn/trạng thái trạm tại t0 có thể không còn phù hợp khi người dùng đến nơi.
Research đồng thời cho thấy VinFast đã có station discovery và route planning, nên nhóm không nên build lại chức năng hiện có.
Khoảng trống hợp lý để test là re-evaluation/monitoring, nhưng baseline và data/API real-time vẫn chưa đủ.
Vì vậy Decision là Not Yet: pilot Rule + Workflow trước, AI chỉ được thêm nếu tạo uplift đo được.
```

**Nếu Go — pilot nhỏ nhất (data nào, chạy tay ra sao, đo 3 số nào):**

``` text
Khi đủ điều kiện Go:
- Dùng 10-20 scenario kiểm soát, mỗi scenario có mức pin, vị trí, 3-5 trạm, ETA/traffic và trạng thái trụ; một số scenario cố tình thay đổi trạng thái ở t1, gồm cả trường hợp trụ bị người khác sử dụng trước.
- Chạy A: người dùng tự chọn; B: Rule + deterministic Workflow; C: thêm AI/ranking nếu B chưa đạt target.
- Đo 3 metric chính:
  1. Median re-evaluation time.
  2. Tỷ lệ lựa chọn/re-route không phù hợp.
  3. User override rate.
```

**Nếu Not Yet — cần validate gì trước:**

``` text
1. Đo baseline thời gian re-check/re-route và tần suất pain trên mẫu lớn hơn hoặc scenario replay.
2. Xác nhận quyền truy cập và freshness của pin, traffic, trạng thái trụ và reservation nếu có.
3. Validate riêng hypothesis multi-vehicle coordination và ưu tiên xe pin thấp; không suy ra trực tiếp từ survey hiện tại.
4. Benchmark Rule + weighted score + deterministic Workflow trước khi thêm AI.
5. Kiểm tra các case trạng thái thay đổi ngoài quyền kiểm soát hệ thống, ví dụ người khác tới sạc trước.
```

**Nếu No-Go — làm gì thay AI:**

``` text
Giữ Rule + deterministic Workflow/UI alert:
lọc trạm không khả thi, cảnh báo dữ liệu stale, trigger khi trạng thái đổi và để người lái chọn từ danh sách đã lọc.
```

**Exit / rollback (khi nào dừng AI, quay về cách cũ):**

``` text
Không dùng AI/ranking nếu Rule + deterministic Workflow đã đạt target hoặc AI không tạo uplift rõ ràng.
Rollback về Rule + danh sách trạm gốc nếu stale-data rate cao, user override tăng, re-route không cần thiết tăng hoặc recommendation làm xấu safety/decision quality.
Nếu AI liên tục bị người dùng bỏ qua hoặc không cải thiện median re-evaluation time trong pilot, giữ solution ở mức Workflow không AI.
```

------------------------------------------------------------------------

### Self-check nộp phần 02 (nhóm)

- [x] Có nhật ký hội tụ → 1 (nhóm 5 người: 15 candidate → cluster + shortlist + score)
- [x] Có validation (quote thật) + research (link kiểm được)
- [ ] Có workflow trước/sau đủ thời gian, handoff, bottleneck, boundary, fallback — còn thiếu baseline thời gian thực tế
- [ ] Có PS v0 → v1, metric có trước/sau + cách đo, boundary có làm/không làm — metric/target đã rõ nhưng baseline chưa đo
- [x] Có so sánh Rule/Workflow/Agent + Decision Go/Not Yet/No-Go có lý do
