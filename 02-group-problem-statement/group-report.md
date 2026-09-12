# 02 --- Group Problem Statement (Bản nộp nhóm)

> Làm chung 1 bản, mỗi thành viên copy vào repo cá nhân. Đi theo Phase 3
> → 6 trong `01-worksheet.md`. Nhóm chỉ chọn **candidate problem** ở
> Phase 3, viết Problem Statement sau khi validate + vẽ workflow.

## Thành viên nhóm

  -----------------------------------------------------------------------------
  STT   Họ và    Mã học viên   Vai trò trong nhóm (VD: facilitator, workflow,
        tên                    research, writer)
  ----- -------- ------------- ------------------------------------------------
  1     Nguyễn   2A202602428   writer, research
        Văn Huy                

  2     Hoàng    2A202602959   research, facilitator
        Thái Đạt               

  3     Nguyễn   2A202602552   research, workflow
        Trọng                  
        Phúc                   

  4     Nguyễn   2A202602369   research, workflow
        Quốc Đạt               

  5     Nguyễn   2A202602972   research, facilitator
        Việt                   
        Hùng                   
  -----------------------------------------------------------------------------

**Candidate problem nhóm chọn (1 câu):**

Tài xế Xanh SM và chủ xe VinFast cần duy trì lựa chọn trạm sạc phù hợp
trong hành trình, nhưng phương án đã chọn có thể trở nên kém phù hợp khi
mức pin, trạng thái trụ hoặc điều kiện di chuyển thay đổi.

------------------------------------------------------------------------

## Phase 3 --- Group Convergence: từ 9-12 candidates về 1

