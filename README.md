readme_content = """# 🐍 Retro Snake Game (Trò Chơi Con Rắn)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)
[![Pygame](https://img.shields.io/badge/framework-Pygame-informational.svg)](https://www.pygame.org/)
[![Status](https://img.shields.io/badge/status-active-brightgreen.svg)]()

> Một phiên bản hiện đại của tựa game rắn săn mồi kinh điển với đồ họa retro, hiệu ứng âm thanh sống động, hệ thống vật phẩm đa dạng và nhiều chế độ chơi thử thách.

---

## 📋 Mục lục

- [Giới thiệu](#-giới-thiệu)
- [Tính năng nổi bật](#-tính-năng-nổi-bật)
- [Hình ảnh minh họa](#-hình-ảnh-minh-họa)
- [Công nghệ sử dụng](#-công-nghệ-sử-dụng)
- [Cấu trúc dự án](#-cấu-trúc-dự-án)
- [Hướng dẫn cài đặt & Khởi chạy](#-hướng-dẫn-cài-đặt--khởi-chạy)
- [Hướng dẫn điều khiển](#-hướng-dẫn-điều-khiển)
- [Quy tắc tính điểm & Vật phẩm](#-quy-tắc-tính-điểm--vật-phẩm)
- [Tùy chỉnh & Cấu hình](#-tùy-chỉnh--cấu-hình)
- [Kế hoạch phát triển (Roadmap)](#-kế-hoạch-phát-triển-roadmap)
- [Đóng góp dự án](#-đóng-góp-dự-án)
- [Tác giả & Bản quyền](#-tác-giả--bản-quyền)

---

## 🎮 Giới thiệu

**Retro Snake Game** được phát triển nhằm tái hiện lại trải nghiệm tuổi thơ trên các dòng máy Nokia cổ điển, kết hợp thêm các yếu tố gameplay hiện đại:
- Đồ họa pixel/neon mượt mà, hỗ trợ nhiều bảng màu (Themes).
- Cơ chế tăng tốc theo điểm số và xuất hiện vật phẩm ngẫu nhiên.
- Hệ thống lưu điểm cao kỷ lục cục bộ (Local High Scores) và âm thanh vui nhộn.

---

## ✨ Tính năng nổi bật

- [x] **3 Chế độ chơi phong phú:**
  - **Classic:** Không tường bao quanh (xuyên tường) hoặc tường cố định kinh điển.
  - **Obstacle Mode:** Xuất hiện chướng ngại vật ngẫu nhiên theo thời gian.
  - **Time Attack:** Thu thập tối đa thức ăn trước khi hết giờ (mỗi quả táo cộng thêm thời gian).
- [x] **Hệ thống Vật phẩm (Power-ups):**
  - 🍎 **Táo đỏ thông thường:** +10 điểm, tăng chiều dài rắn.
  - 🌟 **Táo vàng may mắn:** Xuất hiện trong 5 giây, +50 điểm.
  - ⚡ **Sấm chớp:** Tăng tốc độ di chuyển trong 7 giây.
  - ❄️ **Băng tuyết:** Làm chậm tốc độ để điều khiển dễ dàng hơn.
- [x] **Giao diện & Âm thanh:**
  - Menu khởi động, tạm dừng (Pause), màn hình Game Over trực quan.
  - Nhạc nền 8-bit và hiệu ứng SFX khi ăn mồi, va chạm, thăng cấp.
  - Hỗ trợ đổi Theme màu: Classic Green, Cyberpunk Neon, Dark Mode.
- [x] **Lưu trữ dữ liệu:** Tự động lưu trữ Top 5 điểm số cao nhất vào file `highscores.json`.

---

## 🖼️ Hình ảnh minh họa

| Màn hình chính (Main Menu) | Màn hình chơi game (Gameplay) |
| :---: | :---: |
| ![Main Menu](assets/screenshots/menu_preview.png) | ![Gameplay](assets/screenshots/gameplay_preview.png) |

*(Bạn có thể thay thế đường dẫn trên bằng ảnh chụp thực tế hoặc file GIF demo)*

---

## 🛠️ Công nghệ sử dụng

- **Ngôn ngữ lập trình:** [Python 3.8+](https://www.python.org/)
- **Thư viện đồ họa & âm thanh:** [Pygame 2.5+](https://www.pygame.org/)
- **Quản lý dữ liệu:** JSON (High Scores & Settings)

---

## 📂 Cấu trúc dự án

```text
snake-game/
├── assets/
│   ├── audio/
│   │   ├── eat.wav             # Âm thanh khi ăn mồi
│   │   ├── game_over.wav       # Âm thanh khi thua cuộc
│   │   └── background_music.mp3 # Nhạc nền 8-bit
│   ├── fonts/
│   │   └── retro_pixel.ttf     # Font chữ Pixel retro
│   └── images/
│       └── icon.png            # Icon ứng dụng
├── src/
│   ├── __init__.py
│   ├── config.py               # Thiết lập kích thước, màu sắc, tốc độ
│   ├── food.py                 # Logic tạo và quản lý vật phẩm / mồi
│   ├── game.py                 # Vòng lặp chính của trò chơi (Game Loop)
│   ├── scoreboard.py           # Quản lý điểm số và lưu Highscore
│   ├── snake.py                # Xử lý tọa độ, hướng di chuyển, va chạm của rắn
│   └── ui.py                   # Giao diện menu, HUD, màn hình Game Over
├── data/
│   └── highscores.json         # File lưu kỷ lục điểm số
├── tests/
│   └── test_snake.py           # Unit tests kiểm tra logic di chuyển & va chạm
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
