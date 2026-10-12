# HƯỚNG DẪN DÙNG CHANNEL FACTORY

## 0. Chuẩn bị
- Claude (chat thường, không cần MCP), NotebookLM và Gemini Pro (nghiên cứu), Google Flow (ảnh, clip), VieNeu-TTS (giọng, chạy máy bạn), một harness chạy agent cho Remotion.
- Tạo thư mục trên máy: `channels/<handle>/` với `research/`, `plan/`, `visual/`, `videos/V01/`, `metrics/` (xem README). Mỗi lần agent in một khối LOCKED trong code block, bạn lưu ngay vào đúng file. Agent không tự lưu.

## 1. Quy tắc dùng chung
- Mỗi lượt agent chỉ làm một stage. Bạn trả lời bằng một lệnh:
| Lệnh | Ý nghĩa |
|---|---|
| `ok` | khóa stage, sang stage sau |
| `revise: <ghi chú>` | sửa theo ghi chú (ghi càng cụ thể, càng ra quy tắc đo được) |
| `back` | quay lại stage trước |
| `skip` | bỏ qua, chỉ ở nơi cho phép |
| `jump <stage>` | nhảy tới stage (ví dụ `jump B1`) |
| `reopen L#` | (trong B3) mở lại một lớp; agent sẽ báo các lớp bị ảnh hưởng |
| `auto from L#` | (trong B3) từ lớp đó agent chỉ báo kết quả, không chờ duyệt từng lớp |
- Chat dài thì mở chat mới theo mục 2, đừng cố nhét tất cả vào một chat.
- Mọi con số hiệu suất đánh dấu `[ASSUMPTION]` là giả định, sẽ được đo ở B1.

## 2. Các bước

### Chat 1: nghiên cứu, kênh, Bible (R0 đến A6)
1. Dán toàn bộ `MASTER_PROMPT.md`.
2. Điền form R0 bằng câu trả lời thô. Ví dụ cho Tiền Có Lý Do có trong `examples/tien-co-ly-do.seed.md`. Agent trả về recap và khối `CHANNEL IDEA`.
3. **R1 chạy ngoài chat** (NotebookLM + Gemini), mở `phases/STAGE1_RESEARCH_KIT.md`:
   1. Tạo notebook, thêm 8 đến 15 video đối thủ, thumbnail và khung hình (nếu muốn phân tích hình).
   2. Chạy R2 (source audit); chuyển nguồn lệch ngách sang notebook khác nếu có "SPLIT RECOMMENDED".
   3. Chạy R3 (Deep Research) nếu thiếu nguồn.
   4. Trong Gemini Pro đính kèm notebook, chạy Part A, B, C, rồi R5 (tự kiểm).
   5. Ghép HAND-OFF HEADER + A + B + C thành `research/REPORT.md`.
   - Nếu có hai giai đoạn người xem khác tệp, làm hai notebook và hai báo cáo.
   - Không chạy được kit: để agent làm LITE bằng web search, hoặc gõ `skip: no evidence` (mọi nhận định chiến lược thành giả định).
4. Dán báo cáo vào chat. R2 cho verdict SUFFICIENT hoặc INSUFFICIENT; nếu thiếu thì bổ sung nguồn rồi dán lại.
5. A1 đến A6, mỗi stage `ok` hoặc `revise`. Chốt tên ở A1 trước, đừng đổi sau (đổi tên kéo theo làm lại, xem `docs/LESSONS.md`). Kiểm tra tên và handle trên YouTube thật trước khi `ok`.
6. A5: tự tạo avatar và banner bằng prompt agent đưa (Gemini hoặc Flow), upload ảnh để agent chấm và sửa prompt. Xóa dấu sao của Gemini ở hậu kỳ nếu có; xác nhận vùng an toàn banner trong Studio. Làm theo checklist cài đặt Studio.
7. A6: lưu `BIBLE.md`.