### 3.1. Trình bày top 3 mỗi người (mỗi candidate 1-2 phút)

  ----------------------------------------------------------------------------------------
  \#          Người đưa   Candidate    Người gặp vấn Điểm nghẽn          Cảm nhận nhanh
              ra          problem      đề                                của nhóm
  ----------- ----------- ------------ ------------- ------------------- -----------------
  1           Nguyễn Văn  Điều chuyển  Nhân viên vận Phải kiểm tra tồn   Workflow rõ,
              Huy         hàng giữa    hành chuỗi,   nhiều chi nhánh,    impact đo được;
                          các cửa hàng quản lý cửa   safety stock, tốc   nên benchmark
                          khi một chi  hàng          độ bán và khoảng    Rule trước
                          nhánh sắp                  cách trước khi chọn Workflow/AI
                          thiếu hàng                 nguồn               

  2           Nguyễn Văn  Đề xuất      Nhân viên vận Phải biến sales     Có metric rõ
              Huy         lượng bổ     hành /        history, tồn và     nhưng phụ thuộc
                          sung tồn kho merchandise   promotion thành     chất lượng dữ
                          cho từng cửa planner       lượng replenishment liệu lịch sử
                          hàng                                           

  3           Nguyễn Văn  Tìm nguyên   Nhân viên     Phải lần            Rule
              Huy         nhân chênh   kho, quản lý  transaction         reconciliation có
                          lệch tồn kho cửa hàng      bán/nhập/trả/điều   thể xử lý nhiều
                                                     chuyển để tìm       case; AI chỉ nên
                                                     nguyên nhân         hỗ trợ case khó

  4           Hoàng Thái  Đối soát các Nhân viên kế  Phải thu thập và    Có nhu cầu thực
              Đạt         giao dịch    toán          đối chiếu nhiều     tế nhưng cần
                          online                     giao dịch thủ công  baseline rõ

  5           Hoàng Thái  Tìm kiếm và  Chủ shop bán  Khó tìm đúng video  Cần mapping video
              Đạt         xuất video   hàng online   khi cần đối         ↔ đơn hàng và tần
                          gói hàng                   soát/khiếu nại      suất đủ lớn

  6           Hoàng Thái  Check quy    Người mua     Phải tra cứu và đối Giá trị cao nhưng
              Đạt         hoạch/tính   bán, nhân     chiếu nhiều nguồn   rủi ro pháp lý
                          pháp lý của  viên BĐS                          lớn
                          sổ đỏ                                          

  7           Nguyễn      App VinFast  Tài xế Xanh   Quyết định tại t0   Pain trực tiếp
              Trọng Phúc  khó duy trì  SM, chủ xe    có thể không còn    user; worksheet
                          lựa chọn     VinFast       phù hợp tại t1 khi  nhóm chấm cao
                          trạm sạc phù               pin/traffic/trạng   nhất
                          hợp khi dữ                 thái trụ thay đổi   
                          liệu thay                                      
                          đổi                                            

  8           Nguyễn      QA Xanh SM   Team QA Xanh  Bước nghe và phân   Workflow/metric
              Trọng Phúc  phải nghe    SM            loại mất khoảng     rõ; phụ thuộc
                          ghi âm hủy                 8-12 phút/case theo Speech-to-Text
                          chuyến và                  worksheet           
                          note thủ                                       
                          công                                           

  9           Nguyễn      CSKH VinFast CSKH VinFast  Phải hiểu mô tả     Khả thi với NLP
              Trọng Phúc  phân tích                  thiếu ý/sai chính   nhưng tác động
                          lỗi từ mô tả               tả rồi phân loại    chủ yếu nội bộ
                          tiếng Việt                                     
                          của khách                                      

  10          Nguyễn Quốc Hiểu một     Developer     Mất thời gian gom   Actor rõ; cần
              Đạt         task mới từ                context trước khi   định nghĩa "hiểu
                          nhiều Slack                bắt đầu             đủ"
                          thread,                                        
                          ticket và                                      
                          tài liệu                                       

  11          Nguyễn Quốc Tìm người    Developer /   Không biết đúng     Có thể đo thời
              Đạt         phụ trách    thành viên    owner nên bị chuyển gian chờ; cần
                          đúng việc    nhóm          tiếp                owner list chuẩn
                          khi task bị                                    
                          vướng                                          

  12          Nguyễn Quốc Viết weekly  Developer /   Phải gom nhiều      Workflow lặp lại;
              Đạt         update bằng  thành viên    nguồn rồi viết lại  output rõ
                          cách gom     nhóm                              
                          thông tin                                      
                          thủ công                                       

  13          Nguyễn Việt Tìm nguyên   Developer     Phải đọc code/log   Thường xuyên
              Hùng        nhân và sửa                và thử nhiều hướng  nhưng scope rộng
                          lỗi trong hệ               để tìm root cause   
                          thống                                          

  14          Nguyễn Việt Viết và kiểm Developer     Phải tự xác định    Lặp lại; chưa có
              Hùng        thử test                   nhiều test case và  baseline rõ
                          case cho                   kiểm tra            
                          chức năng                                      
                          mới                                            

  15          Nguyễn Việt Tra cứu      Developer     Mất thời gian tìm   Phù hợp cluster
              Hùng        code, cú                   đúng tài            knowledge search
                          pháp và cách               liệu/context        
                          sử dụng API                                    
  ----------------------------------------------------------------------------------------

### 3.2. Gom trùng / cluster (gom 9-12 ý thành 3-4 cụm)

  ---------------------------------------------------------------------------
  Cluster           Candidates        Pattern chung     Ghi chú
                    included                            
  ----------------- ----------------- ----------------- ---------------------
  A                 Nguyễn Văn Huy:   Vận hành tồn kho  Có thể so Rule với
                    điều chuyển hàng, chuỗi: phát hiện  Workflow; cùng một
                    replenishment,    thiếu/dư → quyết  retail context
                    chênh lệch tồn    định → đối soát   

  B                 Nguyễn Quốc Đạt,  Developer mất     Phù hợp
                    Nguyễn Việt Hùng  thời gian tìm     Search/RAG/Workflow
                                      context, owner,   nhưng cần thu hẹp
                                      code/API hoặc     scope
                                      root cause trước  
                                      khi làm việc      

  C                 Hoàng Thái Đạt    Thu thập dữ liệu  Rule/Workflow phù
                                      → đối chiếu →     hợp; bài pháp lý cần
                                      kiểm tra → đưa ra human review
                                      kết quả           

  D (nếu có)        Nguyễn Trọng Phúc Các pain trong hệ Candidate trạm sạc
                                      sinh thái         tác động trực tiếp
                                      VinFast/Xanh SM   user; QA có metric rõ
                                      liên quan vận     
                                      hành và trải      
                                      nghiệm khách hàng 
  ---------------------------------------------------------------------------

