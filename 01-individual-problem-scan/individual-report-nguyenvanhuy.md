# 01 --- Individual Problem Scan

## Thông tin cá nhân

-   **Họ và tên:** Nguyễn Văn Huy
-   **Mã học viên:** 2A202602428
-   **Vai trò / bối cảnh:** Nhân viên vận hành tại một chuỗi bán lẻ gồm
    10 cửa hàng *(scenario giả định)*.
-   **Công việc chính:** Theo dõi tồn kho và doanh số; xử lý thiếu hàng;
    phối hợp điều chuyển; lập kế hoạch bổ sung; đối soát chênh lệch tồn
    kho.

> Các số liệu trong bài là **baseline giả định cho scenario** nhằm mô
> phỏng đầy đủ quá trình problem discovery của Day 02. Nếu triển khai
> thực tế, cần thay bằng log, bấm giờ hoặc interview thật.

------------------------------------------------------------------------

## Scan rộng

Scan 10 problems, vượt mức tối thiểu 5.

  ----------------------------------------------------------------------------
  \#             Lăng kính      Problem quan    Ai chịu ảnh    Dấu hiệu thật /
                                sát được        hưởng?         baseline
                                                               scenario
  -------------- -------------- --------------- -------------- ---------------
  1              Lặp lại        Cuối ngày tổng  Nhân viên vận  Khoảng 38
                                hợp doanh thu,  hành, quản lý  phút/ngày
                                số đơn và tồn   vùng           
                                kho từ 10 cửa                  
                                hàng                           

  2              Tốn thời gian  Khi một cửa     Nhân viên vận  Khoảng 17
                                hàng sắp hết    hành, quản lý  phút/case, 5
                                SKU, phải kiểm  cửa hàng       case/ngày
                                tra nhiều chi                  
                                nhánh để tìm                   
                                nguồn điều                     
                                chuyển                         

  3              AI có thể tốt  Khó xác định    Nhân viên vận  Khoảng 55
                 hơn            lượng hàng nên  hành, quản lý  phút/lần lập kế
                                bổ sung cho     cửa hàng       hoạch, 3
                                từng SKU/cửa                   lần/tuần
                                hàng khi tốc độ                
                                bán thay đổi                   

  4              Tốn thời gian  Khi tồn thực tế Nhân viên kho, Khoảng 24
                                lệch hệ thống,  quản lý cửa    phút/case, 6
                                phải lần lại    hàng           case/tuần
                                giao dịch để                   
                                tìm nguyên nhân                

  5              Pain từ người  Nhân viên cửa   Nhân viên bán  Khoảng 12 câu
                 khác           hàng hỏi lại    hàng, quản lý  hỏi/tuần
                                chính sách      cửa hàng       
                                promotion/đổi                  
                                trả vì thông                   
                                tin phân tán                   

  6              Tốn thời gian  Quản lý vùng    Quản lý vùng   Khoảng 35
                                phải đọc báo                   phút/ngày
                                cáo từng cửa                   
                                hàng để tìm                    
                                doanh số/tồn                   
                                kho bất thường                 

  7              Lặp lại        Khi đổi giá     Vận hành, quản Khoảng 45
                                hoặc chạy       lý cửa hàng    phút/campaign
                                promotion, phải                
                                rà nhiều cửa                   
                                hàng đã cập                    
                                nhật đúng chưa                 

  8              Pain từ người  Khi cửa hàng    Nhân viên bán  Khoảng 8
                 khác           hiện tại hết    hàng, khách    phút/yêu cầu
                                hàng, nhân viên hàng           
                                phải tìm và gọi                
                                chi nhánh khác                 
                                để giữ hàng cho                
                                khách                          

  9              Lặp lại        Phải theo dõi   Nhân viên vận  Khoảng 25
                                các yêu cầu     hành           phút/ngày
                                điều chuyển                    
                                đang chờ và                    
                                nhắc cửa hàng                  
                                xác nhận                       

  10             AI có thể tốt  Khó phát hiện   Nhân viên vận  Rà khoảng 200
                 hơn            sớm SKU bán     hành, quản lý  SKU mất 60
                                chậm/dư tồn     vùng           phút/tuần
                                trong danh mục                 
                                lớn                            
  ----------------------------------------------------------------------------

