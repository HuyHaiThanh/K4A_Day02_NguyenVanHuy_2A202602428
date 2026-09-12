# 03 — Individual Reflection

> Viết bằng lời của bạn (Phase 7 trong `01-worksheet.md`). Có thể dùng AI gợi ý câu hỏi tự soi, không dùng AI viết thay. 8-12 câu, có chuyện cụ thể.

## Thông tin cá nhân

- Họ và tên: Nguyễn Văn Huy
- Mã học viên: 2A202602428
- Nhóm: Nhóm 5 thành viên gồm Nguyễn Văn Huy, Hoàng Thái Đạt, Nguyễn Trọng Phúc, Nguyễn Quốc Đạt, Nguyễn Việt Hùng
- Candidate problem nhóm chọn: Tài xế Xanh SM/chủ xe VinFast có thể phải đánh giá lại lựa chọn trạm sạc trong hành trình khi mức pin, giao thông hoặc trạng thái trụ thay đổi so với thời điểm lựa chọn ban đầu.

---

## 1. Tôi đã tham gia vào phần nào?

Ghi việc cụ thể + kết quả cụ thể. Không ghi chung chung kiểu "tham gia thảo luận".

| Hoạt động | Tôi đã làm gì? (việc cụ thể) | Kết quả / ảnh hưởng tới nhóm |
|---|---|---|
| Scan cá nhân | Tôi scan 10 vấn đề trong cùng bối cảnh vận hành chuỗi bán lẻ và chọn Top 3 gồm điều chuyển hàng giữa cửa hàng, đề xuất replenishment và tìm nguyên nhân chênh lệch tồn kho. | Nhóm có thêm một cụm candidate về vận hành tồn kho với actor, workflow và metric tương đối rõ để so sánh với các bài của thành viên khác. |
| Pitch Problem Card | Tôi pitch Card #1 về điều chuyển hàng giữa các cửa hàng khi một chi nhánh sắp thiếu hàng, với baseline scenario 17 phút/case và bottleneck ở bước so safety stock, tốc độ bán và khoảng cách. | Giúp nhóm thấy một bài toán có thể benchmark Rule trước AI và có human boundary rõ trước khi tạo yêu cầu điều chuyển. |
| Challenge bài của bạn khác | Tôi cùng nhóm challenge bài trạm sạc theo chuỗi: pin + quãng đường → thêm traffic + trạng thái trụ real-time → xung đột khi hai xe cùng đến một trụ → trường hợp người ngoài hệ thống tới sạc trước. | Nhóm không dừng ở “tìm trạm gần nhất” mà chuyển sang bài toán monitor, re-evaluate và xem priority theo mức pin là hypothesis cần kiểm chứng. |
| Gom trùng / cluster | Tôi tham gia gom ba candidate retail của mình vào cụm vận hành tồn kho và cùng nhóm tách các cụm developer, đối soát/tài liệu và VinFast/Xanh SM. | Danh sách candidate được thu gọn thành các pattern rõ hơn để shortlist thay vì chọn theo cảm tính. |
| Chọn candidate problem | Tôi tham gia so sánh shortlist và chấp nhận không chọn bài retail của mình khi candidate trạm sạc có tác động trực tiếp tới người dùng và tạo được nhiều câu hỏi về Rule/Workflow/Agent. | Nhóm hội tụ về một candidate chung thay vì cố giữ bài cá nhân của từng người. |
| Validation / research | Tôi tham gia đọc lại kết quả survey 6 người và đối chiếu các tính năng hiện có của VinFast để tránh giả định rằng app chưa có tìm trạm/route planning. | Problem được thu hẹp từ “tìm trạm” sang khoảng cách giữa lựa chọn ở t0 và tình trạng thực tế ở t1; multi-vehicle priority được giữ ở mức hypothesis. |
| Workflow nhóm | Tôi tham gia rà current/future workflow và nhấn mạnh bước monitor → trigger → re-score/re-route, cùng fallback khi dữ liệu thiếu/trễ hoặc trụ bị người khác sử dụng trước. | Future workflow thể hiện rõ Rule, Workflow, AI optional, human boundary và fallback thay vì mô tả một AI tự quyết định toàn bộ. |
| Problem Statement | Tôi tham gia sửa Problem Statement theo hướng problem-first, tách pain đã có evidence khỏi solution hypothesis và giữ impact định lượng ở mức chưa có baseline. | PS v1 rõ hơn về actor, bottleneck, success metric, boundary và AI intervention point; tránh overclaim từ survey nhỏ. |
| Rule / Workflow / Agent | Tôi ủng hộ chọn Workflow làm mức chính, Rule/weighted score làm baseline và chỉ dùng AI cho ranking/trade-off nếu Rule không đạt metric. | Nhóm không chọn Agent chỉ vì bài toán phức tạp; giải pháp được hạ về mức đơn giản hơn, dễ kiểm soát và dễ pilot. |
| Decision | Tôi đồng ý với Decision `Not Yet` vì nhóm chưa có baseline thời gian và chưa xác nhận data/API real-time dù pain đã có tín hiệu từ survey. | Quyết định cuối nhất quán với evidence: cần benchmark Rule + deterministic Workflow và validate data trước khi cân nhắc AI sâu hơn. |

