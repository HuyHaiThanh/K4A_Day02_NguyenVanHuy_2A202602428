# 01 --- Individual Problem Scan

> Điền theo Phase 1 + Phase 2 trong `01-worksheet.md`. Tự scan trước,
> dùng AI sau để phản biện. Không bắt đầu từ ý tưởng AI; bắt đầu từ
> actor, workflow và pain.

## Thông tin cá nhân

-   **Họ và tên:** Nguyễn Văn Huy
-   **Mã học viên:** 2A202602428
-   **Bối cảnh giả định:** Nhân viên vận hành tại một chuỗi bán lẻ gồm
    10 cửa hàng.
-   **Công việc chính:** Theo dõi doanh số và tồn kho; xử lý thiếu hàng;
    phối hợp điều chuyển giữa các chi nhánh; kiểm tra chênh lệch tồn;
    tổng hợp báo cáo vận hành.

> **Lưu ý về dữ liệu:** Bài scan sử dụng một tình huống giả định thống
> nhất để thực hành Day 02. Các con số về thời gian/tần suất bên dưới là
> baseline giả định ban đầu và cần được thay bằng số đo hoặc validation
> thật nếu dùng để ra quyết định triển khai.

------------------------------------------------------------------------

## Phase 1 --- Scan rộng

Scan 8 problems trong **cùng một bối cảnh chuỗi cửa hàng bán lẻ**.

  --------------------------------------------------------------------------
  \#             Lăng kính      Problem quan   Ai chịu ảnh    Dấu hiệu thật
                                sát được       hưởng?         / baseline giả
                                                              định
  -------------- -------------- -------------- -------------- --------------
  1              Lặp lại        Cuối ngày phải Nhân viên vận  Mỗi ngày phải
                                tổng hợp doanh hành, quản lý  gom dữ liệu từ
                                thu, số đơn và vùng           10 cửa hàng;
                                tồn kho từ                    giả định mất
                                nhiều cửa hàng                khoảng 30--45
                                để làm báo cáo                phút/ngày
                                vận hành                      

  2              Tốn thời gian  Khi một cửa    Nhân viên vận  Một yêu cầu
                                hàng sắp hết   hành, quản lý  phải kiểm tra
                                hàng, nhân     cửa hàng,      nhiều cửa hàng
                                viên phải kiểm khách mua      rồi liên hệ
                                tra tồn kho                   xác nhận; giả
                                nhiều chi                     định 15--20
                                nhánh để tìm                  phút/lần
                                nơi có thể                    
                                điều chuyển                   

  3              AI có thể tốt  Khó quyết định Nhân viên vận  Cùng SKU có
                 hơn            nên bổ sung    hành, quản lý  thể bán nhanh
                                bao nhiêu hàng cửa hàng       ở cửa hàng A
                                cho từng cửa                  nhưng chậm ở
                                hàng vì tốc độ                B; quyết định
                                bán khác nhau                 thường dựa
                                theo cửa hàng,                nhiều vào kinh
                                ngày và chương                nghiệm
                                trình khuyến                  
                                mãi                           

  4              Lặp lại        Phải đối chiếu Nhân viên kho, Giả định mất
                                tồn kho trên   quản lý cửa    20--30
                                hệ thống với   hàng, vận hành phút/case để
                                kiểm kê thực                  kiểm tra nhập,
                                tế rồi lần lại                bán, trả hàng
                                giao dịch khi                 và điều chuyển
                                có chênh lệch                 

  5              Pain từ người  Nhân viên cửa  Nhân viên bán  Cùng câu hỏi
                 khác           hàng phải hỏi  hàng, quản lý  có thể được
                                lại chính sách cửa hàng,      hỏi lại ở
                                khuyến mãi/đổi khách hàng     nhiều chi
                                trả vì thông                  nhánh; dễ áp
                                tin nằm ở                     dụng nhầm
                                nhiều thông                   phiên bản
                                báo hoặc tài                  chính sách
                                liệu                          

  6              Tốn thời gian  Quản lý vùng   Quản lý vùng,  Phải so nhiều
                                phải đọc báo   nhân viên vận  bảng và nhiều
                                cáo từng cửa   hành           kỳ; bất thường
                                hàng để phát                  nhỏ dễ bị bỏ
                                hiện SKU hoặc                 qua
                                chi nhánh có                  
                                doanh số/tồn                  
                                kho bất thường                

  7              Lặp lại        Khi thay đổi   Vận hành, quản Phải rà nhiều
                                giá hoặc chạy  lý cửa hàng,   SKU/cửa hàng;
                                khuyến mãi,    nhân viên bán  sai giá ảnh
                                vận hành phải  hàng           hưởng trực
                                kiểm tra nhiều                tiếp bán hàng
                                cửa hàng đã                   
                                cập nhật đúng                 
                                hay chưa                      

  8              Pain từ người  Khi sản phẩm   Nhân viên bán  Tồn hệ thống
                 khác           hết ở cửa hàng hàng, khách    có thể chưa đủ
                                hiện tại, nhân hàng           để chắc hàng
                                viên phải tra                 thực sự có thể
                                cứu rồi liên                  bán/giữ cho
                                hệ chi nhánh                  khách
                                khác để xác                   
                                nhận còn hàng                 
                                cho khách                     
  --------------------------------------------------------------------------

