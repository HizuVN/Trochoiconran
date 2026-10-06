# Nhật Ký Prompt (Prompt Log) - Tuần 5: CSS Animations

Dưới đây là danh sách các câu lệnh (prompt) đã được sử dụng để nhờ AI hỗ trợ xây dựng, tinh chỉnh tốc độ và độ mượt của các hiệu ứng chuyển động trong bài tập tuần này:

## 1. Micro-interactions (Nút Bấm Cảm Xúc)
- **Prompt gốc:** "Hãy viết mã CSS transition cho một button sao cho khi hover nó sẽ nâng lên 3px, thêm box-shadow đậm hơn, và sử dụng hàm timing 'cubic-bezier' để chuyển động trông tự nhiên hơn. Khi click (active), nút thu nhỏ lại scale(0.95)."
- **Prompt tinh chỉnh UI & hiệu năng:** "Thêm background gradient cho nút, tăng mức độ translateY lên -5px và sửa tham số cubic-bezier thành (0.25, 0.46, 0.45, 0.94) để hiệu ứng nảy mượt mà, chân thực hơn. Đảm bảo chỉ dùng transform."

## 2. Loading Master (Spinner)
- **Prompt:** "Tạo loading spinner CSS, sử dụng border-top màu khác biệt, animation xoay 360° infinite với timing function là linear."
- **Prompt tinh chỉnh:** "Làm cho viền spinner dày hơn một chút và kết hợp thêm màu ở viền phải (border-right-color) để tạo cảm giác đa sắc."

## 3. Thư viện AOS & Animate.css
- **Prompt:** "Hướng dẫn tôi cách tích hợp thư viện AOS và Animate.css qua CDN. Viết code ví dụ áp dụng thuộc tính data-aos='fade-up' cho các thẻ section để nội dung hiện ra mượt mà khi cuộn trang."

## 4. Floating Action Button & Card Flip
- **Prompt FAB:** "Thiết kế một Floating Action Button (FAB) liên hệ cố định ở góc dưới bên phải màn hình, có hiệu ứng pulse nhấp nháy liên tục bằng @keyframes để thu hút sự chú ý."
- **Prompt Card Flip:** "Tạo thẻ nhân sự lật 3D. Khi hover vào thẻ sẽ xoay rotateY(180deg) để hiện thông tin liên hệ ở mặt sau. Sử dụng transform-style: preserve-3d và backface-visibility: hidden."

## 5. Hiệu ứng gõ chữ (Typing) & Parallax
- **Prompt Typing:** "Viết mã CSS thuần để tạo hiệu ứng gõ chữ (typing effect) cho dòng chữ 'Tôi là một Web Developer...', kết hợp con trỏ nhấp nháy liên tục ở cuối mà không cần dùng JavaScript."
- **Prompt Parallax:** "Hướng dẫn cách làm background parallax tạo chiều sâu chỉ bằng CSS thuần, sử dụng thuộc tính background-attachment: fixed."

## 6. Hamburger Menu & Skill Bar
- **Prompt Hamburger:** "Tạo hiệu ứng CSS biến đổi 3 dấu gạch ngang của menu Hamburger thành dấu X mượt mà thông qua CSS Transitions khi được thêm class 'active'."
- **Prompt Skill Bar:** "Tạo thanh kỹ năng (Skill bar) cho HTML (90%), CSS (85%), JS (75%) có animation chạy thanh tiến trình từ 0% lên mức tương ứng khi trang tải xong bằng @keyframes."

## 7. Tối ưu hiệu năng (Performance Refactoring)
- **Prompt:** "Kiểm tra lại toàn bộ file CSS. Hãy chắc chắn rằng không sử dụng các thuộc tính thay đổi layout (như top, left, margin) cho hiệu ứng chuyển động. Hãy chuyển toàn bộ sang sử dụng transform (translate, scale, rotate) và opacity để ép trình duyệt render bằng GPU, tránh hiện tượng Layout Reflow gây lag trên điện thoại."