### Chat 2: kế hoạch 10 video và visual (B1, B2)
1. Mở chat mới, dán `MASTER_PROMPT.md`, rồi dán `BIBLE.md` và nói: `jump B1`.
2. B1: duyệt kế hoạch, lưu `plan/VIDEO_PLAN.md`.
3. B2: tạo bộ ảnh mẫu bằng prompt agent đưa, upload ảnh để agent chấm điểm (đạt từ 13/16 và không có 0 ở nhất quán hoặc SOUL). Lặp đến khi đạt. Lưu `visual/VISUAL_LOCK.md` cùng ảnh đã duyệt.

### Chat 3: video đầu tiên (B3)
1. Chat mới, dán `MASTER_PROMPT.md`, `BIBLE.md`, `VISUAL_LOCK.md`, `VIDEO_PLAN.md`, nói: `jump B3, video 1`.
2. Mỗi lớp L0 đến L11 một lượt, mỗi lớp lưu một LOCK RECORD vào `videos/V01/`.
3. Phần làm ngoài chat (agent đưa thẻ HAND-OFF CARD, một công cụ và một lần dán):
   - L0: đọc bài mẫu ~150 từ bằng VieNeu-TTS, báo số giây. PACE đã đo: 264 từ/phút (giọng VieNeu-TTS, bài đọc 150 từ trong 34,11 giây).
   - L3: nhập 3 hạt giống "soul" (khoảnh khắc thật, niềm tin gây phản đối, điều người xem nên làm đầu tiên).
   - L6, L7: chạy thẻ Flow theo từng batch, upload kết quả để agent chấm.
   - L8: thử 3 giọng, chốt giọng.
4. L11: agent in 3 khối (SCENE_PLAN.json, PARAMETERS, SEO). Dán vào `phases/REMOTION_ASSEMBLY_AGENT_PROMPT.md`, đặt file ảnh, clip, nhạc đúng thư mục và chạy agent trong harness. Duyệt từng cổng G1 đến G5.
5. Tự xem bản render, đăng ở chế độ Private rồi tự công bố. Agent lắp ráp không được đăng thay bạn.
6. Lưu FIRST COMMIT SUMMARY.

### Chat 4: đóng gói skill (B4)
Chat mới với `phases/STAGE4_SKILL_COMPILER.md`, dán Bible, mọi LOCK RECORD, script, scene plan, prompt tốt nhất kèm ghi chú lỗi, 3 khối hand-off và báo cáo QA của agent lắp ráp. Chạy K1 đến K4.

### Sau khi đăng
Ghi `metrics/VIDEO_REVIEW.md` ở ngày 3, 7, 28 theo `templates/VIDEO_PLAN_10.md`, đối chiếu giả thuyết và bảng quyết định. Kết quả thay đổi Bible (tiêu đề, hook, tỷ lệ pillar) thì tăng version trong Bible.

## 3. Gỡ rối
| Tình huống | Làm gì |
|---|---|
| Agent làm nhiều stage một lượt | Nhắc: "Một stage mỗi lượt, quay lại stage hiện tại." |
| Agent bịa số liệu | Hỏi nguồn ID (V##, F##); không có thì yêu cầu đánh dấu `[ASSUMPTION]` |
| Chat quá dài, agent quên luật | Mở chat mới, dán master prompt, Bible và lock record mới nhất, rồi `jump` |
| Muốn đổi tên sau khi chốt | Làm lại từ A1 theo danh sách cascade trong `docs/LESSONS.md` |
| Câu mở, câu kết nghe gượng | Đọc thành tiếng giữa một câu thường; gượng thì `revise` |
| Ảnh Flow lỗi chữ, đếm sai | Đưa ảnh cho agent chấm, thêm lỗi vào BANS theo bảng failure-fix |
| Muốn chạy đầy đủ một giai đoạn | Dán prompt gốc trong `phases/` thay cho master |
