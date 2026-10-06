# [Sáng tạo] THIẾT KẾ MÔ HÌNH VẬN HÀNH AGILE CHO TOÀN MẢNG SẢN PHẨM

## Phần 1 - Kiến trúc mô hình

### 1.1. Các module quy trình và vai trò

Mô hình vận hành Agile cho mảng RikkeiGo được thiết kế dựa trên khung Scrum, với các module quy trình rõ ràng và phân tách trách nhiệm như sau:

*   **Module 1: Thu thập và Quản lý Tầm nhìn Sản phẩm (Product Vision & Strategy)**
    *   **Mục tiêu:** Định hình tầm nhìn dài hạn, chiến lược sản phẩm, và các mục tiêu kinh doanh.
    *   **Vai trò chính:** Product Owner (chịu trách nhiệm cuối cùng), cùng với Ban lãnh đạo và các bên liên quan (Stakeholders).
    *   **Artifacts liên quan:** Product Goal, Product Backlog (cấp độ Epic/Feature).

*   **Module 2: Lập kế hoạch và Ưu tiên Sản phẩm (Product Backlog Management)**
    *   **Mục tiêu:** Liên tục tinh chỉnh, ước lượng và sắp xếp thứ tự ưu tiên cho các hạng mục trong Product Backlog dựa trên giá trị kinh doanh, rủi ro, và phản hồi từ người dùng.
    *   **Vai trò chính:** Product Owner.
    *   **Sự kiện liên quan:** Product Backlog Refinement (hoạt động liên tục, không phải sự kiện Scrum chính thức nhưng rất quan trọng).
    *   **Artifacts liên quan:** Product Backlog (bao gồm User Stories, bugs, technical debt).

*   **Module 3: Thực thi Sprint (Sprint Execution)**
    *   **Mục tiêu:** Chuyển đổi các hạng mục ưu tiên cao từ Product Backlog thành các Increment có khả năng phát hành trong một khoảng thời gian cố định (Sprint).
    *   **Sự kiện liên quan:**
        *   **Sprint Planning:** Scrum Team (Product Owner, Developers, Scrum Master) cùng nhau chọn hạng mục từ Product Backlog, xác định Sprint Goal, và tạo Sprint Backlog.
        *   **Daily Scrum:** Developers kiểm tra tiến độ đạt được Sprint Goal và điều chỉnh kế hoạch làm việc trong 24 giờ tới.
    *   **Vai trò chính:** Developers (thực hiện công việc), Product Owner (làm rõ yêu cầu), Scrum Master (hỗ trợ quá trình).
    *   **Artifacts liên quan:** Sprint Backlog, Increment (đang trong quá trình hình thành).

*   **Module 4: Đánh giá và Phản hồi Sản phẩm (Product Review & Feedback)**
    *   **Mục tiêu:** Thanh tra Increment đã hoàn thành và nhận phản hồi từ các bên liên quan để định hướng các Sprint tiếp theo.
    *   **Sự kiện liên quan:** **Sprint Review:** Scrum Team trình bày Increment "Done" cho Stakeholders, Product Owner giải thích Product Backlog hiện tại, và cùng nhau thảo luận về các bước tiếp theo. Đây là cơ hội để thể hiện sự **MINH BẠCH** và **THANH TRA** sản phẩm.
    *   **Vai trò chính:** Scrum Team, Stakeholders.
    *   **Artifacts liên quan:** Increment "Done", Product Backlog (có thể được cập nhật sau Review).

*   **Module 5: Cải tiến Quy trình (Process Improvement)**
    *   **Mục tiêu:** Liên tục thanh tra cách thức làm việc của Scrum Team và xác định các cải tiến để nâng cao hiệu quả và sự hài lòng.
    *   **Sự kiện liên quan:** **Sprint Retrospective:** Scrum Team thảo luận về Sprint vừa qua, xác định điều gì đã đi tốt, điều gì cần cải thiện, và tạo ra một kế hoạch cải tiến cho Sprint tiếp theo. Đây là cơ hội để thực hiện sự **THÍCH NGHI** về quy trình.
    *   **Vai trò chính:** Scrum Team.

### 1.2. Vị trí của đội Đối soát trong mô hình chung