**Vì sao phần scan này hợp lý:**

-   Có scan rộng trước khi hội tụ.
-   Có nhiều lăng kính khác nhau.
-   Tất cả problem nằm trong **cùng một bối cảnh vận hành chuỗi cửa
    hàng**.
-   Mỗi problem có actor và dấu hiệu có thể đo.
-   Không bắt đầu bằng "xây chatbot" hoặc "làm agent".

------------------------------------------------------------------------

## Top 3

  --------------------------------------------------------------------------
  Rank              Problem           Vì sao chọn          Điều còn chưa
                                                           chắc
  ----------------- ----------------- -------------------- -----------------
  1                 Điều chuyển hàng  Workflow rõ, xảy ra  Tồn kho có đủ
                    giữa các cửa hàng thường xuyên, có     real-time không;
                    khi một chi nhánh baseline thời gian   Rule đơn giản có
                    sắp thiếu hàng    và bottleneck cụ thể thể đã đủ tốt

  2                 Đề xuất lượng bổ  Tốn nhiều thời gian, Forecast quality
                    sung tồn kho cho  output cụ thể, có    phụ thuộc dữ liệu
                    từng cửa hàng     thể đo               lịch sử và
                                      stockout/overstock   promotion

  3                 Tìm nguyên nhân   Workflow lặp lại,    Nhiều case có thể
                    chênh lệch tồn    bottleneck rõ ở      giải hoàn toàn
                    kho               transaction history  bằng Rule
                                                           reconciliation
  --------------------------------------------------------------------------

------------------------------------------------------------------------

## Problem Card #1 --- Điều chuyển hàng giữa các cửa hàng khi một chi nhánh sắp thiếu hàng

**Problem 1 câu:**\
Khi một cửa hàng sắp hết một SKU, nhân viên vận hành mất khoảng 17 phút
kiểm tra tồn kho các chi nhánh, safety stock, tốc độ bán và khoảng cách
để chọn cửa hàng nguồn và lượng điều chuyển phù hợp.

**Actor:**\
Nhân viên vận hành chuỗi chịu trách nhiệm đề xuất điều chuyển; quản lý
cửa hàng nguồn và cửa hàng nhận xác nhận.

**Thời điểm / bối cảnh:**\
Khi tồn của một SKU tại một cửa hàng xuống dưới ngưỡng cảnh báo hoặc dự
kiến không đủ bán trong vài ngày tới.

**Current workflow:**

``` text
1. Phát hiện SKU tại cửa hàng A sắp thiếu
2. Mở tồn kho toàn chuỗi
3. Kiểm tra các cửa hàng B/C/D... còn bao nhiêu
4. Kiểm tra safety stock và tốc độ bán của từng nguồn
5. So khoảng cách/thời gian điều chuyển
6. Liên hệ cửa hàng nguồn để xác nhận tồn thực tế
7. Chọn nguồn + số lượng và tạo yêu cầu điều chuyển
```

**Bottleneck:**\
Bước 3--5 --- nhân viên phải tự so sánh nhiều nguồn theo tồn hiện tại,
safety stock, tốc độ bán và khoảng cách. Phần này mất khoảng 9 phút
trong tổng 17 phút/case.

**Impact:**\
Khoảng 17 phút/case × 5 case/ngày = **85 phút/ngày**. Quyết định không
tốt còn có thể chuyển stockout từ cửa hàng nhận sang cửa hàng nguồn.

**Success metric:**\
Giảm thời gian xử lý từ khoảng 17 phút xuống dưới 5 phút/case, đồng thời
không tăng số trường hợp cửa hàng nguồn xuống dưới safety stock sau điều
chuyển.

**Non-AI alternative:**\
Rule cố định: loại các cửa hàng có tồn sau điều chuyển dưới safety
stock, sau đó ưu tiên nguồn gần nhất và đủ số lượng. Đây là baseline cần
thử trước AI.

**AI hypothesis:**\
Workflow tự lấy tồn kho, tốc độ bán và khoảng cách; Rule loại nguồn
không an toàn; thuật toán ranking/AI chỉ hỗ trợ xếp hạng các nguồn còn
hợp lệ. Nhân viên vận hành review trước khi tạo yêu cầu.

**Quick gut:**\
Workflow.