### Nhận xét sau scan

Các vấn đề nằm trong cùng một chuỗi vận hành:

``` text
[Bán hàng] → [Cập nhật doanh số/tồn kho] → [Phát hiện SKU sắp thiếu hoặc dư]
→ [Kiểm tra tồn các chi nhánh] → [Quyết định bổ sung/điều chuyển]
→ [Thực hiện điều chuyển] → [Đối soát tồn kho] → [Tổng hợp báo cáo]
```

Pain lặp lại nhiều nhất nằm quanh **tồn kho và điều chuyển giữa các cửa
hàng**, nên Phase 2 ưu tiên các candidate trong cụm này.

------------------------------------------------------------------------

## Phase 2 --- Top 3 Problem Cards

## Top 3

  -----------------------------------------------------------------------
  Rank              Problem           Vì sao chọn       Điều còn chưa
                                                        chắc
  ----------------- ----------------- ----------------- -----------------
  1                 Điều chuyển hàng  Actor/workflow    Tồn hệ thống có
                    giữa các cửa hàng rõ; nhiều bước    real-time không;
                    khi một chi nhánh thủ công; impact  chưa có baseline
                    sắp thiếu hàng    đo được bằng thời thật; cần safety
                                      gian xử lý, số    stock cho cửa
                                      lần liên hệ và    hàng nguồn
                                      chất lượng điều   
                                      chuyển            

  2                 Đề xuất lượng bổ  Cùng domain;      Mùa vụ/promotion
                    sung tồn kho cho  input rõ như      làm nhu cầu biến
                    từng cửa hàng     sales history,    động; thiếu lịch
                                      tồn, tốc độ bán,  sử sẽ làm dự báo
                                      promotion; so     yếu
                                      được Rule với     
                                      forecasting/AI    

  3                 Phát hiện và tìm  Workflow lặp lại; Nguyên nhân đa
                    nguyên nhân chênh bottleneck rõ ở   dạng; cần
                    lệch tồn kho      bước lần giao     transaction data
                                      dịch; output kiểm và ground truth
                                      chứng được        
  -----------------------------------------------------------------------

## Problem Card #1 --- Điều chuyển hàng giữa các cửa hàng khi một chi nhánh sắp thiếu hàng

**Problem 1 câu:**\
Khi một cửa hàng sắp hết một SKU nhưng các cửa hàng khác vẫn còn hàng,
nhân viên vận hành mất thời gian kiểm tra nhiều chi nhánh, cân nhắc nhu
cầu của cả cửa hàng nguồn và cửa hàng nhận rồi mới quyết định điều
chuyển từ đâu và bao nhiêu.

**Actor:**\
Nhân viên vận hành chuỗi ra đề xuất; quản lý cửa hàng nguồn và cửa hàng
nhận xác nhận; khách hàng chịu ảnh hưởng nếu cửa hàng thiếu hàng.

