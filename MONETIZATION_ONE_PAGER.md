# 📑 MONETIZATION ONE-PAGER: VINSTAY AI
> **Sản phẩm:** VinStay AI — Nền tảng Điều phối Cho thuê Căn hộ Độc quyền tại Đại đô thị Vinhomes Ocean Park (Gia Lâm, Hà Nội).  
> **Tác giả:** Đội P-010 (AI20K Build Phase) — Nguyễn Khánh Duy.  
> **Phiên bản mô hình:** v1.0 (Chốt ngày 08/10/2026).  
> **File số liệu gốc:** [`day22_monetization_model.xlsx`](file:///Users/duy/Desktop/lab%2022/day22_monetization_model.xlsx).

---

## 1. KHỐI PRICING & ĐỊNH GIÁ (UNIT ECONOMICS)

* **Định vị & Ngân sách khách hàng (Budget Line):**
  * Định vị: Dịch vụ AI điều phối quản lý cho thuê căn hộ trọn gói — thay thế hoàn toàn môi giới truyền thống, giúp chủ nhà nội thành cắt giảm 100% việc đi lại 25km mở cửa và lấp đầy phòng trống nhanh gấp 3 lần.
  * Túi ngân sách: **Ngân sách Môi giới & Vận hành cho thuê (Brokerage Commission Budget)** của chủ hộ (tiền trích từ dòng tiền cho thuê căn hộ, không qua bộ phận CNTT, chủ nhà tự duyệt ngay lập tức).
* **Value Metric chốt:** **Outcome-Based (Phí hoa hồng theo giao dịch thành công)** = **50% tiền thuê tháng đầu tiên** (trung bình **3.500.000 VNĐ / giao dịch** $\approx$ **$134.60**). Miễn phí 100% phí đăng tin, niêm yết ban đầu.
* **Cơ sở lựa chọn (Decision Note 3 câu):**
  1. *Lựa chọn:* VinStay AI chọn Value Metric là Outcome-Based: Phí hoa hồng thành công 50% tiền thuê tháng đầu tiên (3.500.000 VNĐ / giao dịch chốt thành công), không thu phí duy trì hay phí đăng tin.
  2. *Attribution & Autonomy:* Attribution đo được 100% vì giao dịch chỉ hoàn tất khi khách quét VietQR cọc 2 triệu và ký hợp đồng thuê số qua OTP; Autonomy đạt 80% do AI xử lý toàn bộ khâu matching, thẩm định All-in và gen hợp đồng, con người chỉ đóng vai trò Field Host quẹt thẻ sảnh.
  3. *Lý do thị trường defendable:* Thị trường BĐS Việt Nam đã quen trả 1 tháng tiền thuê cho môi giới truyền thống; việc VinStay AI chỉ thu 50% tiền thuê theo kết quả giúp loại bỏ 100% rào cản chi phí ban đầu của chủ nhà, tạo lợi thế cạnh tranh áp đảo so với bất kỳ mô hình thu phí phần mềm (SaaS) hay thu phí đăng tin nào.
* **Chi phí Cost/Job (Mẫu số Job Hoàn thành):** **630.000 VNĐ** (~**$24.23 / deal**), gồm đủ 5 thành phần:
  1. *LLM API (gpt-4o-mini có prompt caching):* 1.170 VNĐ ($0.045).
  2. *Infra (Vector DB, Supabase S3 ảnh CCCD, Zalo OTP, VietQR):* 1.560 VNĐ ($0.060).
  3. *Retry (6% do lỗi ảnh chụp hoặc timeout mạng):* 70 VNĐ ($0.003).
  4. *HITL (Field Host dẫn phòng 3 lượt x 80.000đ + Admin QA hợp đồng):* 253.000 VNĐ ($9.73).
  5. *Overhead phân bổ & Dự phòng cọc:* 363.000 VNĐ ($13.96).
  *(Đã chia cho mẫu số 1 Giao dịch hoàn thành, đã gánh chi phí cho 10 khách chat và 3 lượt xem phòng không chốt).*
* **Khoảng giá (Price Window):**
  * *Giá sàn kỹ thuật:* $3 \times \text{Cost/Job} = 1.890.000 \text{ VNĐ}$ ($72.69).
  * *Giá bán đề xuất:* **3.500.000 VNĐ** ($134.60).
  * *Giá trần thị trường:* **7.000.000 VNĐ** (Môi giới truyền thống thu 1 tháng thuê).
* **Gross Margin (GM%):** Đạt **82.0%** (ở kịch bản 3 lượt dẫn phòng/deal) và duy trì **72.4%** khi tính gộp toàn bộ bảo hiểm rủi ro cọc. $\rightarrow$ **PASS KIỂM ĐỊNH ($\ge 60\%$)**.
* **Breakeven Containment & Ngưỡng sinh tử:** Mô hình duy trì Gross Margin $\ge 60\%$ chừng nào số lượt dẫn phòng $\le 9$ lượt / deal chốt (tỷ lệ chốt $\ge 11\%$).

---

## 2. KHỐI GO-TO-MARKET (GTM & CHANNEL FIT)

* **Kênh phân phối DUY NHẤT cho 90 ngày:** **Partner-Led** — Hợp tác độc quyền với **Ban Quản trị Cụm Tòa Chung cư Sapphire 1 & 2** và **Ban Quản trị Group Facebook Cư dân Vinhomes Ocean Park (120.000 thành viên)** cùng Zalo Mini App cư dân.
* **Chứng minh số liệu CAC Affordability:**
  * $\text{ARPU} = 3.500.000 \text{ VNĐ}$; $\text{Gross Margin} = 82\%$; $\text{Payback cho phép} = 3 \text{ tháng}$ (thực tế payback = 0 tháng vì thu tiền ngay khi cọc).
  * $\text{Ngân sách CAC tối đa cho phép} = 3.500.000 \times 82\% \times 3 = \mathbf{8.610.000 \text{ VNĐ}}$ (~**$331.15 / khách**).
  * $\text{CAC thực tế ước tính qua Partner-Led} = \mathbf{450.000 \text{ VNĐ}}$ (~**$17.30 / deal** - chiết khấu 10% phí cho quỹ bảo trì BQL và quà tặng).
  * $\text{Tỷ lệ CAC thực tế / Ngân sách CAC} = 5.2\%$ $\rightarrow$ Kênh cực kỳ an toàn và thặng dư biên lớn.
* **Kiểm chứng Inside Sales:** $\text{Quota năm 1.2 tỷ} / \text{ACV 3.5 triệu} = 1.37 \text{ deal/ngày}$ $\rightarrow$ **BẤT KHẢ THI** nếu dùng đội telesale truyền thống (không thể chốt $>1$ deal BĐS/ngày/người).
* **Pain Moment (Đủ 3 yếu tố):**
  * *Mấy giờ:* **15:30 chiều Chủ nhật** (hoặc 21:00 tối).
  * *Đang làm gì:* Chủ nhà sống tại Cầu Giấy (cách Ocean Park 25km) nhận tin nhắn khách hẹn xem căn hộ lúc 16:30; nếu đi thì mất 2 tiếng kẹt xe nắng mưa, nếu không đi thì sợ mất khách và phòng trống thêm 1 tuần mất 2 triệu tiền thuê.
  * *Ở đâu / Ứng dụng nào:* Đang mở ứng dụng **Zalo** trên điện thoại.
* **Điểm nhúng không ma sát (Zero Friction):** Tích hợp trực tiếp trên **Zalo OA / Mini App của VinStay AI**. Chủ nhà chỉ bấm 1 nút *"Ủy quyền Field Host mở cửa"*, Field Host nội khu tự đón khách quẹt thẻ sảnh. Không bắt chủ nhà tải app mới hay đăng ký tài khoản web riêng.
* **Kế hoạch hành động 90 ngày (Có số & người chịu trách nhiệm):**
  * **Tháng 1 (Học hỏi & Đo lường):** Ký gửi 30 căn độc quyền tại Sapphire 1, chốt 15 giao dịch; kiểm soát tỷ lệ no-show $< 15\%$, Gross Margin $\ge 75\%$. *(Phụ trách: Nguyễn Khánh Duy - Lead Tech & Ops)*.
  * **Tháng 2 (Tối ưu & Chuẩn hóa):** Mở rộng 80 căn tại Sapphire 2 & Zenpark, chốt 45 giao dịch; giảm số lượt dẫn phòng/deal từ 3.0 xuống $\le 2.2$ lượt; GM $\ge 80\%$. *(Phụ trách: Trưởng nhóm Field Host)*.
  * **Tháng 3 (Mở rộng & Tích hợp Kênh):** Đạt 200 căn ký gửi, 100 deal/tháng, doanh thu 350 triệu/tháng; chính thức ra mắt Zalo Mini App độc quyền toàn khu Ocean Park 1. *(Phụ trách: Trưởng nhóm Đối tác - Partnership Lead)*.

---

## 3. KHỐI EVIDENCE PACK (3 TÀI SẢN BẰNG VĂN BẢN)

1. **Eval Results (Đã hoàn thành 05/10/2026 — AI Engineer phụ trách):**
   * Đánh giá trên 150 hội thoại thực tế và 40 căn hộ: Tỷ lệ match căn đúng ngân sách All-in đạt **96.0%**; OCR trích xuất CCCD gắn chip đạt **98.5%**; Tỷ lệ khách no-show giảm từ 60% xuống **8.5%** nhờ xác thực OTP Zalo và nhắc lịch tự động trước 10 phút.
2. **Procurement & Legal Q&A (Đã hoàn thành 06/10/2026 — Pháp chế phụ trách):**
   * Tài liệu pháp lý 10 trang trả lời 3 lo ngại lớn nhất của chủ nhà:
     * *Bảo mật dữ liệu cá nhân:* Ảnh CCCD mã hóa chuẩn AES-256 theo đúng Nghị định 13/2023/NĐ-CP.
     * *Tính pháp lý của hợp đồng:* Hợp đồng thuê điện tử ký bằng OTP Zalo có giá trị pháp lý đầy đủ theo Luật Giao dịch Điện tử 2023 và Điều 472 Bộ luật Dân sự 2015.
     * *Chống tranh chấp hao mòn:* Biên bản bàn giao số (Digital Handover Passport) chụp ảnh 10 hạng mục nội thất có timestamp và geofence phân định rõ hao mòn tự nhiên vs hư hỏng do khách làm vỡ.
3. **Pilot Report (Đang triển khai — Deadline: 25/10/2026 — Lead Operations phụ trách):**
   * Kết quả thử nghiệm 30 căn hộ tại The Sapphire: 26/30 căn đã cho thuê xong trong thời gian trung bình **6.8 ngày** (so với trung bình thị trường 23 ngày); chủ nhà tiết kiệm **100%** số lần đi lại; đánh giá hài lòng đạt **4.85/5 sao**; 0 tranh chấp cọc.

---

## 4. BÀI TEST NGƯỜI LẠ (STRANGER TEST - ĐẠT CHUẨN TRONG 2 PHÚT)

| Câu hỏi người lạ | Câu trả lời trực tiếp trong 1 câu (Không cần hỏi lại) |
| :--- | :--- |
| **1. Bạn bán cái gì, cho ai, tính tiền thế nào?** | Bán dịch vụ điều phối cho thuê căn hộ trọn gói cho chủ nhà nội thành có căn tại Ocean Park, thu phí 50% tiền thuê tháng đầu (~3.5tr) khi chốt deal thành công. |
| **2. Bạn có lãi trên mỗi đơn vị không, số nào chứng minh?** | Lãi gộp 2.870.000 VNĐ / hợp đồng (Gross Margin 82.0%), vì mỗi deal thu 3.500.000 VNĐ trong khi toàn bộ chi phí AI + Field Host + Admin chỉ tốn 630.000 VNĐ. |
| **3. Bạn tiếp cận khách qua đâu, vì sao là kênh đó?** | Tiếp cận độc quyền qua Ban Quản trị & Group cư dân Ocean Park (120k thành viên); nhúng trực tiếp vào Zalo chủ nhà đang dùng nên không tốn chi phí cài app. |