### 3.3. Shortlist (giữ 2-3 bài trả lời được 7 câu hỏi worksheet)

  -----------------------------------------------------------------------
  Candidate               Vì sao vào shortlist    Rủi ro / điều chưa rõ
                          (2-3 ý)                 
  ----------------------- ----------------------- -----------------------
  Duy trì lựa chọn trạm   Pain trực tiếp user;    Chưa rõ data/API
  sạc VinFast/Xanh SM khi nhiều signal động; so   real-time; cần phân
  điều kiện thay đổi      được                    biệt với tính năng
                          Rule/Workflow/Agent     VinFast đã có

  Phân loại lý do hủy     Bottleneck rõ; đo được  Cần audio data, ground
  chuyến Xanh SM từ ghi   thời gian/case và       truth và STT tiếng Việt
  âm                      accuracy; dễ pilot      đủ tốt

  Phân tích lỗi CSKH      Actor/output rõ; có thể Tác động chủ yếu nội
  VinFast từ mô tả tiếng  đo classification       bộ; cần taxonomy lỗi
  Việt                    accuracy                
  -----------------------------------------------------------------------

### 3.4. Score để đồng thuận (chấm 1-5, ép nói rõ vì sao cho 5 / cho 3)

  ------------------------------------------------------------------------------------------
  Candidate      Actor rõ   Workflow    Pain có   Impact      Làm  So sánh     Nhóm     Tổng
                                  rõ   evidence  đo được    trong    R/W/A     hiểu 
                                                              lab     được   domain 
  -------------- -------- ---------- ---------- -------- -------- -------- -------- --------
  Duy trì lựa           4          3          5        4        3        4        5       28
  chọn trạm sạc                                                                     
  VinFast/Xanh                                                                      
  SM                                                                                

  Phân loại lý          5          3          3        3        4        4        4       26
  do hủy chuyến                                                                     
  Xanh SM                                                                           

  Phân tích lỗi         5          4          4        3        4        4        2       26
  CSKH VinFast                                                                      
  ------------------------------------------------------------------------------------------

**Candidate nhóm chọn (1 bài duy nhất):**

``` text
Duy trì lựa chọn trạm sạc phù hợp cho tài xế Xanh SM/chủ xe VinFast
khi mức pin, trạng thái trụ và điều kiện di chuyển thay đổi trong hành trình.
```

**Vì sao chọn (4-5 câu):**

``` text
Candidate này đạt tổng điểm cao nhất trong worksheet nhóm: 28/35.
Pain tác động trực tiếp đến người dùng cuối thay vì chỉ tối ưu một workflow nội bộ.
Bài toán có nhiều tín hiệu động như mức pin, trạng thái trụ và điều kiện di chuyển nên phù hợp để so sánh Rule, Workflow và Agent.
Research cho thấy VinFast đã có tìm trạm và route planning cơ bản, vì vậy khoảng trống đáng kiểm tra hơn là lúc lựa chọn tại t0 trở nên kém phù hợp tại t1.
Nhóm chọn candidate này để tiếp tục validate khoảng trống đó thay vì xây lại chức năng “tìm trạm gần nhất”.
```

**Vì sao KHÔNG chọn các candidate còn lại (mỗi bài 2-3 câu):**

``` text
Phân loại lý do hủy chuyến có workflow và metric rõ, thậm chí dễ pilot hơn,
nhưng tác động chính nằm trong quy trình QA nội bộ thay vì trải nghiệm trực tiếp của người dùng.

Phân tích lỗi CSKH cũng phù hợp NLP/LLM và có thể đo accuracy,
nhưng impact chủ yếu là tăng tốc xử lý nội bộ và nhóm hiểu domain này ít hơn candidate trạm sạc.
```

**Disagreement (nếu có --- ai lo gì, chốt ra sao):**

``` text
Một ý kiến trong nhóm lo rằng “tìm trạm sạc” đã là chức năng hiện có nên candidate có thể bị trùng giải pháp thị trường.
Nhóm thống nhất không framing bài toán là thiếu chức năng tìm trạm, mà chuyển sang việc duy trì lựa chọn phù hợp khi trạng thái thay đổi.
Nhóm cũng thống nhất chưa dùng Agent; trước tiên phải kiểm tra xem Rule + Workflow có giải được phần lớn case hay không.
```

------------------------------------------------------------------------

## Phase 4 --- Quick Validation + Research

### 4.1. Quick validation (ít nhất 1 cách: interview 2-3 người hoặc survey 5-10 người)

