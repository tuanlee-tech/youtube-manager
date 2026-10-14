# LOCK RECORD: L7 — TÀI NGUYÊN CLIP CHUYỂN ĐỘNG (MOTION CLIPS)

- Video: V01 — Lương 15 Triệu Cuối Tháng Còn 0: Tiền Của Bạn Đã Đi Đâu?
- Ngày khóa: 2026-10-14
- Trạng thái: LOCKED & VERIFIED

---

## 1. TỔNG QUAN TÀI NGUYÊN CLIP ĐÃ NGHIỆM THU (5 CLIPS)

Toàn bộ 5 clip chuyển động 2D Graphic Novel Animation được tạo từ chính ảnh gốc tham chiếu trên Google Flow / Omni / Veo, lưu tại:
`channels/tiencolydo/videos/V01/images/`

Tất cả đã được làm sạch tên file và kiểm tra thông số kỹ thuật bằng `ffprobe`:

| Mã cảnh | File clip | Độ phân giải | FPS | Thời lượng clip | Kế hoạch cảnh | Cơ chế Remotion Clip Fit | Mô tả chuyển động |
|---|---|:---:|:---:|:---:|:---:|:---:|---|
| **S001** | `S001_anim.mp4` | 1280x720 (16:9) | 24 | 10.0s | 10.0s | `exact` (Khớp 100%) | Khói cà phê bốc lên lượn lờ, Minh nhìn ra cửa sổ mờ sương, mưa bụi bay nhẹ. |
| **S002** | `S002_anim.mp4` | 1280x720 (16:9) | 24 | 10.0s | 7.0s | `trim_end` (Cắt lấy 7s đầu) | Minh gõ phím làm việc nhịp nhàng, mắt chớp tự nhiên, ánh đèn bàn ấm. |
| **S004** | `S004_anim.mp4` | 1280x720 (16:9) | 24 | 6.0s | 5.0s | `trim_end` (Cắt lấy 5s đầu) | Bóng người bước đi cô độc trên vỉa hè chạng vạng, vạt áo lay theo gió. |
| **S015** | `S015_anim.mp4` | 1280x720 (16:9) | 24 | 10.0s | 10.0s | `exact` (Khớp 100%) | Dòng cát đỏ gạch chảy đều đặn và êm đềm xuống đáy đồng hồ cát. |
| **S018** | `S018_anim.mp4` | 1280x720 (16:9) | 24 | 10.0s | 14.0s | `hold_last` (Động 10s + tĩnh 4s) | Điện thoại rung chuông cuộc gọi "Mẹ ở quê" trên mặt bàn gỗ. |

---

## 2. ĐỐI CHIẾU CHÍNH SÁCH CHUYỂN ĐỘNG (ANIMATION POLICY)

- **Vùng Hook Zone (S001–S004):** Đạt **75%** tỷ lệ chuyển động (3 clip / 4 cảnh), vượt ngưỡng tối thiểu 70% của Stage 3. Giúp giữ chân người xem tối đa trong 28 giây quan trọng nhất.
- **Thân bài (S005–S024):** Có đúng 2 clip chuyển động tại điểm bước ngoặt thời gian (S015) và đỉnh điểm khủng hoảng (S018). Các cảnh còn lại dùng ảnh tĩnh kết hợp hiệu ứng camera Remotion.
- **Chính sách âm thanh clip:** Mute toàn bộ audio gốc của clip trong Remotion để nhường trọn vẹn không gian cho giọng đọc VieNeu-TTS và nhạc nền lo-fi.