**Thời điểm / bối cảnh:**\
Khi tồn một SKU tại cửa hàng giảm xuống mức thấp hoặc nhu cầu dự kiến
vượt lượng tồn trong vài ngày tới.

**Current workflow:**

``` text
1. Phát hiện SKU tại cửa hàng A sắp thiếu.
2. Mở báo cáo tồn kho các cửa hàng.
3. Kiểm tra B/C/D... còn bao nhiêu.
4. Xem tốc độ bán của cửa hàng nguồn.
5. So khoảng cách/thời gian điều chuyển.
6. Liên hệ cửa hàng nguồn xác nhận hàng thực tế.
7. Chọn nguồn + số lượng và tạo yêu cầu điều chuyển.
```

**Bottleneck:**\
Bước 3--5: phải tự so sánh nhiều cửa hàng và cân bằng tồn hiện tại, tốc
độ bán, khoảng cách và nhu cầu của cửa hàng nhận. Chọn nơi "còn nhiều
nhất" chưa chắc đúng vì có thể khiến cửa hàng nguồn thiếu hàng sau đó.

**Impact:**\
Baseline giả định 15--20 phút/yêu cầu. Nếu có 5 yêu cầu/ngày, riêng việc
tìm nguồn và quyết định có thể tốn khoảng 75--100 phút/ngày.

**Success metric:**\
Giảm thời gian từ lúc phát hiện thiếu hàng đến lúc có đề xuất từ 15--20
phút xuống dưới 5 phút/case; giảm số cửa hàng phải liên hệ; không tăng
số trường hợp cửa hàng nguồn xuống dưới safety stock sau điều chuyển.

**Non-AI alternative:**\
Rule cố định: chỉ lấy từ cửa hàng có tồn sau điều chuyển lớn hơn safety
stock, ưu tiên cửa hàng gần và giới hạn số lượng theo min/max stock. Đây
là baseline phải thử trước AI.

**AI hypothesis:**\
Workflow tự lấy tồn kho, tốc độ bán và khoảng cách; Rule loại nguồn
không an toàn; AI/thuật toán ranking hỗ trợ xếp hạng khi nhiều nguồn đều
hợp lệ. Nhân viên vẫn review trước khi tạo yêu cầu.

**Quick gut:**\
Workflow.

### Draft current workflow

``` text
CURRENT STATE — baseline giả định 15–20 phút/case

[1 Phát hiện thiếu: 1']
→ [2 Mở tồn chuỗi: 2']
→ [3 Kiểm tra từng cửa hàng: 5']       <-- bottleneck
→ [4 So tốc độ bán/tồn an toàn: 4']    <-- bottleneck
→ [5 So khoảng cách: 2']
→ [6 Liên hệ xác nhận: 4']
→ [7 Tạo yêu cầu: 2']
```

### Draft future workflow

``` text
FUTURE STATE — target dưới 5 phút/case

[1 Auto-detect SKU thiếu]                 -- Rule
→ [2 Pull tồn + sales rate + khoảng cách] -- Workflow
→ [3 Loại nguồn dưới safety stock]        -- Rule
→ [4 Rank nguồn + số lượng]               -- Workflow/AI support
→ [5 Nhân viên review + xác nhận: 2–3']   -- Human boundary
→ [6 Tạo yêu cầu điều chuyển]

Fallback:
Dữ liệu tồn cũ/mâu thuẫn, không có nguồn an toàn hoặc confidence thấp
→ kiểm tra và gọi xác nhận thủ công.
```

## Problem Card #2 --- Đề xuất lượng bổ sung tồn kho cho từng cửa hàng

**Problem 1 câu:**\
Nhân viên vận hành khó xác định mỗi cửa hàng nên được bổ sung bao nhiêu
đơn vị cho từng SKU vì nhu cầu khác nhau theo vị trí, tốc độ bán, ngày
trong tuần và chương trình khuyến mãi.