> Nội dung validation dưới đây bám theo Google Sheet nhóm. Vì chưa có
> file evidence gốc đính kèm trong repo, các quote/số liệu này cần được
> xem là ghi nhận của nhóm và nên bổ sung evidence nếu giảng viên yêu
> cầu kiểm chứng.

  --------------------------------------------------------------------------
  Nguồn            Số người / mẫu Tín hiệu xác  Tín hiệu phản Nhóm sửa
                                  nhận (kèm     bác           problem thế
                                  quote nguyên                nào
                                  văn)                        
  ------------- ----------------- ------------- ------------- --------------
  Interview       10 người: 6 tài "Đến nơi thấy Người đi giờ  Thu hẹp pain
                xế Xanh SM, 4 chủ 3 xe đang đợi thấp điểm     từ "khó tìm
                       xe cá nhân dù app báo    hoặc dùng     trạm" sang
                                  còn 2 trụ     trạm quen cho "lựa chọn ban
                                  trống"; "Pin  biết hầu như  đầu có thể mất
                                  còn 10% đến   không gặp trở hiệu lực khi
                                  nơi trạm lại  ngại          trạng thái
                                  đang bảo trì,               thay đổi"
                                  rất hoang                   
                                  mang"                       

  Survey / poll   Chưa có dữ liệu Chưa có       Chưa có       Không dùng
                      riêng trong                             survey để suy
                        worksheet                             rộng thêm
                                                              ngoài dữ liệu
                                                              hiện có

  Log / ticket   Review cộng đồng Worksheet ghi Worksheet ghi Crowdsourced
  / review (nếu         Facebook; 45% phản ánh  khoảng 15%    signal chỉ là
  có)              worksheet chưa trạng thái    khiếu nại đến input bổ sung;
                       ghi số mẫu trụ ảo/trụ    từ 4G/thanh   cần log/API
                                  hỏng          toán, không   chính thức để
                                                phải điều     xác nhận
                                                phối          
  --------------------------------------------------------------------------

**Insight sau validation (1-2 câu --- pain thật nằm ở đâu):**

``` text
Pain không nằm ở việc chỉ “tìm một trạm sạc”, mà ở việc một phương án hợp lý tại t0 có thể trở nên kém phù hợp tại t1 khi pin, trạng thái trụ hoặc điều kiện di chuyển thay đổi.
Tuy nhiên mức độ pain vẫn cần được xác nhận bằng evidence gốc và baseline đo trực tiếp.
```

Bằng chứng đính kèm (nếu có): `02-group-problem-statement-survey.png`,
`...-interview-notes.md`

### 4.2. Research giải pháp đã có (ít nhất 2-3 tools/patterns + 1-2 link kiểm được)

  --------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Nguồn /     Link                                                                                         Họ giải quyết   Điểm mạnh   Khoảng trống /  Bài học cho
  tool / case                                                                                              bước nào?                   rủi ro          nhóm
  ----------- -------------------------------------------------------------------------------------------- --------------- ----------- --------------- ---------------
  VinFast --- https://vinfastauto.com/vn_vi/su-dung-tinh-nang-lien-quan-den-pin-tren-ung-dung-vinfast      Xem pin, trạm   Đã giải     Chưa đủ bằng    Không build lại
  tính năng                                                                                                gần,            quyết phần  chứng để kết    "tìm trạm gần
  Pin và Sạc                                                                                               availability,   lớn station luận mọi thay   nhất"
                                                                                                           thời gian/quãng discovery   đổi khi đang di 
                                                                                                           đường, pin dự               chuyển đều được 
                                                                                                           kiến, chỉ                   xử lý tối ưu    
                                                                                                           đường/đặt chỗ                               

  VinFast --- https://vinfastauto.com/vn_vi/cau-hoi-thuong-gap/cau-hoi-xe-o-to/san-pham/ung-dung-vinfast   Tìm trạm gần,   Xác nhận    Làm yếu framing Tập trung vào
  FAQ ứng                                                                                                  route planning, route       cũ "app khó tìm re-evaluation
  dụng ô tô                                                                                                gợi ý trạm trên planning đã trạm"           khi trạng thái
                                                                                                           hành trình      tồn tại                     thay đổi

  VinFast --- https://vinfastauto.com/vn_vi/cach-tim-tram-sac-vinfast                                      Tìm trạm, xem   Workflow    Chưa chứng minh Chỉ giữ
  cách tìm                                                                                                 tình trạng,     hiện tại    multi-vehicle   multi-vehicle
  trạm sạc                                                                                                 khoảng          khá đầy đủ  priority là     coordination
                                                                                                           cách/thời gian              khoảng trống    như hypothesis
                                                                                                           và chỉ đường                thực tế         
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Research takeaway (2-3 câu --- nên build gì / không build gì):**

