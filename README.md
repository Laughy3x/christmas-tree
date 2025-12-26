# 🎄 Cây Giáng Sinh 3D Tương Tác Sang Trọng

> Một ứng dụng web cây Giáng Sinh 3D độ phân giải cao dựa trên **React**, **Three.js (R3F)** và **nhận diện cử chỉ AI**.

Dự án này không chỉ đơn thuần là một cái cây; đó là một phòng trưng bày tương tác lưu giữ những kỷ niệm. Hàng trăm hạt, ánh sáng rực rỡ và những bức ảnh Polaroid trôi nổi kết hợp tạo nên một cây Giáng Sinh sang trọng. Người dùng có thể điều khiển hình dạng của cây (tụm lại/lan rộng) và xoay góc nhìn bằng cử chỉ, trải nghiệm một bữa tiệc thị giác điện ảnh.

![Xem trước dự án](public/preview.png)

*(Lưu ý: Nên tải lên ảnh chụp màn hình dự án đang chạy của bạn tại đây)*

## ✨ Các tính năng chính

* **Trải nghiệm hình ảnh tuyệt đỉnh**: Thân cây được tạo thành từ hơn 45.000 hạt phát sáng, kết hợp với hiệu ứng nở rộ và phát sáng động, tạo nên một bầu không khí như trong mơ.

* **Bộ sưu tập kỷ niệm:** Các bức ảnh trôi nổi phía trên cây theo phong cách Polaroid, mỗi bức là một vật thể phát sáng độc lập, hỗ trợ hiển thị hai mặt.

* **Điều khiển bằng cử chỉ AI:** Không cần chuột; điều khiển hình dạng của cây (tập hợp/phân tán) và xoay góc nhìn thông qua các cử chỉ được ghi lại bằng camera.

* **Chi tiết phong phú:** Bao gồm đèn màu nhấp nháy động, bông tuyết vàng và bạc rơi, và quà Giáng sinh cùng kẹo trang trí được phân bố ngẫu nhiên.

* **Khả năng tùy chỉnh cao:** Người dùng có thể dễ dàng thay thế ảnh bằng ảnh của riêng mình và tự do điều chỉnh số lượng ảnh. **

## 🛠️ Công nghệ sử dụng

* **Khung phần mềm**: React 18, Vite

* **Công cụ 3D**: React Three Fiber (Three.js)

* **Thư viện**: @react-three/drei, Maath

* **Xử lý hậu kỳ**: @react-three/postprocessing

* **Thị giác AI**: MediaPipe Tasks Vision (Google)

## 🚀 Bắt đầu nhanh

### 1. Chuẩn bị môi trường

Đảm bảo máy tính của bạn đã cài đặt Node.js (https://nodejs.org/) (khuyến nghị phiên bản 18 trở lên).

### 2. Cài đặt các thư viện phụ thuộc

Mở terminal trong thư mục gốc của dự án và chạy lệnh: `bash npm install`

### 3. Khởi chạy dự án

`npm run dev`

### 🖼️ Ảnh tùy chỉnh

### 1. Chuẩn bị ảnh

Tìm thư mục `public/photos/` trong thư mục dự án.

Ảnh bìa/ảnh trên cùng: Đặt tên là top.jpg (ảnh này sẽ xuất hiện trên ngôi sao năm cánh 3D ở đỉnh cây).

Ảnh thân cây: Đặt tên là 1.jpg, 2.jpg, 3.jpg... và cứ thế tiếp tục.

Gợi ý: Sử dụng ảnh vuông hoặc ảnh có tỷ lệ khung hình 4:3, và giữ kích thước tệp nhỏ (lý tưởng là dưới 500kb mỗi ảnh để hiệu suất mượt mà).

### 2. Thay thế ảnh Chỉ cần sao chép ảnh của bạn vào thư mục public/photos/, ghi đè lên các ảnh hiện có. Vui lòng giữ nguyên định dạng tên tệp (1.jpg, 2.jpg, v.v.).

### 3. Thay đổi số lượng ảnh (Tăng hoặc Giảm) Nếu bạn thêm nhiều ảnh hơn (ví dụ: từ mặc định 31 lên 100), bạn cần sửa đổi mã để hướng dẫn chương trình tải chúng.

Mở tập tin: src/App.tsx
Tìm đoạn mã xung quanh dòng 19: // --- Tạo động danh sách ảnh (top.jpg + 1.jpg đến 31.jpg) ---
const TOTAL_NUMBERED_PHOTOS = 31; // <--- Hãy sửa số này!

### 🖐️ Hướng dẫn điều khiển bằng cử chỉ

* **Dự án này có hệ thống nhận diện cử chỉ AI tích hợp. Vui lòng đứng trước camera để thao tác (có nút DEBUG ở góc dưới bên phải màn hình để xem hình ảnh từ camera)**:

🖐 Mở lòng bàn tay: Phân tán - Cây thông Noel nổ tung thành một cơn mưa các hạt và ảnh.

✊ Nắm tay: Lắp ráp - Tất cả các yếu tố ngay lập tức được lắp ráp thành một cây thông Noel hoàn hảo.

👋 Di chuyển lòng bàn tay sang trái/phải: Xoay góc nhìn - Di chuyển tay sang trái, cây sẽ xoay sang trái; di chuyển tay sang phải, cây sẽ xoay sang phải.

👋 Di chuyển lòng bàn tay lên/xuống: Chế độ xem nghiêng - Di chuyển tay lên, chế độ xem sẽ nghiêng; di chuyển tay xuống, chế độ xem sẽ nghiêng.

### ⚙️ Cấu hình nâng cao

* **Nếu bạn quen thuộc với lập trình, bạn có thể điều chỉnh thêm các thông số hình ảnh trong đối tượng CONFIG trong src/App.tsx**:

const CONFIG = {
colors: { ... }, // Thay đổi màu sắc của cây, đèn và đường viền
counts: {

foliage: 15000, // Thay đổi số lượng hạt lá (có thể gây lag trên các hệ thống cấu hình thấp)

ornaments: 300, // Thay đổi số lượng ảnh/Polaroid treo

lights: 400 // Thay đổi số lượng đèn dây

},

tree: { height: 22, radius: 9 }, // Thay đổi kích thước của cây

// ...

};

### 📄 Giấy phép

Giấy phép MIT. Hãy thoải mái sử dụng và chỉnh sửa cho các lễ hội của riêng bạn!

### Chúc mừng Giáng sinh! 🎄✨
