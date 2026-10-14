# LOCK RECORD: L11 — BÀN GIAO SANG REMOTION (REMOTION HAND-OFF)

- Video ID: V01 — Lương 15 Triệu Cuối Tháng Còn 0: Tiền Của Bạn Đã Đi Đâu?
- Kênh: Tiền Có Lý Do (@tiencolydo)
- Trạng thái: READY FOR AUTOMATED ASSEMBLY

---

## 1. BIÊN BẢN KIỂM ĐỊNH TÍNH NHẤT QUÁN (CONSISTENCY CHECKS)

| Hạng mục kiểm tra | Tiêu chuẩn kỹ thuật | Kết quả đối soát | Trạng thái |
|---|---|---|:---:|
| **Khớp số lượng cảnh** | Kế hoạch có 24 cảnh (S001 -> S024) | 5 clip chuyển động (`S001`, `S002`, `S004`, `S015`, `S018`) + 19 ảnh tĩnh + 1 Thumbnail | **PASS** |
| **Thumbnail đi kèm** | 1 file Thumbnail 16:9 chất lượng cao | File `THUMBNAIL.jpg` đã tích hợp sẵn text | **PASS** |
| **Quy chuẩn tên file** | Đặt tên đúng mã cảnh (S001.jpg, S001_anim.mp4) | Đã chuẩn hóa toàn bộ 30 files, không sót hậu tố | **PASS** |
| **Tỷ lệ khung hình** | 16:9 chuẩn YouTube | 100% tài nguyên ảnh & clip đạt chuẩn 16:9 | **PASS** |
| **Animation Policy** | Vùng Hook >= 70% chuyển động | 3/4 cảnh Hook là video (75%), thân bài có 2 clip | **PASS** |
| **Clip Fit Policy** | Xử lý lệch thời lượng clip | S001/S015 (exact), S002/S004 (trim_end), S018 (hold_last) | **PASS** |
| **Tổng thời lượng ước tính** | 445s (~7m25s) +-5% | Khớp kịch bản 1,955 từ với PACE 264 WPM | **PASS** |
| **Phiên âm VieNeu-TTS** | Mọi con số/viết tắt có `tts_text` chuẩn | Đã nạp 100% `tts_text` vào `SCENE_PLAN.json` | **PASS** |

---

## 2. GÓI DỮ LIỆU BÀN GIAO (3 FILE NÒNG CỐT)

Các file cấu hình máy đọc tự động đã sẵn sàng tại:
1. [SCENE_PLAN.json](file:///e:/youtube-prompt/channels/tiencolydo/videos/V01/SCENE_PLAN.json): Chứa 24 cảnh với timeline, narration, `tts_text`, hiệu ứng camera Remotion, chuyển cảnh và text trên màn hình.
2. [PARAMETERS.md](file:///e:/youtube-prompt/channels/tiencolydo/videos/V01/PARAMETERS.md): Toàn bộ thông số kỹ thuật phân giải (1920x1080 30fps), VieNeu-TTS, Whisper subtitles (Be Vietnam Pro, màu ngà & highlight đỏ gạch), âm nhạc (-22dB, ducking -8dB).
3. [SEO.md](file:///e:/youtube-prompt/channels/tiencolydo/videos/V01/SEO.md): Tiêu đề, mô tả hoàn chỉnh có mốc thời gian `{{CHAPTERS}}`, danh sách tags, bình luận ghim và thiết lập xuất bản Private.

---

## 3. CẤU TRÚC THƯ MỤC KHUYẾN NGHỊ CHO DỰ ÁN REMOTION

```text
remotion-project/
  public/
    scenes/            # Copy toàn bộ file từ channels/tiencolydo/videos/V01/images/ (S001.jpg -> S024.jpg)
    music/             # background.mp3
  brief/
    SCENE_PLAN.json    # Copy từ channels/tiencolydo/videos/V01/SCENE_PLAN.json
    PARAMETERS.md      # Copy từ channels/tiencolydo/videos/V01/PARAMETERS.md
    SEO.md             # Copy từ channels/tiencolydo/videos/V01/SEO.md
  out/                 # Nơi render draft.mp4, preview_mix.mp4, final.mp4
```