``` text
Nhóm không nên build lại một “AI tìm trạm sạc gần nhất” vì các chức năng tìm trạm và route planning cơ bản đã tồn tại.
Hướng đáng pilot hơn là Workflow monitor các signal, chỉ re-score/re-route khi phương án hiện tại vượt ngưỡng rủi ro và luôn để người lái xác nhận.
Multi-vehicle coordination chỉ nên tiếp tục nếu validation thật xác nhận nhu cầu.
```

> Lưu ý: không dùng số liệu AI đưa nếu không verify được link chính
> thức. Ghi rõ giả định chưa chắc.

------------------------------------------------------------------------

## Phase 5 --- Workflow + Problem Statement

### 5.1. Current workflow bản nhóm

Dán workflow hoặc link file:
`02-group-problem-statement-workflow.png/pdf/md`

``` text
[1 Kiểm tra pin - người lái]
→ [2 Mở app/map tìm trạm]
→ [3 Xem availability + ETA + pin dự kiến]
→ [4 Chọn trạm]
→ [5 Di chuyển]
→ [6 Điều kiện thay đổi - bottleneck]
→ [7 Tự kiểm tra lại]
```

  ------------------------------------------------------------------------------------
  Bước        Actor       Input               Output      Thời gian / Ghi chú
                                                          tần suất    (handoff?
                                                                      bottleneck?)
  ----------- ----------- ------------------- ----------- ----------- ----------------
  1           Người lái   Mức pin, hành trình Quyết định  Khi cần sạc Human
                                              cần sạc                 

  2           Người lái + Vị trí hiện tại     Danh sách   Mỗi lần cần VinFast đã hỗ
              app                             trạm        tìm trạm    trợ

  3           Người lái + Availability,       Các lựa     Chưa có     Input cho quyết
              app         khoảng cách, ETA,   chọn        baseline    định
                          pin dự kiến                                 

  4           Người lái   Danh sách lựa chọn  Trạm được   Chưa có     Human decision
                                              chọn        baseline    

  5           Người lái   Route               Xe di       Theo hành   ---
                                              chuyển      trình       

  6           Hệ thống    Pin/traffic/trạng   Phương án   Không cố    **Bottleneck**
              thực tế     thái trụ mới        cũ có thể   định        
                                              kém phù hợp             

  7           Người lái   Thông tin cập nhật  Giữ hoặc    Chưa có     Manual re-check
                                              đổi trạm    baseline    
  ------------------------------------------------------------------------------------

**Bottleneck chính (2-3 câu):**

``` text
Bottleneck xuất hiện sau khi người lái đã chọn trạm: trạng thái dùng để quyết định ở t0 có thể thay đổi ở t1.
Khi đó người lái phải tự nhận biết thay đổi, mở lại thông tin và đánh giá lại phương án.
Nhóm chưa có baseline đủ tốt cho thời gian re-check nên đây là metric cần đo trong pilot.
```

### 5.2. Future workflow bản nhóm

Phải nhìn ra 5 thứ: bước nào máy (Rule), bước nào AI, bước nào người,
boundary ở đâu, fallback khi AI sai.

``` text
[1 Pull pin/vị trí/trạng thái - máy]
→ [2 Rule loại phương án không an toàn]
→ [3 Workflow/AI re-score khi vượt ngưỡng]
→ [4 Người lái review/xác nhận - boundary]
→ [5 Giữ hoặc đổi route]
→ [6 Tiếp tục monitor]

Fallback: data thiếu/trễ hoặc recommendation không đủ tin cậy
→ hiển thị dữ liệu gốc + danh sách trạm hiện có và để người lái tự chọn.
```