**Dấu tay rõ nhất của tôi trong artifact cuối (1-2 câu):**

```text
Dấu tay rõ nhất của tôi là cách challenge để nhóm không nhảy thẳng từ “tìm trạm” sang một Agent điều phối hoàn chỉnh, mà tách bài toán thành Rule safety filter, deterministic Workflow, monitor/re-evaluate và AI chỉ là lớp hỗ trợ nếu thật sự cần.
Tôi cũng đóng góp góc nhìn “Rule trước AI” từ Problem Card điều chuyển tồn kho cá nhân sang cách nhóm ra quyết định cho bài trạm sạc.
```

---

## 2. Bảng dùng AI (mỗi dòng 1 phase có dùng AI — 2 cột cuối bắt buộc)

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai / hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| Scan | Dùng AI để gợi ý cách mở rộng problem scan trong bối cảnh chuỗi bán lẻ và kiểm tra xem problem có actor/workflow/metric chưa. | Giúp tôi nhìn được nhiều pain lặp lại quanh tồn kho, replenishment và vận hành cửa hàng thay vì chỉ nghĩ tới một solution AI. | Một số gợi ý ban đầu quá rộng hoặc giống ý tưởng sản phẩm hơn là problem thật. | Tôi giữ các problem cùng một context retail, thêm actor và baseline scenario, đồng thời bỏ các ý khó truy ngược về workflow cụ thể. |
| Problem Card | Nhờ AI phản biện Card điều chuyển hàng và so sánh Rule với Workflow/AI. | AI chỉ ra data freshness và safety stock có thể quan trọng hơn thuật toán ranking. | AI có xu hướng đề xuất ranking/AI khá sớm dù Rule có thể đã đủ cho nhiều case. | Tôi đưa `safety stock + nguồn gần nhất` thành non-AI/Rule baseline và đặt human boundary trước lúc tạo lệnh điều chuyển. |
| Workflow | Dùng AI để kiểm tra current/future workflow và cách thể hiện bottleneck, boundary, fallback. | Giúp tách rõ bước máy, bước Rule, bước người và chỗ cần re-evaluate. | Nếu chỉ theo AI, workflow dễ bị “đẹp trên giấy” nhưng bỏ qua case người khác tới trụ trước hoặc dữ liệu stale. | Tôi bổ sung monitor → trigger → re-score/re-route và fallback khi trạng thái ngoài hệ thống thay đổi. |
| Research | Dùng AI để gợi ý những điểm cần kiểm chứng về tính năng hiện có và gap của VinFast. | Giúp xác định câu hỏi research: app đã có station discovery/route planning tới đâu, gap còn lại là gì. | AI có thể suy diễn rằng sản phẩm hiện tại thiếu tính năng hoặc đưa claim không có nguồn chính thức. | Tôi chỉ giữ các kết luận truy được về nguồn VinFast chính thức và sửa framing từ “thiếu tìm trạm” sang “re-evaluation khi trạng thái thay đổi”. |
| Problem Statement | Nhờ AI phản biện field nào đang solution-first, overclaim hoặc chưa có metric. | Hữu ích nhất ở việc tách validated pain khỏi hypothesis về priority/multi-vehicle coordination. | AI từng có xu hướng biến cơ chế ưu tiên xe pin thấp thành một rule đã đúng trong khi survey chưa chứng minh điều đó. | Tôi giữ priority là hypothesis, ghi rõ impact chưa có baseline và không coi reservation/priority là policy thật trong boundary. |
| Rule / Workflow / Agent | Dùng AI để thử lập luận cho cả Rule, Workflow và Agent trên cùng một bài toán. | Giúp thấy độ phức tạp cao không đồng nghĩa với phải chọn Agent. | AI dễ đánh giá cao Agent vì có nhiều signal động và nhiều bước. | Tôi chốt Workflow là mức chính, Rule là baseline/safety layer và AI chỉ optional cho ranking khi deterministic approach không đạt metric. |
| Decision | Dùng AI để kiểm tra xem `Go`, `Not Yet` hay `No-Go` có nhất quán với evidence không. | Giúp chỉ ra mâu thuẫn nếu vừa nói impact đo được cao vừa thừa nhận chưa có baseline/data feasibility. | AI có thể làm report trông “hoàn thành” bằng cách giả định baseline hoặc target như dữ liệu thật. | Tôi giữ Decision `Not Yet`, không bịa baseline và ghi rõ những validation/data check cần có trước khi Go. |

