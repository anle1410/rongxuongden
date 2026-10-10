<div align="center">

  # 🐉 RỒNG XƯƠNG ĐEN (BLACK BONE DRAGON)
  ### *Dynamic SVG Kinetic Animation & Interactive Cursor Effect*

  [![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
  [![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css
  3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
  [![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
  [![SVG](https://img.shields.io/badge/SVG-FF9900?style=for-the-badge&logo=svg&logoColor=white)](https://www.w3.org/TR/SVG11/)
  [![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](LICENSE)

  <p align="center">
    <b>Một tác phẩm nghệ thuật đồ họa chuyển động tương tác (Kinetic Dragging & Inverse Kinematics) được tạo 100% từ Vanilla JS và SVG Vector thuần túy.</b>
    <br />
    <a href="https://github.com/anle1410/rongxuongden"><strong>Khám phá kho lưu trữ »</strong></a>
    <br />
    <br />
    <a href="#-tính-năng-nổi-bật">Tính Năng</a>
    ·
    <a href="#-phân-tích-thuật-toán-cốt-lõi">Giải Thích Thuật Toán</a>
    ·
    <a href="#-tùy-chỉnh--nâng-cấp">Tùy Chỉnh</a>
    ·
    <a href="#-hướng-dẫn-sử-dụng">Hướng Dẫn Cài Đặt</a>
  </p>

---

</div>

## 🌟 GIỚI THIỆU TỔNG QUAN

**Rồng Xương Đen (Black Bone Dragon)** là một ứng dụng Web Animation tương tác cao cấp, tái hiện một con rồng xương phương Tây huyền bí uốn lượn uyển chuyển theo chuyển động con trỏ chuột của người dùng. 

Không sử dụng bất kỳ thư viện nặng nề nào ngoài JS & SVG nguyên bản, dự án kết hợp xuất sắc giữa **Toán học Động lực học Khớp (Kinetic Segment Physics)**, **Đường cong Lissajous** và **Vector Styling Gradient** để mang tới trải nghiệm mượt mà 60 FPS chuẩn 4K/Retina.

> 💡 **Điểm đặc biệt:** Khi không có tương tác chuột, Rồng Xương Đen sở hữu trí tuệ tự hành (Idle AI) tự động bay lượn tự do theo nhịp sinh học ngẫu nhiên quanh trung tâm màn hình.

---

## 🔥 TÍNH NĂNG NỔI BẬT

- ⚡ **Thuật Toán Động Lực Học Khớp (Inverse Kinematics):** 40 đốt xương (`Head`, `Fins`, `Spine`) liên kết chặt chẽ qua phép xoay lượng giác `Math.atan2`, mô phỏng chuyển động uyển chuyển của cơ thể rồng thật.
- 🎯 **Tương Tác Con Trỏ Nhạy Bằng Chuột & Cảm Ứng:** Bám sát tọa độ con trỏ (`pointermove`) với gia tốc làm mịn (`Easing`), tương thích hoàn hảo từ Desktop tới thiết bị cảm ứng Touch Screen (`touch-action: none`).
- 🔄 **Quỹ Đạo Tự Bay Tự Do (Idle Mode):** Tự động chuyển sang chế độ tự hành khi người dùng ngưng di chuột, bay lượn theo đường cong lượng giác Lissajous phức hợp (`sin/cos` kết hợp tỉ lệ khung hình).
- 📐 **Tỷ Lệ Thu Nhỏ Thần Kỳ (Tapering Body Physics):** Công thức toán học tự điều chỉnh kích thước từng đốt (`scale`) từ đầu rồng lớn tới chóp đuôi nhỏ dần tạo chiều sâu 3D chân thực.
- 🎨 **Đồ Họa Vector Sắc Nét 100%:** Sử dụng `<defs>`, `<g>`, `<linearGradient>` và `<use>` trong SVG giúp tăng hiệu năng render đỉnh cao, không bị mờ hay vỡ nét trên bất kỳ màn hình nào.
- 🪶 **Siêu Nhẹ & Tối Ưu Tuyệt Đối:** Mã nguồn tổng cộng chưa đến **10 KB**, zero-dependencies (không cần React, Three.js hay GSAP).

---

## 🏗️ CẤU TRÚC THƯ MỤC DỰ ÁN

```text
rồng/
├── 📄 index.html      # Cấu trúc SVG Defs chứa các mảnh Vector (Head, Fins, Spine)
├── 🎨 style.css       # Layout full màn hình, khóa cuộn trang & phối màu tông tối
├── ⚡ script.js        # Vòng lặp Animation (requestAnimationFrame) & Thuật toán lượng giác
└── 📖 README.md       # Tài liệu chi tiết dự án
```

---

## 🛠️ CÔNG NGHỆ SỬ DỤNG

| Công Nghệ | Vai Trò & Ứng Dụng |
| :--- | :--- |
| **HTML5 Canvas / SVG** | Định nghĩa đối tượng đồ họa mẫu (`Cabeza`, `Aletas`, `Espina`) & Gradient màu bạc-đen. |
| **Vanilla CSS3** | Thiết lập không gian tràn màn hình (`position: absolute`, `overflow: hidden`), bộ lọc màu `sepia(20%)`. |
| **JavaScript (ES6+)** | Tính toán ma trận biến hình `transform`, phép xoay `rotate()`, tịnh tiến `translate()`, tỉ lệ `scale()`. |
| **Pointer Events API** | Lắng nghe chuyển động chuột & cảm ứng đa nền thị mượt mà. |

---

## 📐 PHÂN TÍCH THUẬT TOÁN CỐT LÕI

### 1. Thuật toán Liên Kết Đốt Xương (Segment Tracking Physics)
Mỗi đốt xương `i` sẽ tính toán góc nghiêng `a` so với đốt phía trước `i - 1` thông qua hàm tang ngược `Math.atan2`:

$$\theta = \text{atan2}(y_i - y_{i-1}, x_i - x_{i-1})$$

Tọa độ của đốt xương sẽ liên tục đuổi theo đốt trước với độ trễ tự nhiên:

```javascript
const a = Math.atan2(e.y - ep.y, e.x - ep.x);
e.x += (ep.x - e.x + (Math.cos(a) * (100 - i)) / 5) / 4;
e.y += (ep.y - e.y + (Math.sin(a) * (100 - i)) / 5) / 4;
```

### 2. Thuật toán Tự Thu Nhỏ Thân Rồng (Dynamic Tapering)
Tỉ lệ `scale` được tính theo chỉ số đốt $i$ giúp phần đầu to và phần đuôi nhỏ dần:

```javascript
const s = (162 + 4 * (1 - i)) / 50;
```

### 3. Ma Trận Biến Hình SVG Transform
Mỗi khung hình (`requestAnimationFrame`), JS cập nhật thuộc tính `transform` cho thẻ `<use>` tương ứng:

```javascript
e.use.setAttributeNS(
  null,
  "transform",
  `translate(${(ep.x + e.x) / 2},${(ep.y + e.y) / 2}) rotate(${(180 / Math.PI) * a}) scale(${s},${s})`
);
```

### 4. Quỹ Đạo Bay Tự Hành (Lissajous Idle Curve)
Khi không di chuyển chuột, bán kính rồng mở rộng và lượn theo công thức:

```javascript
const ax = (Math.cos(3 * frm) * rad * width) / height;
const ay = (Math.sin(4 * frm) * rad * height) / width;
```

---

## 🚀 HƯỚNG DẪN SỬ DỤNG & CÀI ĐẶT

### Trực tiếp trên trình duyệt
Không cần cài đặt bất kỳ Node.js hay Build tool nào!

1. **Clone repository về máy local:**
   ```bash
   git clone https://github.com/anle1410/rongxuongden.git
   cd rongxuongden
   ```

2. **Mở dự án:**
   Double click vào file `index.html` hoặc chạy với extension **Live Server** trong VS Code.

---

## 🎨 TÙY CHỈNH & NÂNG CẤP DỄ DÀNG

Bạn có thể tùy biến các thông số trong [script.js](file:///d:/th%C6%B0%20vi%E1%BB%87n%20animation/r%E1%BB%93ng/script.js) để tạo các hiệu ứng khác nhau:

### 1. Thay đổi chiều dài rồng (Số lượng đốt xương `N`):
```javascript
// Thay đổi số N trong script.js (Mặc định: 40)
const N = 60; // Thân rồng dài hơn, uốn lượn phức tạp hơn
```

### 2. Đổi màu nền & Màu Rồng (trong [style.css](file:///d:/th%C6%B0%20vi%E1%BB%87n%20animation/r%E1%BB%93ng/style.css) & [index.html](file:///d:/th%C6%B0%20vi%E1%BB%87n%20animation/r%E1%BB%93ng/index.html)):
- Nền màn hình: Thay đổi `background` trong file `style.css`.
- Màu rồng: Tùy biến mã màu `stop-color` trong `<linearGradient>` ở file `index.html`.

---

## 👤 TÁC GIẢ & THÔNG TIN LIÊN HỆ

- **Tác giả:** LÊ AN
- **GitHub:** [@anle1410](https://github.com/anle1410)
- **Email:** `anle64437@gmail.com`
- **Repository:** [github.com/anle1410/rongxuongden](https://github.com/anle1410/rongxuongden)

---

<div align="center">

  **⭐ Nếu bạn thấy dự án này thú vị, hãy dành tặng 1 Star trên GitHub nhé! ⭐**

  *Developed with ❤️ & Pure Mathematics by LÊ AN.*

</div>