**Actor:**\
Nhân viên vận hành/merchandise planner lập kế hoạch; quản lý cửa hàng
nhận hàng; kho trung tâm chuẩn bị hàng.

**Thời điểm / bối cảnh:**\
Theo chu kỳ bổ sung hàng hằng ngày/vài lần mỗi tuần và trước promotion.

**Current workflow:**

``` text
1. Xuất tồn hiện tại.
2. Xem doanh số lịch sử.
3. Kiểm tra promotion.
4. Ước lượng nhu cầu từng SKU/cửa hàng.
5. So với tồn và hàng đang về.
6. Chỉnh số lượng theo kinh nghiệm.
7. Gửi kế hoạch bổ sung.
```

**Bottleneck:**\
Bước 4--6: phải biến nhiều tín hiệu thành số lượng replenishment cụ thể.
Rule cố định có thể không phù hợp cho SKU bán nhanh, mùa vụ hoặc cửa
hàng có hành vi khách khác nhau.

**Impact:**\
Bổ sung thiếu gây stockout; bổ sung quá nhiều làm tăng tồn và điều
chuyển ngược. Chưa có dữ liệu thật để lượng hóa.

**Success metric:**\
So trên một nhóm SKU: tỷ lệ stockout, số ngày tồn kho, tồn cuối kỳ và số
lần điều chuyển khẩn cấp. Mục tiêu là giảm stockout mà không làm tồn
bình quân tăng quá baseline.

**Non-AI alternative:**\
Min/max inventory, reorder point và moving average theo SKU/cửa hàng.

**AI hypothesis:**\
Forecast nhu cầu ngắn hạn từ sales history, tồn, ngày trong tuần và
promotion; Workflow chuyển forecast thành đề xuất có constraint; người
vận hành review.

**Quick gut:**\
Workflow.

### Draft current workflow

``` text
CURRENT STATE

[Xuất tồn] → [Xem sales history] → [Xem promotion]
→ [Ước lượng nhu cầu]  <-- bottleneck
→ [Tính lượng bổ sung] → [Chỉnh theo kinh nghiệm] → [Gửi kế hoạch]
```

### Draft future workflow

``` text
FUTURE STATE

[Pull sales + inventory + promotion]
→ [Rule kiểm tra dữ liệu]
→ [Forecast nhu cầu theo SKU/cửa hàng]
→ [Rule tính replenishment + min/max]
→ [Nhân viên review ngoại lệ]  -- Human boundary
→ [Gửi kế hoạch]

Fallback:
SKU mới/dữ liệu ít/promotion bất thường
→ dùng min/max + moving average và người vận hành quyết định.
```

## Problem Card #3 --- Phát hiện và tìm nguyên nhân chênh lệch tồn kho

**Problem 1 câu:**\
Khi tồn thực tế khác tồn trên hệ thống, nhân viên phải lần nhiều giao
dịch bán, nhập, trả và điều chuyển để tìm nguyên nhân.

**Actor:**\
Nhân viên kho/cửa hàng kiểm kê; quản lý cửa hàng và vận hành xử lý chênh
lệch.

**Thời điểm / bối cảnh:**\
Sau kiểm kê định kỳ hoặc khi phát hiện tồn hệ thống không khớp thực tế.

**Current workflow:**

``` text
1. Ghi nhận kiểm kê thực tế.
2. So với tồn hệ thống.
3. Xác định SKU bị lệch.
4. Lấy lịch sử bán/nhập/trả/điều chuyển.
5. Đọc từng giao dịch để tìm bất thường.
6. Liên hệ nếu thiếu chứng từ.
7. Xác nhận nguyên nhân và xử lý.
```

**Bottleneck:**\
Bước 4--6: phải tự nối timeline từ nhiều loại giao dịch. Case qua nhiều
lần transfer/return dễ kéo dài.

**Impact:**\
Baseline giả định 20--30 phút/case. Chậm xử lý làm tồn kho kém tin cậy
và ảnh hưởng tiếp tới bán hàng, replenishment và transfer.