**Before/after impact:**

  ------------------------------------------------------------------------------------
  Metric                                   Trước          Sau kỳ vọng Cách đo
  --------------- ------------------------------ -------------------- ----------------
  Tổng thời gian       Chưa có baseline re-check Giảm so với baseline Bấm giờ /
                                                                pilot interaction log

  Số bước                                      7                    6 So workflow

  Số bước thủ                         Khoảng 4/7                  2/6 Đếm thao tác cần
  công                                                                người

  Bottleneck         Tự kiểm tra và đánh giá lại               Review Quan sát pilot
  chính                                                recommendation 

  Risk mới                              Không có    Data trễ, ranking Log
                    hallucination/recommendation     sai, route churn override/error
                                            risk                      
  ------------------------------------------------------------------------------------

### 5.3. Problem Statement v0 (mỗi field 2-3 câu)

  -----------------------------------------------------------------------
  Field                               Nội dung
  ----------------------------------- -----------------------------------
  **Actor**                           Tài xế Xanh SM và chủ xe VinFast
                                      đang cần sạc trong một hành trình.
                                      Họ là người trực tiếp chọn hoặc đổi
                                      trạm.

  **Workflow**                        Người lái kiểm tra pin, xem trạm,
                                      chọn phương án và bắt đầu di
                                      chuyển. Nếu trạng thái thay đổi, họ
                                      phải tự kiểm tra và quyết định lại.

  **Bottleneck**                      Lựa chọn tại t0 có thể kém phù hợp
                                      ở t1 do pin, trạng thái trụ hoặc
                                      điều kiện di chuyển thay đổi. Người
                                      lái phải tự phát hiện và
                                      re-evaluate.

  **Impact**                          Làm tăng decision effort và có thể
                                      gây đổi route hoặc chờ đợi.
                                      Worksheet có tín hiệu validation
                                      nhưng chưa có baseline gốc đủ để
                                      lượng hóa impact.

  **Success Metric**                  Giảm thời gian và số lần manual
                                      re-check; không tăng số lần
                                      re-route không cần thiết. Theo dõi
                                      thêm tỷ lệ user override.

  **Boundary**                        Hệ thống chỉ monitor, lọc, xếp hạng
                                      và đề xuất. Người lái vẫn xác nhận;
                                      hệ thống không tự lái, tự đổi route
                                      hoặc bảo đảm reservation ngoài khả
                                      năng hiện có.
  -----------------------------------------------------------------------

**Câu hỏi AI phản biện v0 (nếu có):** - Field nào mơ hồ: Impact và
baseline của manual re-check vẫn chưa có số đo gốc; "AI" cũng chưa chắc
cần thiết. - Tôi sửa gì: Giữ decision là `Not Yet`, dùng Rule + Workflow
làm baseline và chỉ thêm AI/ranking nếu pilot chứng minh trade-off khó
xử lý bằng rule.

------------------------------------------------------------------------

## Phase 6 --- Rule / Workflow / Agent + Decision

### 6.0. Ma trận độ phù hợp (suy nghĩ nhanh, không thay quyết định cuối)

-   Độ mơ hồ: \[ \] Thấp (có đúng/sai rõ) / \[x\] Cao (nhiều cách trả
    lời vẫn OK) --- Vì sao: nhiều trạm có thể cùng hợp lệ nhưng khác
    nhau về ETA, buffer pin, availability và độ ổn định.
-   Độ phức tạp: \[ \] Thấp (1-2 bước) / \[x\] Cao (3+ bước/nguồn, phụ
    thuộc nhau) --- Vì sao: cần phối hợp pin, vị trí, trạng thái trạm,
    ETA/traffic và cập nhật theo thời gian.

**Bài toán nhóm nằm ở ô nào:**

``` text
Mơ hồ cao + Phức tạp cao
```

**Vì sao (2-3 câu):**

``` text
Có nhiều phương án cùng hợp lệ và trade-off giữa chúng thay đổi theo thời gian.
Tuy vậy, các bước chính vẫn mô tả trước được nên chưa đủ lý do để chọn Agent.
```