### Draft current workflow

``` text
CURRENT STATE — 17 phút

[1 Phát hiện thiếu: 1']
→ [2 Mở tồn toàn chuỗi: 2']
→ [3 Kiểm tra nguồn: 4']
→ [4 So safety stock + tốc độ bán: 3']  <-- bottleneck
→ [5 So khoảng cách: 2']                <-- bottleneck
→ [6 Liên hệ xác nhận: 3']
→ [7 Tạo yêu cầu: 2']
```

### Draft future workflow

``` text
FUTURE STATE — mục tiêu dưới 5 phút

[1 Auto-detect SKU thiếu: <1']
→ [2 Auto-pull inventory + sales rate: <1']
→ [3 Rule loại nguồn không an toàn: <1']
→ [4 Rank nguồn + lượng đề xuất: <1']
→ [5 Nhân viên review + xác nhận: 2–3']  <-- human boundary
→ [6 Tạo yêu cầu điều chuyển]

Fallback:
Dữ liệu tồn cũ/mâu thuẫn hoặc không có nguồn đạt safety stock
→ bỏ recommendation và kiểm tra thủ công.
```

------------------------------------------------------------------------

## Problem Cards #2 và #3 --- tóm tắt

  -----------------------------------------------------------------------------
  Card        Actor         Bottleneck      Metric      Quick gut   Vì sao chưa
                                                                    chọn làm #1
  ----------- ------------- --------------- ----------- ----------- -----------
  Đề xuất     Nhân viên vận Biến sales      55 phút →   Workflow    Forecast
  lượng bổ    hành /        history + tồn + dưới 30                 quality khó
  sung tồn    merchandise   promotion thành phút/lần                đánh giá
  kho         planner       lượng                                   hơn và phụ
                            replenishment                           thuộc dữ
                                                                    liệu lịch
                                                                    sử

  Tìm nguyên  Nhân viên kho Đọc và nối      24 phút →   Workflow    Nhiều case
  nhân chênh  / quản lý cửa transaction     dưới 10                 có thể giải
  lệch tồn    hàng          timeline để tìm phút/case               bằng Rule;
  kho                       nguyên nhân                             ground
                                                                    truth
                                                                    nguyên nhân
                                                                    khó hơn
  -----------------------------------------------------------------------------

------------------------------------------------------------------------

## Card muốn pitch nhất

**Card #1 --- Điều chuyển hàng giữa các cửa hàng khi một chi nhánh sắp
thiếu hàng.**

**Vì sao chọn:**

-   Workflow 7 bước rõ và xảy ra khoảng 5 lần/ngày.
-   Có baseline khoảng 17 phút/case, trong đó bottleneck nằm ở bước so
    sánh nguồn.
-   Có thể benchmark trực tiếp **Rule vs Workflow**, thay vì mặc định
    phải dùng AI.
-   Impact sau cải tiến đo được bằng thời gian xử lý và tình trạng
    safety stock của cửa hàng nguồn.

**Câu hỏi muốn nhóm challenge:**

1.  Nếu Rule `safety stock + nguồn gần nhất` đã xử lý tốt phần lớn case,
    AI có còn tạo đủ giá trị để đáng triển khai?
2.  Nếu inventory không real-time, bottleneck thật có phải ranking hay
    vẫn là bước gọi cửa hàng xác nhận?

**AI phản biện:**

-   Baseline hiện là scenario giả định, chưa phải evidence thực tế.
-   Data freshness có thể là bottleneck lớn hơn việc lựa chọn thuật
    toán.
-   Không nên dùng Agent: workflow đủ xác định để dùng Rule + Workflow.
-   Human boundary phải nằm trước lúc tạo lệnh điều chuyển.

------------------------------------------------------------------------

### Self-check nộp phần 01

-   [x] Scan 10 problems trước khi hội tụ.
-   [x] Problem cùng một context, có actor và dấu hiệu đo được.
-   [x] Top 3 truy ngược trực tiếp từ scan.
-   [x] Card #1 có workflow, bottleneck, impact và metric rõ.
-   [x] Có Non-AI alternative trước AI hypothesis.
-   [x] Có current/future workflow, human boundary và fallback.
-   [x] Có lý do chọn Workflow thay vì Agent.