**Success metric:**\
Giảm thời gian điều tra/case; giảm số giao dịch phải đọc; đo tỷ lệ
nguyên nhân đúng xuất hiện trong top 3 gợi ý. Không tự điều chỉnh tồn
nếu chưa có người xác nhận.

**Non-AI alternative:**\
Rule reconciliation theo transaction ID; cảnh báo duplicate, transfer
chưa nhận, return chưa hoàn tất hoặc giao dịch thiếu cặp.

**AI hypothesis:**\
Rule xử lý pattern rõ; AI tóm tắt timeline và xếp hạng nguyên nhân ở
case còn lại. Nhân viên xem chứng từ gốc trước khi xác nhận.

**Quick gut:**\
Workflow.

### Draft current workflow

``` text
CURRENT STATE — baseline giả định 20–30 phút/case

[Kiểm kê] → [So system stock] → [Xác định SKU lệch]
→ [Lấy transaction history] → [Đọc/lần timeline]  <-- bottleneck
→ [Liên hệ xác minh] → [Xác nhận nguyên nhân]
```

### Draft future workflow

``` text
FUTURE STATE

[Physical count + system stock]
→ [Rule phát hiện mismatch]
→ [Rule kiểm duplicate/missing transfer/return]
→ [AI tóm tắt timeline + rank nguyên nhân]
→ [Nhân viên xem chứng từ và xác nhận]  -- Human boundary
→ [Xử lý]

Fallback:
Thiếu transaction/chứng từ hoặc AI không có bằng chứng
→ giữ trạng thái chưa xác minh và điều tra thủ công.
```

## Card muốn pitch nhất

**Card đề xuất để pitch:**\
Card #1 --- Điều chuyển hàng giữa các cửa hàng khi một chi nhánh sắp
thiếu hàng.

**Vì sao:**\
Problem có actor cụ thể, workflow lặp lại và bottleneck rõ ở bước chọn
cửa hàng nguồn + số lượng. Metric trước/sau dễ đo bằng thời gian xử lý,
số lần liên hệ và khả năng giữ safety stock cho cửa hàng nguồn. Bài toán
cũng cho phép so Rule/Workflow/Agent rõ: Rule xử lý constraint cứng,
Workflow tổng hợp dữ liệu và ranking; chưa cần Agent.

**Câu hỏi đề xuất để nhóm challenge:**

1.  Nếu `safety stock + cửa hàng gần nhất` đã giải được phần lớn case,
    AI còn tạo giá trị gì?
2.  Tồn kho có đủ real-time hay vẫn phải gọi cửa hàng xác nhận?
3.  Nếu cửa hàng B đang dư nhưng tốc độ bán cũng tăng nhanh, làm sao
    tránh chuyển sang A rồi khiến B thiếu?
4.  Nên tối ưu thời gian ra quyết định hay tỷ lệ stockout toàn chuỗi?

**AI phản biện Card:** - Baseline 15--20 phút/case và 5 case/ngày hiện
là **giả định scenario**, không phải evidence thật. - Trước AI phải
benchmark với `safety stock + distance + sales rate`. - Data freshness
là dependency quan trọng. - Human boundary nằm trước lúc tạo lệnh điều
chuyển; không tự chuyển nếu dữ liệu mâu thuẫn.

### Self-check nộp phần 01

-   [x] Phase 1 có 8 vấn đề trong **một bối cảnh thống nhất: vận hành
    chuỗi cửa hàng bán lẻ**.
-   [x] Có nhiều lăng kính và mỗi problem có actor/dấu hiệu.
-   [x] Số liệu giả định được ghi rõ, không giả thành evidence thật.
-   [x] Top 3 truy ngược trực tiếp về Phase 1 và cùng cụm
    inventory/retail operations.
-   [x] Cả 3 card có actor, workflow, bottleneck, impact, metric, non-AI
    alternative và AI hypothesis.
-   [x] Có before/after workflow, human boundary và fallback.
-   [x] Không bắt đầu bằng chatbot/agent; Rule và non-AI alternative
    được xét trước.
-   [ ] Cần thay baseline giả định bằng quan sát/interview/log thật nếu
    dùng để ra quyết định triển khai.