> Nếu phase nào không dùng AI, ghi `Không dùng` và vì sao tự làm.

---

## 3. Reflection câu hỏi mở

Chọn 3-4 câu trong 6 câu dưới để viết thành đoạn 8-12 câu (không trả lời bullet 1 dòng):
- Tôi học được gì khi nghe top 3 problems của các bạn khác?
- Nhóm có lúc nào bị solution-first, đòi làm Agent cho ngầu không?
- Tôi có thay đổi ý kiến sau khi bị challenge không, vì sao đổi?
- Tôi đóng góp gì thật sự vào artifact cuối, phần nào có dấu tay của tôi?
- Điều khó nhất khi viết Problem Statement là gì, metric hay boundary?
- Nếu làm lại, tôi sẽ challenge nhóm mạnh hơn ở điểm nào?

**Reflection:**

```text
Qua Day 02, tôi nhận ra một problem tốt không nhất thiết phải là problem của chính mình hoặc problem nghe “AI” nhất, mà phải có actor, workflow, bottleneck và cách đo đủ rõ.
Ban đầu tôi tập trung vào ba bài toán retail vì chúng có workflow quen thuộc và dễ nhìn thấy Rule baseline, nhưng khi nghe các candidate của nhóm tôi thấy bài trạm sạc có nhiều thay đổi trạng thái theo thời gian và tạo ra nhiều câu hỏi product hơn.
Trong lúc thảo luận, nhóm cũng có xu hướng đi khá nhanh từ bài toán chỉ đường sang điều phối real-time và priority, nên tôi thấy việc challenge solution-first là cần thiết.
Điểm làm tôi thay đổi cách nhìn là phản biện “nếu hai xe cùng được chỉ đến một trụ thì sao” và tiếp theo là “nếu một người ngoài hệ thống tới sạc trước thì sao”; từ đó tôi hiểu rằng solution không thể chỉ tối ưu một lần ở t0.
Tôi cho rằng đóng góp rõ nhất của mình là giữ tư duy Rule trước AI và yêu cầu có fallback, human boundary trước khi tăng mức tự động hóa.
Khi viết Problem Statement, phần khó nhất với tôi không phải mô tả workflow mà là giữ metric và impact trung thực, vì survey mới cho tín hiệu pain nhưng chưa cho baseline định lượng.
Tôi cũng học được rằng research existing solution có thể làm thay đổi cả cách framing problem: sau khi biết VinFast đã có tìm trạm và route planning, nhóm phải thu hẹp gap sang re-evaluation khi trạng thái thay đổi.
Việc so sánh Rule, Workflow và Agent giúp tôi thấy Agent không phải đích đến mặc định; trong case này Workflow hợp lý hơn vì các bước chính vẫn mô tả và kiểm soát được.
Tôi đồng ý với Decision Not Yet vì nó phản ánh đúng mức evidence hiện tại thay vì cố biến bài làm thành một dự án đã sẵn sàng triển khai.
Nếu làm lại, tôi sẽ challenge nhóm sớm hơn về baseline, data freshness/API và cách chứng minh priority theo mức pin trước khi dành nhiều thời gian thiết kế solution.
```

---

## 4. Tự kiểm cuối bài (check trước khi nộp repo)

- [x] [12đ] Cá nhân có 5+ problems + top 3 Problem Cards
- [x] [12đ] Tôi đã pitch rõ + challenge nhóm đúng trọng tâm (ghi ở bảng mục 1)
- [x] Nhóm có nhật ký hội tụ từ candidates về 1 bài
- [x] [15đ] Nhóm có workflow trước/sau
- [x] [20đ] Nhóm có PS v0/v1 với metric + boundary rõ
- [x] [15đ] Nhóm có so sánh No AI / Rule / Workflow / Agent
- [x] [10đ] Nhóm có Go / Not Yet / No-Go + lý do rõ
- [x] [10đ] Reflection này có vai trò thật + AI giúp/sai ở đâu + điều học được + nếu làm lại đổi gì
- [x] [6đ] Tôi tự giải thích được mạch problem → workflow → metric → boundary → độ phù hợp AI