### 6.1. So sánh Rule / Workflow / Agent (so trên cùng 1 bài)

  ----------------------------------------------------------------------------
  Mức            Phương án cho  Khi nào đủ     Rủi ro           Chọn? (Dùng
                 bài toán nhóm                                  cho bước nào?)
  -------------- -------------- -------------- ---------------- --------------
  **Rule**       Loại trạm      Safety filter  Cứng nhắc với    Có, dùng bên
                 không khả      và case đơn    trade-off        trong Workflow
                 dụng, không đủ giản                            
                 buffer pin;                                    
                 trigger khi                                    
                 signal vượt                                    
                 ngưỡng                                         

  **Workflow**   Pull data →    Khi các bước   Phụ thuộc        **Chọn cho
                 Rule filter →  xác định trước data/API; phải   pilot**
                 monitor →      và chỉ cần     xử lý stale data 
                 re-score →     branch hữu hạn                  
                 người lái                                      
                 confirm                                        

  **Agent**      Tự lập kế      Chỉ khi        Khó              Chưa chọn
                 hoạch, gọi     Workflow cố    debug/control;   
                 tool và tự     định chứng     tăng rủi ro      
                 quyết định     minh không đủ  quyết định route 
                 bước tiếp theo                                 
  ----------------------------------------------------------------------------

**5 câu hỏi chốt (trả lời câu đầy đủ):** 1. Rule có giải được 70-80%
case không?\
Chưa có dữ liệu để khẳng định 70-80%, nhưng Rule có thể xử lý phần
safety constraint và các trường hợp đơn giản; đây phải là baseline đầu
tiên.

2.  Các bước có đi thẳng một đường không hay phải rẽ nhánh?\
    Có rẽ nhánh khi signal thay đổi, nhưng các nhánh chính vẫn mô tả
    trước được: giữ route, re-score hoặc fallback về manual choice.

3.  Có thật sự cần Agent tự lập kế hoạch + gọi tool không?\
    Chưa. Workflow xác định trước đã đủ cho pilot và dễ kiểm soát hơn.

4.  Nếu AI sai, ai phát hiện đầu tiên và sửa trong bao lâu?\
    Người lái là người review cuối; nếu recommendation không hợp lý, họ
    có thể bỏ ngay và quay về danh sách trạm/route gốc trong cùng phiên
    sử dụng.

5.  Có hạ được từ Agent → Workflow → Rule không?\
    Có. Nhóm chủ động hạ từ Agent xuống Workflow, đồng thời dùng Rule
    cho safety filter và trigger.

**Mức chọn:**

``` text
Workflow
```

**Vì sao chọn (3-4 câu):**

``` text
Bài toán có nhiều signal và cần monitor theo thời gian nên Rule thuần túy có thể quá cứng.
Tuy nhiên luồng chính vẫn xác định trước được: pull data → filter → monitor → re-score → human confirm.
Workflow vì vậy dễ test, debug và rollback hơn Agent.
AI/ranking chỉ là một step bên trong Workflow, không phải hệ thống tự chủ.
```

**Vì sao không chọn mức đơn giản hơn (2-3 câu):**

``` text
Rule vẫn dùng được cho safety constraint nhưng khó biểu diễn đầy đủ các trade-off giữa ETA, buffer pin và trạng thái trạm khi nhiều phương án cùng hợp lệ.
Vì vậy nhóm chọn Workflow để phối hợp nhiều bước/nguồn, nhưng vẫn giữ Rule làm baseline và lớp an toàn.
```

### 6.2. Problem Statement v1 (v0 sửa chặt hơn + 3 field cuối)

  -----------------------------------------------------------------------
  Field                               Nội dung
  ----------------------------------- -----------------------------------
  **Actor**                           Tài xế Xanh SM và chủ xe VinFast
                                      cần sạc trong một hành trình đang
                                      diễn ra.

  **Workflow**                        Kiểm tra pin → xem/chọn trạm → di
                                      chuyển → hệ thống monitor signal →
                                      đánh giá lại khi vượt ngưỡng →
                                      người lái giữ/đổi phương án.

  **Bottleneck**                      Thông tin dùng để chọn trạm có thể
                                      thay đổi sau quyết định ban đầu,
                                      khiến người lái phải tự phát hiện
                                      và đánh giá lại phương án.

  **Impact**                          Tăng decision effort và có thể tạo
                                      re-route/chờ đợi; mức độ thực tế
                                      cần baseline pilot.

  **Success Metric**                  Giảm thời gian và số lần manual
                                      re-check mà không tăng re-route
                                      không cần thiết; theo dõi user
                                      override.

  **Boundary** (làm / không làm)      Làm: monitor, filter, re-score và
                                      đề xuất. Không làm: tự lái, tự đổi
                                      route, tự bảo đảm reservation.

  **AI intervention point** (can      Sau Rule safety filter và trước
  thiệp sau bước nào, trước bước nào) bước người lái review/xác nhận.

  **Mức chọn** (Rule / Workflow /     Workflow --- vì bài toán nhiều
  Agent + 1 câu vì sao)               bước/nguồn nhưng luồng chính vẫn mô
                                      tả trước được.

  **Rủi ro & người thật kiểm tra**    Rủi ro lớn nhất là stale/wrong data
  (rủi ro lớn nhất + ai kiểm tra bằng làm ranking sai; người lái kiểm tra
  cách nào)                           recommendation và có thể quay về
                                      route/list gốc ngay.
  -----------------------------------------------------------------------

