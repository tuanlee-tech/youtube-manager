# TỔNG KẾT FIRST COMMIT: VIDEO V01
# KÊNH: TIỀN CÓ LÝ DO (@tiencolydo)

- **Tiêu đề chính thức:** `Lương 15 Triệu Cuối Tháng Còn 0: Tiền Của Bạn Đã Đi Đâu?`
- **Định dạng:** Long-form Video (~7 phút 25 giây, 1,955 từ)
- **Phong cách thị giác đã khóa:** 100% Narrative Graphic Novel / Ligne Claire Editorial (nền giấy ngà ấm `#F5F0E8`, nét mực đen than `#2C2825`, màu gouache/watercolor hoài niệm).
- **Ngày hoàn tất:** 2026-10-14
- **Trạng thái:** HOÀN TẤT & ĐÓNG BĂNG (ALL 12 LAYERS LOCKED)

---

## 1. TIÊU ĐỀ 12 HỒ SƠ KHÓA (LOCK RECORDS)

| Lớp | Tên hồ sơ khóa | Đường dẫn file | Trạng thái |
|:---:|---|---|:---:|
| **L0** | Đo tốc độ giọng đọc thực tế (PACE) | [L0_PACE.md](file:///e:/youtube-prompt/channels/tiencolydo/videos/V01/L0_PACE.md) | LOCKED (264 WPM) |
| **L1** | Đóng gói nội dung & Bao bì (Packaging) | [L1_PACKAGING.md](file:///e:/youtube-prompt/channels/tiencolydo/videos/V01/L1_PACKAGING.md) | LOCKED |
| **L2** | Góc tiếp cận & Dàn ý nhịp (Beat Map) | [L2_BEAT_MAP.md](file:///e:/youtube-prompt/channels/tiencolydo/videos/V01/L2_BEAT_MAP.md) | LOCKED (8 beats) |
| **L3** | Giọng thoại & Kịch bản (Script) | [L3_SCRIPT.md](file:///e:/youtube-prompt/channels/tiencolydo/videos/V01/L3_SCRIPT.md) | LOCKED (1,955 từ) |
| **L4** | Kế hoạch cảnh (Scene Plan) | [L4_SCENE_PLAN.md](file:///e:/youtube-prompt/channels/tiencolydo/videos/V01/L4_SCENE_PLAN.md) | LOCKED (24 cảnh) |
| **L5** | Ngôn ngữ thị giác & Key Assets | [L5_KEY_ASSETS.md](file:///e:/youtube-prompt/channels/tiencolydo/videos/V01/L5_KEY_ASSETS.md) | LOCKED |
| **L6** | Tài nguyên hình ảnh tĩnh | [L6_IMAGE_ASSETS.md](file:///e:/youtube-prompt/channels/tiencolydo/videos/V01/L6_IMAGE_ASSETS.md) | LOCKED (24 ảnh + Thumbnail) |
| **L7** | Sản xuất clip chuyển động (Motion Clips) | [L7_MOTION_CLIPS.md](file:///e:/youtube-prompt/channels/tiencolydo/videos/V01/L7_MOTION_CLIPS.md) | LOCKED (5 clips) |
| **L8** | Âm thanh, Phụ đề, Nhạc nền & Hòa âm | [L8_AUDIO_SUBTITLES.md](file:///e:/youtube-prompt/channels/tiencolydo/videos/V01/L8_AUDIO_SUBTITLES.md) | LOCKED |
| **L9** | Thiết kế Thumbnail | [L9_THUMBNAIL.md](file:///e:/youtube-prompt/channels/tiencolydo/videos/V01/L9_THUMBNAIL.md) | LOCKED (AI In-image text) |
| **L10** | Gói SEO & Xuất bản | [SEO.md](file:///e:/youtube-prompt/channels/tiencolydo/videos/V01/SEO.md) | LOCKED |
| **L11** | Bàn giao sang Remotion | [L11_REMOTION_HANDOFF.md](file:///e:/youtube-prompt/channels/tiencolydo/videos/V01/L11_REMOTION_HANDOFF.md) | READY FOR ASSEMBLY |

---

## 2. BỘ QUY TẮC CỐT LÕI ĐƯỢC CHUẨN HÓA (RULES & BANS)

### Bộ RULES (Bắt buộc tuân thủ cho mọi video tiếp theo):
1. `RULE [PACE]:` Đo tốc độ giọng đọc thực tế với VieNeu-TTS (khóa ở mức 264 từ/phút), không bao giờ giả định con số 150 WPM.
2. `RULE [THUMBNAIL]:` Thumbnail chữ tối đa 4 từ, tích hợp trực tiếp typography vào ảnh tạo bởi AI (theo chỉ đạo creator) để không phụ thuộc vào dựng text bên ngoài.
3. `RULE [BEAT LINK]:` Mọi beat phải liên kết bằng **NHƯNG (BUT)** hoặc **VÌ VẬY (THEREFORE)**, tuyệt đối không dùng liên kết tuần tự "và sau đó".
4. `RULE [ART STYLE]:` 100% hình ảnh dùng phong cách Narrative Graphic Novel / Ligne Claire trên nền giấy ngà hoài niệm (`#F5F0E8`), viền mực đen than (`#2C2825`), bảng màu gouache trầm ấm (Navy `#3B5B75`, Terracotta `#D7263D`, Amber `#D4A359`, Olive `#6B7F62`).
5. `RULE [ANIMATION POLICY]:` Vùng Hook (30s đầu) đạt tối thiểu 70% cảnh chuyển động. Thân bài chỉ chuyển động ở bước ngoặt/cảm xúc. Toàn bộ chuyển động sinh ra từ chính ảnh 2D Comic bằng Image-to-Video.
6. `RULE [CLIP FIT]:` Remotion tự động xử lý lệch thời lượng clip: dài hơn thì `trim_end`, ngắn hơn thì `hold_last`.
7. `RULE [CHARACTER MINH]:` Nhân vật Minh luôn là nam 26 tuổi, công sở điềm tĩnh; prompt luôn có `female, woman, girl, feminine features` trong danh sách Avoid để chống biến thiên giới tính.
8. `RULE [TTS NORMALIZATION]:` Mọi số tiền, tỷ lệ %, chữ viết tắt bắt buộc phải có trường `tts_text` phiên âm chữ đầy đủ (ví dụ: `15%` -> `mười lăm phần trăm`, `15 triệu` -> `mười lăm triệu`).
9. `RULE [SUBTITLE]:` Phụ đề karaoke Be Vietnam Pro 52px, chữ thường màu ngà `#F5F0E8`, từ active màu đỏ gạch `#D7263D`, viền đen `3px #1F2421`, tối đa 5 từ/trang.
10. `RULE [AUDIO MIX]:` Nhạc nền lo-fi acoustic guitar âm lượng -22dB, ducking -8dB (về -30dB khi có voiceover), target -16 LUFS.

### Bộ BANS (Điều cấm tuyệt đối):
1. `BAN [NO CINEMATIC REALISM]:` Cấm tuyệt đối chèn footage người thật / 35mm cinematic photorealism lẫn vào video phong cách graphic novel.
2. `BAN [NO FAKE CLAIMS]:` Cấm tuyên bố số liệu làm giàu nhanh, hứa hẹn x2 x5 tài sản trong thời gian ngắn. Mọi phép tính lãi suất chỉ lấy mức giả định khiêm tốn (8%/năm).
3. `BAN [NO AUTO-PUBLISH]:` Mặc định luôn để chế độ Private khi xuất bản, creator là người duy nhất duyệt trước khi bấm Public.

---

## 3. GÓI DỮ LIỆU ĐÃ SẴN SÀNG CHO REMOTION

1. **Thư mục tài nguyên:** `channels/tiencolydo/videos/V01/images/`
   - Đủ 5 clip chuyển động: `S001_anim.mp4`, `S002_anim.mp4`, `S004_anim.mp4`, `S015_anim.mp4`, `S018_anim.mp4`
   - Đủ 19 ảnh tĩnh đồ họa: `S003.jpg`, `S005.jpg` đến `S014.jpg`, `S016.jpg`, `S017.jpg`, `S019.jpg` đến `S024.jpg`
   - Đủ 1 ảnh thumbnail: `THUMBNAIL.jpg` (có text sẵn)
2. **Kế hoạch máy đọc:** [SCENE_PLAN.json](file:///e:/youtube-prompt/channels/tiencolydo/videos/V01/SCENE_PLAN.json) (đã liên kết clip và thông số clip_fit)
3. **Thông số kỹ thuật:** [PARAMETERS.md](file:///e:/youtube-prompt/channels/tiencolydo/videos/V01/PARAMETERS.md)
4. **Dữ liệu đăng tải:** [SEO.md](file:///e:/youtube-prompt/channels/tiencolydo/videos/V01/SEO.md)