Đội Đối soát **không áp dụng hoàn toàn** mô hình Scrum chung với nhịp Sprint và các sự kiện giống như các đội Đặt xe và Thanh toán.
**Lý do:** Công việc của đội Đối soát có tính chất đặc thù, yêu cầu sự ổn định cao và tuân thủ chặt chẽ các quy định pháp luật, đặc biệt là quy định thuế. Các yêu cầu về tính năng hoặc sản phẩm ít thay đổi đột ngột so với các đội phát triển. Việc áp dụng chu kỳ Sprint cố định và các sự kiện Scrum thường xuyên có thể tạo ra gánh nặng không cần thiết và không tối ưu cho tính chất công việc của họ.
Thay vào đó, đội Đối soát sẽ áp dụng **các nguyên tắc Agile** như minh bạch, kiểm tra và thích nghi trong cách làm việc, nhưng có thể sử dụng một khung làm việc khác như **Kanban** để quản lý dòng chảy công việc, hoặc một phiên bản Scrum được điều chỉnh với chu kỳ "Sprint" dài hơn (ví dụ: theo chu kỳ báo cáo/quy định), phù hợp hơn với đặc thù công việc ổn định và dựa trên tuân thủ. Điều này giúp họ giữ được tinh thần cải tiến liên tục mà vẫn đảm bảo tính hiệu quả và tuân thủ các quy định.

### 1.3. Luồng giá trị từ nhu cầu người dùng đến cải tiến tiếp theo

Luồng giá trị của RikkeiGo được thiết kế để khép kín, liên tục thu thập phản hồi và thúc đẩy cải tiến, thể hiện rõ 3 trụ cột của Scrum: Minh bạch (Transparency), Thanh tra (Inspection), và Thích nghi (Adaptation).

**1. Nhu cầu & Cơ hội Kinh doanh** (Từ thị trường, người dùng, ban lãnh đạo)
    ⬇ (Thu thập & Phân tích)
**2. Product Vision & Mục tiêu Sản phẩm** (Định hướng bởi Product Owner)
    ⬇ (Hình thành & Ưu tiên) - **MINH BẠCH** Product Backlog
**3. Product Backlog** (Danh sách các hạng mục đã được tinh chỉnh và ưu tiên bởi Product Owner)
    ⬇ (Lập kế hoạch Sprint) - **Sự kiện: Sprint Planning** (Scrum Team chọn Sprint Goal và các hạng mục)
**4. Sprint Backlog** (Kế hoạch làm việc của Developers trong Sprint)
    ⬇ (Thực thi & Tự quản lý) - **Sự kiện: Daily Scrum** (Developers thanh tra tiến độ & điều chỉnh kế hoạch - **THANH TRA, THÍCH NGHI**)
**5. Phát triển Increment** (Developers làm việc để hoàn thành các hạng mục theo Definition of Done)
    ⬇ (Hoàn thành theo DoD) - **MINH BẠCH** Increment "Done"
**6. Increment "Done"** (Sản phẩm có giá trị, có khả năng phát hành)
    ⬇ (Đánh giá Increment) - **Sự kiện: Sprint Review** (Scrum Team & Stakeholders thanh tra Increment, cập nhật Product Backlog - **MINH BẠCH, THANH TRA**)
**7. Phản hồi & Học hỏi** (Từ người dùng thực tế và các bên liên quan sau Sprint Review/Triển khai)
    ⬇ (Cải tiến quy trình) - **Sự kiện: Sprint Retrospective** (Scrum Team thanh tra cách làm việc & thích nghi - **THANH TRA, THÍCH NGHI**)
**8. Cải tiến cho Sprint tiếp theo** (Cập nhật quy trình làm việc, hành động cải tiến)
    ⬇ (Quay lại bước 3: Cập nhật Product Backlog và bắt đầu Sprint mới)

## Phần 2 - Xử lý tình huống

### Tình huống 1: Đến buổi Sprint Review nhưng không có hạng mục nào đạt tiêu chuẩn "xong".

*   **Nơi phát hiện:**
    *   Chính thức: Sự kiện Sprint Review.
    *   Trên thực tế: Có thể được nhận thấy sớm hơn trong Daily Scrum hoặc qua công cụ quản lý Sprint Backlog khi không có hạng mục nào đạt Definition of Done (DoD).
*   **Ai xử lý:**
    *   **Scrum Master:** Hỗ trợ nhóm nhận ra vấn đề, tạo môi trường an toàn để nhóm thanh tra và thích nghi.
    *   **Developers:** Chịu trách nhiệm thực hiện công việc và đảm bảo đạt DoD.
    *   **Product Owner:** Quản lý kỳ vọng của các bên liên quan và điều chỉnh Product Backlog.