### 6.3. Final decision

  -----------------------------------------------------------------------
  Câu hỏi                 Yes / Not Yet / No      Ghi chú (câu đầy đủ)
  ----------------------- ----------------------- -----------------------
  Actor + workflow rõ     Yes                     Actor, current workflow
  chưa?                                           và future workflow đã
                                                  được thu hẹp rõ.

  Baseline + metric đo    Not Yet                 Có metric cần đo nhưng
  được chưa?                                      chưa có baseline gốc
                                                  cho manual re-check.

  Data/input đủ dùng      Not Yet                 Chưa xác nhận quyền/API
  chưa?                                           và freshness của toàn
                                                  bộ signal cần thiết.

  AI sai, hậu quả chấp    Not Yet                 Human review và
  nhận được không?                                fallback giúp giảm rủi
                                                  ro nhưng cần pilot thực
                                                  tế.

  Có người review/owner   Yes                     Người lái luôn là người
  không?                                          quyết định cuối.

  Có cách non-AI đơn giản Yes                     Rule + deterministic
  hơn không?                                      Workflow là baseline
                                                  phải thử trước.
  -----------------------------------------------------------------------

**Decision:**

``` text
Not Yet
```

**Lý do (3-4 câu dựa trên bằng chứng):**

``` text
Nhóm đã hội tụ được candidate và có tín hiệu validation trong worksheet.
Research cho thấy VinFast đã có nhiều chức năng tìm trạm/route planning, nên problem đã được thu hẹp sang re-evaluation khi trạng thái thay đổi.
Tuy nhiên nhóm chưa có baseline gốc cho manual re-check và chưa xác nhận đủ data/API/freshness.
Vì vậy chưa nên Go trước khi chạy một pilot nhỏ với Rule + Workflow.
```

**Nếu Go --- pilot nhỏ nhất (data nào, chạy tay ra sao, đo 3 số nào):**

``` text
Chưa áp dụng vì Decision hiện tại là Not Yet.
```

**Nếu Not Yet --- cần validate gì trước:**

``` text
1. Lưu evidence gốc của interview/review trong worksheet.
2. Đo baseline thời gian và số lần người dùng phải manual re-check trong một hành trình.
3. Xác nhận availability/freshness của pin, trạng thái trạm và ETA/traffic.
4. Chạy pilot Rule + Workflow trước khi thêm AI/ranking.
```

**Nếu No-Go --- làm gì thay AI:**

``` text
Chưa áp dụng vì Decision hiện tại là Not Yet.
Nếu pilot cho thấy AI/ranking không cải thiện metric, giữ Rule + deterministic Workflow hoặc UI cảnh báo đơn giản.
```

**Exit / rollback (khi nào dừng AI, quay về cách cũ):**

``` text
Dừng recommendation nâng cao và quay về Rule + danh sách/route gốc nếu data thiếu hoặc trễ,
tỷ lệ user override cao, re-route không cần thiết tăng, hoặc pilot không giảm manual re-check.
```

------------------------------------------------------------------------

### Self-check nộp phần 02 (nhóm)

-   [x] Có nhật ký hội tụ 9-12 → 1 (cluster + shortlist + score)
-   [ ] Có validation (quote thật) + research (link kiểm được)
-   [x] Có workflow trước/sau đủ thời gian, handoff, bottleneck,
    boundary, fallback
-   [x] Có PS v0 → v1, metric có trước/sau + cách đo, boundary có
    làm/không làm
-   [x] Có so sánh Rule/Workflow/Agent + Decision Go/Not Yet/No-Go có lý
    do