*   **Cách xử lý:**
    1.  **Tại Sprint Review:** Scrum Team cần minh bạch báo cáo rằng không có Increment nào "Done" để giới thiệu. Product Owner cần giải thích tình hình (mà không đổ lỗi) cho các bên liên quan và tập trung vào những gì đã học được từ Sprint. Điều này nhấn mạnh trụ cột **Minh bạch**.
    2.  **Tại Sprint Retrospective (ngay sau đó):** Đây sẽ là trọng tâm chính của buổi Retrospective.
        *   Scrum Team cần **Thanh tra** lý do cốt lõi tại sao không có hạng mục nào đạt DoD. Các câu hỏi có thể bao gồm: Definition of Done có thực tế không? Ước lượng có chính xác không? Có trở ngại nào không được xử lý kịp thời không? Có sự phân tán hay thay đổi phạm vi nào trong Sprint không?
        *   Nhóm sẽ cùng nhau xác định các hành động cụ thể để **Thích nghi** và cải thiện cho Sprint tiếp theo, ví dụ:
            *   Điều chỉnh Definition of Done (nếu không thực tế).
            *   Cải thiện kỹ thuật ước lượng hoặc giảm cam kết công việc trong Sprint Planning.
            *   Cải thiện khả năng phát hiện và giải quyết trở ngại của Scrum Master.
            *   Tăng cường sự tập trung của Developers vào Sprint Goal.
            *   Product Owner làm việc với Developers để bảo vệ Sprint Goal tốt hơn khỏi sự thay đổi.
    3.  **Hạng mục chưa "xong":** Các hạng mục chưa đạt DoD sẽ không được coi là một phần của Increment và sẽ được đưa trở lại Product Backlog để Product Owner ưu tiên lại.

### Tình huống 2: Đội Thanh toán muốn kéo dài riêng Sprint đang chạy thêm 1 tuần để "làm cho xong", trong khi các đội khác giữ nhịp cũ.

*   **Nơi phát hiện:** Trực tiếp từ đề xuất của Đội Thanh toán đến Scrum Master, Product Owner hoặc trong cuộc họp Daily Scrum.
*   **Ai xử lý:**
    *   **Scrum Master:** Là người chịu trách nhiệm bảo vệ và huấn luyện Scrum Team tuân thủ khung Scrum.
    *   **Product Owner:** Làm việc với Developers để điều chỉnh phạm vi Sprint nếu cần thiết.
    *   **Developers:** Chịu trách nhiệm tự quản lý để đạt được Sprint Goal trong thời gian cố định.
*   **Cách xử lý:**
    1.  **Nguyên tắc Scrum:** Scrum Master phải nhấn mạnh rằng thời lượng Sprint là **cố định (time-boxed)** và tuyệt đối không được kéo dài. Việc kéo dài Sprint sẽ phá vỡ nhịp điệu cố định của Scrum, làm giảm khả năng dự đoán và khả năng thanh tra, thích nghi đều đặn. Các đội khác giữ nhịp cũ cũng củng cố tầm quan trọng của nhịp điệu chung.
    2.  **Scrum Master & Product Owner cùng Developers:**
        *   **Thanh tra & Thích nghi ngay lập tức:** Thay vì kéo dài Sprint, nhóm cần **thanh tra** lý do tại sao họ không thể hoàn thành công việc trong thời gian đã định.
        *   **Điều chỉnh phạm vi:** Product Owner cùng với Developers sẽ xem xét Sprint Backlog. Nếu một phần của Sprint Goal đã đạt được, nhóm cần tập trung vào việc hoàn thành những hạng mục quan trọng nhất để đạt được một Sprint Goal khả thi (có thể điều chỉnh nhỏ). Các hạng mục chưa "xong" hoặc không còn cần thiết để đạt Sprint Goal sẽ được đưa trở lại Product Backlog, được Product Owner ưu tiên lại cho các Sprint sau. Điều này đòi hỏi sự **Minh bạch** về khả năng của nhóm và sự **Thích nghi** với thực tế.
        *   **Kết thúc đúng hạn:** Sprint phải kết thúc đúng ngày đã định. Increment "Done" (nếu có) sẽ được giới thiệu tại Sprint Review.
    3.  **Tại Sprint Retrospective:** Nhóm cần thảo luận về nguyên nhân dẫn đến việc không hoàn thành công việc và đề xuất kéo dài Sprint. Các hành động cải tiến có thể bao gồm: cải thiện kỹ thuật ước lượng, giảm cam kết công việc trong Sprint Planning, tăng cường sự phối hợp nội bộ, hoặc Scrum Master loại bỏ trở ngại hiệu quả hơn. Mục tiêu là học hỏi từ sai lầm để cam kết thực tế hơn trong các Sprint tiếp theo.