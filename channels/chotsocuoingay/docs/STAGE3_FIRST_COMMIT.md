# STAGE 3: FIRST COMMIT, chotsocuoingay
Video 1: "Lương 15 triệu, cuối tháng còn 0: tiền đi đâu?" | P1 | story case study | 9 phút | chỉ tiếng Việt
Cập nhật gần nhất: 2026-10-11 (đổi sang visual v3, ghi LOCK L4 và L5).

## TRẠNG THÁI

| Layer | Trạng thái | Ghi chú |
|---|---|---|
| L0 Setup | Đã khóa | PACE_VI 264 từ/phút (đo lại ở L8) |
| L1 Packaging | Đã khóa, vá BAN 2026-10-11 | Thumbnail thực tế làm ở L9 |
| L2 Beat map | Đã khóa | 9 beat, tổng 2.371 từ sau L3 |
| L3 Voice và script | Đã khóa | 9 beat, facts đã kiểm |
| L4 Scene plan | Đã khóa, thêm cột Mode 2026-10-11 | 84 cảnh, 11 clip |
| L5 Visual và key assets | Đã khóa v3 (thay v2) | 6 key asset đã chốt |
| L6 Ảnh | CHƯA LÀM | Batch 1: S001-S006 |
| L7 Motion (Veo) | Chưa | 11 clip |
| L8 Voice, caption, nhạc, mix | Chưa | Đo lại PACE, xử lý "app" |
| L9 Thumbnail | Chưa | |
| L10 SEO và upload | Chưa | |
| L11 Remotion hand-off | Chưa | |

## CHANGELOG 2026-10-11
- Bỏ visual v2 (hình khối không mặt): thô và xấu theo đánh giá của creator. Thay bằng visual v3 (xem L5).
- L1: sửa BAN "mặt người" thành "biểu cảm sốc, miệng há, chỉ tay vào camera".
- L4: thêm cột Mode (IL/NF), viết lại "Ý hình ảnh" của 11 cảnh (S001, S002, S004, S009, S010, S026, S050, S058, S059, S084). Thêm LOCK RECORD L4 (trước đó chỉ có bảng).
- L5: làm lại, khóa v3. Ảnh v2 để ở folder `keyassets_v2_rejected/`.
- Stage 2 Bible cập nhật lên v2.1 (VISUAL v3, thumbnail ≤4 từ, anti-pattern 6).
- Khác biệt ở L0, L2, L3 (lời, số, beat): không có.

---


```
=== LOCK RECORD: L0 SETUP ===

LAYER: L0

DECISIONS
- Kênh: Chốt Sổ Cuối Ngày (@chotsocuoingay), ngôn ngữ Tiếng Việt (chỉ VI).
- Video đầu: "Lương 15 triệu, cuối tháng còn 0: tiền đi đâu?" | P1 Não bộ và tiền | story case study | hook H1.
- Thời lượng mục tiêu: 9 phút (540 giây).
- Giọng: VieNeu-TTS cục bộ; giọng dùng cho pace_test.wav (giọng chính thức chốt ở L8).

RULES
1. PACE_VI = 264 từ/phút, trong đó "từ" là một chuỗi tách bằng khoảng trắng, mỗi âm tiết một từ ("ki lô" = 2 từ), đếm đúng như văn bản kịch bản.
2. Thời lượng lời của một đoạn = số từ ÷ 264 × 60 giây, làm tròn 0,1 giây.
3. Ngân sách lời toàn video = 2.257-2.495 từ (±5% của 540 giây).
4. PACE chỉ đúng khi số được viết thành chữ (ví dụ "mười lăm triệu"). Nếu tts_text dùng chữ số, đo lại ở L8.
5. Đo lại PACE bằng giọng chính thức ở L8; nếu chênh quá 5% so với 264, cập nhật thời lượng cảnh.

BANS
- Giả định 140 hay 150 từ/phút (đã bị đo thực tế bác bỏ).
- Đếm "ki lô" hay từ ghép khác là 1 từ khi tính PACE.
- Tính thời lượng từ độ dài chữ viết mà không dùng số từ.

PARAMETERS
- PACE_VI: 264 từ/phút (150 từ / 34,11 giây).
- Khoảng ngắt đo được giữa các đoạn SRT: ~0,25 giây.
- Ngân sách lời video 9 phút: 2.257-2.495 từ (mục tiêu 2.376).

GOLDEN SAMPLE: pace_test.wav (34,11 giây) và pace_test.srt (4 đoạn, 150 từ).

CHECKS
1. Số từ của kịch bản cuối ÷ 264 × 60 nằm trong 513-567 giây.
2. Không có chữ số trong tts_text nếu PACE chưa đo lại.
3. Mỗi đoạn lời có số từ khớp planned_sec theo công thức (sai số ≤ 0,2 giây).

OPEN RISKS
- Giọng chưa chốt, PACE có thể đổi ở L8.
- Nếu chọn VOICE_SPEED chậm hơn, PACE giảm tương ứng [ASSUMPTION: tỷ lệ thuận, cần đo lại].
- 264 từ/phút khá nhanh cho người nghe lớn tuổi; cân nhắc làm chậm ở L8.

```

---

```
=== LOCK RECORD: L1 PACKAGING ===

LAYER: L1

DECISIONS
- Package A "Con số biến mất".
- Tiêu đề chính: "Lương 15 triệu, cuối tháng còn 0: tiền đi đâu?" (46 ký tự).
- Lời hứa: cộng từng khoản của một tháng lương 15 triệu (ví dụ minh họa) để thấy khoản nào là cần, khoản nào là thể diện, rồi tự làm bài kiểm tra 15 phút trên sổ của chính bạn.
- Thumbnail: tờ sổ ô li ở giữa, dòng trên là số lương, dòng cuối là chữ "0" đỏ lớn; chữ "15 TRIỆU, CÒN 0" (4 từ).

RULES
1. Chữ thumbnail ≤4 từ, cao tối thiểu 18% chiều cao khung.
2. Số then chốt màu #D7263D chiếm ≤10% diện tích khung.
3. Thumbnail phải qua "cover-the-title test": che tiêu đề vẫn tạo tò mò.
4. Tiêu đề ≤60 ký tự, từ khóa chính trong 40 ký tự đầu, dạng [số tiền cụ thể] + [tình huống] + [câu hỏi/phản biện].

BANS
- Tiền mặt, xấp tiền, đồng xu, ví (lý do: gợi "làm giàu").
- Biểu cảm sốc, miệng há, chỉ tay vào camera (lý do: tránh clickbait, tạo xấu hổ). [Cập nhật 2026-10-11 theo visual v3: mặt bình thản của Hà được phép; thumbnail có Hà hay không quyết định ở L9. Bản cũ: "Mặt người, biểu cảm sốc (lý do: nhân vật không mặt theo DNA)".]
- Mũi tên đi lên, biểu đồ tăng trưởng (lý do: gợi đầu tư, vùng cấm).
- Câu mệnh lệnh "nên/đừng" (lý do: cấm trong DNA).
- Quá 4 từ trên ảnh (lý do: không đọc được ở 160 px).

PARAMETERS
- Chữ thumbnail tối đa 4 từ; số đỏ ≤10% khung; tiêu đề ≤60 ký tự.

GOLDEN SAMPLE
- Xấu: ảnh người há miệng cầm xấp tiền, chữ "SỰ THẬT SỐC!".
- Tốt: tờ sổ ô li, một dòng 15.000.000, một chữ "0" đỏ lớn, chữ "15 TRIỆU, CÒN 0".

CHECKS
1. Đếm từ trên thumbnail ≤4.
2. Tiêu đề ≤60 ký tự và từ khóa chính nằm trong 40 ký tự đầu.
3. Che tiêu đề: thumbnail một mình vẫn gợi câu hỏi "tiền đi đâu?".
4. Không có vật thể trong danh sách cấm.

OPEN RISKS
- Chưa có dữ liệu CTR; package là [ASSUMPTION], đo sau 7 ngày.
- Hình ảnh thật của thumbnail làm ở L9, chưa tạo.
```

---

```
=== LOCK RECORD: L2 ANGLE AND BEAT MAP ===

LAYER: L2

DECISIONS
- Vấn đề sâu xa: thể diện lẫn trong chi tiêu mà không có dòng nào mang tên nó (F05, G03).
- Spine: Hero's Journey (story case study), 9 beat.
- Hạt giống (nhân vật minh họa, không phải trải nghiệm thật): (a) Hà, 26 tuổi, lương 15 triệu, ngày 20 chỉ còn ba trăm mười hai nghìn, "không nhớ tiền đã đi đâu"; (b) cắt ly cà phê không cứu được tháng lương, tiền biến mất ở vài khoản lớn mang tên thể diện; (c) người xem nghĩ khác: tiền đi vào những khoản chưa có tên; việc đầu tiên: 15 phút cộng chi tiêu tháng trước, gạch 3 khoản lớn nhất, hỏi "mình mua cho mình hay cho cái nhìn của người khác?".
- Bảng số (ví dụ minh họa, triệu đồng): Cố định 8,1 | Khoản nhỏ lặp lại 1,35 | Thể diện 3,2 | Trả sau 1,9 | Không nhớ 0,45 | Tổng 15,0.

BEAT MAP (từ | giây)
1 Hook, intro, disclaimer (200 | 45,5) → 2 Status quo (240 | 54,5) → 3 Call to adventure (280 | 63,6) → 4 Guide (280 | 63,6) → 5 Trial 1 (330 | 75,0) → 6 Trial 2 (330 | 75,0) → 7 Crisis (260 | 59,1) → 8 Resolution (310 | 70,5) → 9 New mindset + CTA (150 | 34,1). Tổng 2.380 từ, 540,9 giây.
Nối: B2 THEREFORE, B3 BUT, B4 THEREFORE, B5 THEREFORE, B6 BUT, B7 BUT, B8 THEREFORE, B9 THEREFORE.

RULES
1. Mỗi beat nối với beat trước bằng BUT hoặc THEREFORE như trên, không dùng "và rồi".
2. Vòng lặp mở ở beat 1 ("khoản không có tên") chỉ được giải ở đầu beat 7, tại khoảng 6:17.
3. Lời hứa trong hook dùng "sau sáu phút nữa" (không dùng "phút thứ sáu", vì beat 7 bắt đầu ở 6:17).
4. Số từ mỗi beat nằm trong ±10% mục tiêu; tổng 2.257-2.495 từ.
5. Nhân vật Hà gắn nhãn "nhân vật minh họa" trên màn hình ngay cảnh đầu; mọi số kèm "ví dụ minh họa".
6. Claim "não ít thấy đau khi trả sau" ở beat 5 ghi [VERIFY] đến khi có nguồn (tác giả, năm), không nói như sự thật.
7. Đúng 1 câu đồng cảm ở beat 7; đúng 1 câu hỏi bình luận ở beat 9, rồi "Chốt sổ hôm nay ở đây."

BANS
- "Và rồi" làm câu nối (lý do: không tạo nhân quả).
- Nêu tên "thể diện" cho khoản 3,2 triệu trước beat 6 (lý do: giữ vòng lặp mở).
- Bảo người xem cắt chi tiêu hay "nên/đừng" (lý do: cấm trong DNA).
- Tên người thật (lý do: SOUL).

PARAMETERS: bảng từ và giây ở trên; PACE_VI 264.

GOLDEN SAMPLE: bảng số 6 dòng ở trên.

CHECKS
1. Tổng từ kịch bản trong 2.257-2.495.
2. Beat 7 bắt đầu trong 6:10-6:25 theo timeline thật.
3. Tìm "phút thứ sáu" trong kịch bản: 0 kết quả.
4. Mỗi beat có đúng 1 câu hỏi mở ở cuối.

OPEN RISKS
- Hạt giống là nhân vật minh họa; nên thay bằng chuyện thật nếu có.
- Nguồn học thuật cho claim trả sau chưa có.
```

---

```
=== LOCK RECORD: L3.1 VOICE RULES ===

LAYER: L3 (hiệu chỉnh giọng)

DECISIONS
- Chọn hook A, công thức H1 (74 từ, 16,8 giây).
- Người dẫn "mình", gọi người xem "bạn"; nhân vật minh họa tên Hà, xưng "cô" khi kể.

RULES
1. Câu dài tối đa 25 từ; trung bình cả kịch bản 14 từ; riêng beat 1 (hook) trung bình tối thiểu 8 từ.
2. Mỗi đoạn tối đa 3 câu.
3. Số viết thành chữ trong kịch bản và tts_text (ví dụ "mười lăm triệu"), không dùng chữ số.
4. Hook có đúng 1 vòng lặp mở với lời hứa "sau sáu phút nữa".
5. Intro đúng 2 câu: "Mình là người chốt sổ của kênh này. Mỗi video, mình cộng từng khoản để xem tiền của bạn đi đâu."
6. Disclaimer đúng 15 từ: "Đây là ví dụ minh họa, không phải lời khuyên tài chính hay pháp lý."
7. Kết video: đúng 1 câu hỏi bình luận, rồi "Chốt sổ hôm nay ở đây."

BANS
- Toàn bộ từ cấm trong DNA v2 (ví dụ "nên mua/bán/vay/đầu tư", "đừng bỏ lỡ", "bản án", "con nợ").
- "Nên" khi dùng như lời khuyên về tiền (lý do: vùng cấm).
- Chữ số trong tts_text (lý do: PACE chỉ đúng khi số viết thành chữ).

PARAMETERS: PACE_VI 264 từ/phút; hook A = 74 từ.

GOLDEN SAMPLE (hook A):
Mười lăm triệu vào tài khoản đầu tháng. Cuối tháng, chỉ còn không đồng. Hà, hai mươi sáu tuổi, mở app hôm hai mươi và thấy ba trăm mười hai nghìn. Cô không nhớ tiền đã đi đâu. Cô không mua xe. Cô không mua nhà. Vậy mười lăm triệu ấy đã đi đâu? Trong sổ của Hà có một khoản không mang tên, và mình sẽ chỉ ra nó sau sáu phút nữa.

CHECKS
1. Không có chữ số 0-9 trong tts_text.
2. Không câu nào quá 25 từ.
3. Không có từ trong danh sách cấm (chạy tìm chuỗi).
4. Intro và disclaimer khớp từng chữ với quy tắc 5, 6.

OPEN RISKS
- Giọng đọc chính thức chưa chốt (L8).
- Phong cách câu ngắn ở hook có thể kéo trung bình toàn kịch bản xuống; kiểm tra lại ở bước đọc lại cuối.


L3.2 BEAT 1: ĐÃ KHÓA

Beat 1 chốt ở 156 từ = 35,5 giây. Bản này vào SCRIPT chạy.

Cập nhật các layer đã khóa (ripple đã kiểm):

L3.1 RULE 6 (cũ): Disclaimer đúng 15 từ.
L3.1 RULE 6 (mới): Không có disclaimer đọc thành lời. Miễn trừ nằm ở nhãn "VÍ DỤ MINH HỌA" trên bảng số và một dòng trong mô tả video.
L3.1 BAN thêm: Câu tự giải thích điều hiển nhiên trong lời đọc (lý do: người xem đã biết, làm chậm 15 giây đầu).
L3.1 CHECK 4 (mới): Intro khớp từng chữ rule 5; bảng số có nhãn; SEO sheet có dòng miễn trừ.
L2 RULE 5 (mới): Nhãn "VÍ DỤ MINH HỌA" chỉ ở bảng số, không nhãn "nhân vật minh họa" ở cảnh đầu.
L2 BEAT MAP (mới, từ): 160 | 260 | 300 | 280 | 330 | 330 | 260 | 310 | 150 = 2.380.

Kiểm timeline: lời hứa “sau sáu phút nữa” nói ở giây 16,8, beat 7 bắt đầu ở khoảng 6:16,4, lệch dưới 0,5 giây nên vẫn đúng.

```


| Beat | Từ | Giây | Câu | TB từ/câu | Dài nhất | Dấu ? |
|---|---|---|---|---|---|---|
| 1 | 156 | 35,5 | 14 | 11,1 | 20 | 1 |
| 2 | 268 | 60,9 | 22 | 12,2 | 20 | 1 |
| 3 | 294 | 66,8 | 18 | 16,3 | 23 | 1 |
| 4 | 267 | 60,7 | 17 | 15,7 | 24 | 1 |
| 5 | 333 | 75,7 | 24 | 13,9 | 23 | 1 |
| 6 | 329 | 74,8 | 22 | 15,0 | 23 | 1 |
| 7 | 270 | 61,4 | 17 | 15,9 | 23 | 1 |
| 8 | 305 | 69,3 | 21 | 14,5 | 24 | 1 |
| 9 | 149 | 33,9 | 11 | 13,5 | 25 | 1 |
| **Tổng** | **2.371** | **538,9** | **166** | **14,3** | **25** | |

- Ngân sách từ: 2.371, nằm trong 2.257-2.495. Thời lượng 538,9 giây, nằm trong 513-567.
- Beat 7 bắt đầu ở 374,3 giây (6:14). Lời hứa "sau sáu phút nữa" nói ở giây 16,8 nên rơi vào khoảng 6:17, lệch dưới 3 giây.
- Không chữ số 0-9 nào. Không câu nào quá 25 từ, không đoạn nào quá 3 câu.
- Không có "nên", "đừng", "và rồi", "phút thứ sáu", "bản án", "con nợ". Từ "thể diện" chỉ xuất hiện từ beat 7.
- Mỗi beat có đúng 1 dấu hỏi và nằm ở cuối beat (beat 9 là câu hỏi bình luận, sau đó là "Chốt sổ hôm nay ở đây.").
- Câu đồng cảm ở beat 7: đúng 1.
- Số tiền khớp bảng L2: 8,1 + 1,35 + 1,9 + 3,2 + 0,45 = 15,0.

## Khối 1: LOCK RECORD L3.2 (SCRIPT)

```
=== LOCK RECORD: L3.2 SCRIPT (BEAT 1-9) ===

LAYER: L3 (kịch bản)

DECISIONS
- Beat 1 sửa: bỏ disclaimer đọc thành lời; miễn trừ chỉ ở nhãn "VÍ DỤ MINH HỌA" trên bảng số và một dòng trong mô tả video.
- Người dẫn truyện cũng là "người chốt sổ"; "chị kế toán" (không tên) là người hướng dẫn (Guide) ở beat 4.
- Phương pháp trong truyện: "bốn hộp" = (1) cố định, (2) nhỏ lặp lại, (3) trả sau, (4) còn lại, phân loại bằng phép thử "bỏ dòng đó khỏi tháng sau, tháng có đổ hay không".
- Hộp bốn gồm: ba khoản có người khác ở cạnh (áo khoác 1,2 triệu; bữa tối nhóm bạn 1 triệu; quà sinh nhật và quỹ nhóm 1 triệu) = 3,2 triệu = "thể diện"; cộng 0,45 triệu dòng lẻ không nhớ, kịch bản thừa nhận đó là quên, không bịa lý do.
- Khoản "không mang tên" được gọi tên ở câu đầu beat 7 (khoảng 6:14).
- Bài tự kiểm tra 15 phút (4 bước) được kể qua Hà ở beat 8 và nhắc lại ở beat 9; câu hỏi then chốt: "mình mua cho mình hay cho cái nhìn của người khác".
- Beat 8 không nói người xem cắt chi tiêu; kết quả của Hà: "hộp bốn nhỏ đi, nhưng không phải vì cô tự cấm mình".
- Claim khoa học về "não ít thấy đau khi trả sau" KHÔNG dùng trong lời; beat 5 chỉ dùng quan sát: "trả sau dời cảm giác mất tiền sang ngày khác".

RULES
1. Mỗi beat có đúng 1 dấu hỏi, đặt ở cuối beat.
2. Mỗi beat nối beat trước bằng BUT hoặc THEREFORE như bảng dưới; từ nối mở câu: B3 "Nhưng", B5 "Vì thế", B6 "Nhưng", B7 "Nhưng", B8 "Vì vậy"; B4 và B9 nối bằng nội dung.
3. Khoản không mang tên được gọi tên đúng 1 lần ở đầu beat 7; từ "thể diện" cấm xuất hiện ở beat 1-6.
4. Câu đồng cảm: đúng 1 (beat 7).
5. Số tiền trong truyện phải cộng đúng 15,0 triệu theo bảng số.
6. Mỗi câu tối đa 25 từ; mỗi đoạn tối đa 3 câu; không chữ số.
7. Không có câu tự giải thích điều hiển nhiên hoặc câu phòng thủ trong lời đọc.

BANS
- Khẳng định "não ít thấy đau khi trả sau" (lý do: chưa có nguồn, [VERIFY]).
- Cho nhân vật chị kế toán tên thật hoặc chức danh cụ thể (lý do: SOUL, tránh người thật).
- Bảo người xem cắt hay giảm khoản nào (lý do: vùng cấm).
- Thêm dấu hỏi ngoài câu cuối beat (lý do: vòng lặp mở cần tập trung).

PARAMETERS
- PACE_VI 264 từ/phút; tổng 2.371 từ = 538,9 giây; beat 7 bắt đầu 374,3 giây.
- Từ và giây theo beat: 156 / 35,5 | 268 / 60,9 | 294 / 66,8 | 267 / 60,7 | 333 / 75,7 | 329 / 74,8 | 270 / 61,4 | 305 / 69,3 | 149 / 33,9.
- Liên kết: B2 THEREFORE | B3 BUT | B4 THEREFORE | B5 THEREFORE | B6 BUT | B7 BUT | B8 THEREFORE | B9 THEREFORE.

GOLDEN SAMPLE: câu mở beat 7: "Nhưng khoản không mang tên ấy thật ra có tên, và tên nó là thể diện."

CHECKS
1. Tổng từ 2.257-2.495, thời lượng 513-567 giây.
2. Beat 7 bắt đầu trong 370-385 giây.
3. Không chữ số 0-9; không từ trong danh sách cấm; không "thể diện" ở beat 1-6.
4. Mỗi beat đúng 1 dấu "?", ở cuối beat.
5. Không câu nào quá 25 từ; trung bình toàn kịch bản trong 13,5-14,5.

OPEN RISKS
- Trung bình beat 1 và 2 thấp (11,1 và 12,2); trung bình toàn kịch bản 14,3, đạt.
- "app" (beat 1, 2, 7) có thể bị VieNeu-TTS đọc sai; kiểm ở L8.
- Chi tiết "chị kế toán" là nhân vật hư cấu; thay bằng chuyện thật nếu bạn có.
- Beat 5 dùng "hơn một nửa tháng lương" và "chưa đến một phần mười", đã khớp bảng số nhưng cần giữ nguyên nếu đổi số.
```

## Khối 2: SCRIPT đầy đủ (tts_text, đã khóa)

```
[B1 | HOOK, INTRO, DẪN | 156 từ | 35,5 s]
Mười lăm triệu vào tài khoản đầu tháng. Cuối tháng, chỉ còn không đồng. Hà, hai mươi sáu tuổi, mở app hôm hai mươi và thấy ba trăm mười hai nghìn.
Cô không nhớ tiền đã đi đâu. Cô không mua xe. Cô không mua nhà.
Vậy mười lăm triệu ấy đã đi đâu? Trong sổ của Hà có một khoản không mang tên, và mình sẽ chỉ ra nó sau sáu phút nữa.
Mình là người chốt sổ của kênh này. Mỗi video, mình cộng từng khoản để xem tiền của bạn đi đâu.
Nếu tháng nào bạn cũng hết lương mà không nhớ mình đã tiêu vào đâu, video này dành cho bạn. Trong chín phút tới, mình sẽ cộng từng khoản trong tháng lương của Hà. Cuối video là một bài tự kiểm tra mười lăm phút cho chính sổ của bạn.
Bây giờ, mình bắt đầu với ngày hai mươi của Hà.

[B2 | STATUS QUO | 268 từ | 60,9 s]
Ngày hai mươi, chín giờ tối, Hà ngồi trên giường với điện thoại. Trong app ngân hàng, số dư là ba trăm mười hai nghìn. Còn mười ngày nữa mới đến kỳ lương.
Lương của Hà là mười lăm triệu, vào đều đặn mùng một mỗi tháng. Tháng đó không có biến cố nào: không ốm, không hỏng xe, không đám cưới. Trên giấy, đây là một tháng không có lý do gì để hết sạch.
Hà làm nhân viên văn phòng ở một công ty vừa, đi làm năm ngày một tuần. Cô thuê phòng chung cư nhỏ, ăn trưa gần công ty, cuối tuần đi cà phê với bạn. Nhìn từ ngoài, tháng nào của Hà cũng bình thường.
Hà có một giả thuyết riêng. Cô tin tiền đã đi vào những thứ nhỏ: ly trà sữa, bữa ăn ngoài, vài đơn mua trên mạng. Tháng trước cô cắt gần hết, và cuối tháng vẫn trống.
Điều làm cô khó chịu không phải là hết tiền. Nhiều người hết tiền vì một chuyện lớn, có thể kể ra. Còn Hà không kể được chuyện nào.
Tối đó, Hà kéo danh sách giao dịch từ đầu tháng. Có hàng chục dòng, dòng nào cũng nhỏ, dòng nào cũng nghe có lý. Cô cộng nhẩm trong đầu, cộng đến dòng thứ mười thì bỏ cuộc.
Cô tự nhủ: chắc là tháng này nhiều việc. Tháng sau sẽ khác. Nhưng tháng trước cô cũng nghĩ vậy, và tháng trước nữa cũng thế.
Nếu không có biến cố nào, thì mười lăm triệu ấy đang đi qua những dòng nào?

[B3 | CALL TO ADVENTURE | BUT | 294 từ | 66,8 s]
Nhưng đêm đó có một tin nhắn làm Hà không bỏ cuộc được nữa. Một người bạn rủ cô đi chơi cuối tuần, và cô trả lời rằng mình hết tiền rồi.
Người bạn gửi lại một câu hỏi rất ngắn, không có ý trách, rằng lương mười lăm triệu mà hết thật sao. Hà nhìn câu hỏi ấy một lúc lâu, vì cô nhận ra mình không có câu trả lời nào bằng con số.
Hai mươi sáu tuổi, cô tự lo được công việc, giấy tờ, cả lịch họp của một phòng. Vậy mà một tháng lương của chính mình, cô không theo dõi nổi. Chuyện đó làm cô thấy mình ngớ ngẩn hơn là thấy mình thiếu tiền.
Cô mở một trang trống trên máy tính và kẻ hai cột, một cột tên khoản, một cột số tiền. Không công thức, không màu mè. Cô chỉ muốn thấy từng dòng nằm yên ở một chỗ, thay vì trôi qua trong đầu.
Mới gõ được ba dòng, cô đã bí. Dòng bốn mươi ba nghìn ở một quán lạ không biết ghi là ăn uống hay gì khác. Dòng một trăm tám mươi nghìn cho một tiệm cô không nhớ tên cũng không biết xếp vào đâu.
Cô thử gạch bớt, gộp bớt, đặt tên đại cho vài dòng. Càng sửa, trang giấy càng rối, và đến gần nửa đêm cô tắt máy với cảm giác mình vừa tự làm khó mình. Cô bắt đầu nghi rằng tiền của mình đang đi qua những chỗ mà chính cô không nhìn thấy.
Sáng hôm sau, cô in trang ghi dở ấy ra rồi đến hỏi chị kế toán ngồi bàn bên cạnh. Chị kế toán sẽ chia những dòng ấy theo cách nào?

[B4 | GUIDE | THEREFORE | 267 từ | 60,7 s]
Chị kế toán nhìn trang giấy chừng mười giây rồi bật cười, không phải cười chê, mà như gặp lại một chuyện quen. Theo kinh nghiệm của chị, sổ rối thường vì ghi theo nơi tiêu tiền, chứ không ghi theo việc mà khoản đó đang làm.
Chị lấy bút gạch lên trang giấy, chia thành bốn hộp. Hộp một là những khoản cố định, tức là dù tháng có ra sao vẫn phải trả. Hộp hai là những khoản nhỏ lặp lại, tuần nào cũng có một chút.
Hộp ba là những thứ mua rồi nhưng tiền chưa rời tài khoản, như ví trả sau. Hộp bốn là hộp còn lại, dành cho mọi dòng không biết xếp vào đâu. Chị nói hộp bốn mới là hộp đáng nhìn nhất.
Rồi chị đưa Hà một phép thử cho từng dòng: bỏ dòng đó khỏi tháng sau, xem tháng có đổ hay không. Đổ thì vào hộp một. Không đổ mà tuần nào cũng quay lại thì vào hộp hai.
Hà không nói gì nhiều, chỉ chép lại bốn hộp vào máy. Cô thấy nhẹ đi một chút, vì lần đầu tiên những dòng rối đã có chỗ để ngồi. Chị còn thêm một câu mà cô nhớ mãi: sổ không cần đẹp, chỉ cần cộng đủ.
Chị cũng nói rõ rằng đây chỉ là cách nhìn, không phải đáp án. Hộp nào đầy, hộp nào vơi, tự con số sẽ cho thấy, và chị không đoán trước giúp ai.
Khi từng dòng bắt đầu rơi vào hộp, tháng lương của Hà sẽ hiện ra thế nào?

[B5 | TRIAL 1 | THEREFORE | 333 từ | 75,7 s]
Vì thế, tối hôm sau Hà bắt đầu từ hộp dễ nhất. Cô ghi mọi khoản phải trả dù tháng có ra sao: tiền phòng, điện nước, mạng, đi lại, ăn trưa. Cộng lại, được tám triệu một trăm nghìn.
Con số này làm cô ngạc nhiên, vì cô vẫn nghĩ phần cố định chỉ khoảng sáu triệu. Hóa ra hơn một nửa tháng lương đã có chủ từ ngày mùng một, trước cả khi cô kịp quyết định điều gì.
Sang hộp thứ hai, Hà mong tìm thấy thủ phạm mà cô đã nghi suốt tháng. Trà sữa, cà phê, bữa ăn ngoài, những đơn mua trên mạng, cô cộng từng dòng một. Tổng cộng, một triệu ba trăm năm mươi nghìn.
Cô nhìn con số ấy rất lâu. Chưa đến một phần mười tháng lương. Giả thuyết riêng của cô đã sai, và ly trà sữa hóa ra chỉ là người bị nghi oan.
Rồi đến hộp thứ ba, và đây là chỗ Hà khựng lại. Trong danh sách có nhiều dòng mang chữ ví trả sau, mà cô chưa bao giờ xếp vào chuyện tiêu tiền. Lúc mua, cô đâu có trả đồng nào, vì thế trong đầu cô, những dòng đó chưa từng xảy ra.
Cô cộng lại. Một triệu chín trăm nghìn, nhiều hơn cả hộp thứ hai, mà trong đầu cô chưa từng là tiền.
Mình dừng ở đây một chút, vì chỗ này rất dễ lọt qua. Trả sau không làm tiền biến mất, nó chỉ dời cảm giác mất tiền sang một ngày khác. Đến ngày đó, tài khoản vẫn phải trả.
Đã gần mười một giờ đêm. Cô cộng ba hộp lại được mười một triệu ba trăm năm mươi nghìn, trong khi lương là mười lăm triệu. Phần còn lại, ba triệu sáu trăm năm mươi nghìn, chưa hộp nào nhận.
Gần một phần tư tháng lương đang nằm trong những dòng cô chưa xếp được vào đâu. Những dòng ấy là gì?

[B6 | TRIAL 2 | BUT | 329 từ | 74,8 s]
Nhưng hộp bốn không chịu im lặng như ba hộp kia. Hà mở từng dòng ra xem, ghi thêm ngày và thứ cô đã mua, rồi dần nhớ được hầu hết.
Dòng đầu tiên là một chiếc áo khoác, một triệu hai trăm nghìn, mua trước buổi họp mặt đầu tháng. Cô vẫn còn một chiếc áo khoác khác ở nhà, vẫn mặc tốt. Hôm đó cô chỉ nghĩ rằng mình cần trông ổn một chút.
Dòng thứ hai là bữa tối của nhóm bạn, một triệu đồng. Cô trả hết khi mọi người còn đang tính chia, vì thấy chia từng nghìn trước mặt người khác có vẻ keo kiệt. Về nhà, cô mới nhận ra mình đã trả phần của bốn người.
Dòng thứ ba gộp lại quà sinh nhật và tiền góp quỹ nhóm, một triệu nữa. Chẳng khoản nào lớn, chẳng khoản nào cô hối hận ngay lúc trả. Nhưng ba khoản cộng lại là ba triệu hai trăm nghìn, hơn hai lần tiền trà sữa và ăn ngoài của cả tháng.
Còn lại bốn trăm năm mươi nghìn là những dòng lẻ mà dù cố đến đâu cô cũng không nhớ nổi. Mình sẽ không bịa ra lý do cho chúng, vì có những khoản trong sổ chỉ đơn giản là đã quên.
Nhưng ba dòng kia thì khác. Hà đã nhớ rất rõ lúc cô trả, nhớ cả lý do trong đầu, mà vẫn không biết gọi chúng là gì. Chúng không phải ăn uống, không phải đi lại, không phải một món cô thật sự cần.
Hà đặt bút xuống và thử một cách khác. Cô không hỏi ba dòng ấy là gì, mà hỏi lúc trả cô đang đứng cạnh ai.
Câu trả lời làm cô im lặng. Áo khoác, bữa tối, món quà: lúc nào cũng có người khác ở đó, hoặc sắp nhìn thấy.
Cô lấy bút khoanh tròn ba dòng ấy. Ba dòng ấy đang giữ điều gì?

[B7 | CRISIS | BUT | 270 từ | 61,4 s]
Nhưng khoản không mang tên ấy thật ra có tên, và tên nó là thể diện. Không ai ghi chữ đó vào sổ, nó chỉ nằm lẫn trong áo khoác, bữa tối, quà tặng. Ba triệu hai trăm nghìn, hơn hai mươi phần trăm tháng lương, và không dòng nào mang tên nó.
Đến đây, câu chuyện của Hà không còn là chuyện hết tiền nữa. Cô không thiếu kỷ luật, vì cô đã ghi, đã cộng, đã chia hộp đến tận khuya. Cô vừa thấy một phần lương của mình đang trả cho cảm giác không muốn kém ai trong mắt người khác.
Nếu nghe đến đây mà bạn thấy quen, điều đó rất con người, và không có gì để xấu hổ.
Điều khó nhất là ba dòng ấy không hề vô lý. Áo khoác giúp cô tự tin hơn trong buổi họp mặt, bữa tối giúp cô giữ chỗ trong nhóm bạn. Món quà giúp cô không bị nhớ là người đến tay không, và mỗi dòng đều có một lý do rất hợp lý.
Vì thế chúng rất dễ lọt khỏi mọi cuốn sổ. Trong app ngân hàng, chúng mang tên quán ăn, tên cửa hàng, chưa bao giờ mang tên điều cô thật sự đã mua. Cô mua đúng thứ cô muốn, chỉ là thứ cô muốn không nằm trên hóa đơn.
Cô ngồi yên rất lâu. Lần đầu, cô không thấy tiền biến mất. Cô thấy tiền đã đến những nơi do chính cô chọn, chỉ là cô không biết mình đang chọn.
Biết tên khoản ấy rồi, Hà sẽ làm gì với nó?

[B8 | RESOLUTION | THEREFORE | 305 từ | 69,3 s]
Vì vậy, Hà quyết định không làm gì lớn lao cả. Cô chỉ giữ lại đúng phần đã cho cô thấy sự thật: mười lăm phút, một trang sổ, bốn hộp. Cô gọi đó là bài chốt sổ.
Bước một, cô lấy sao kê của tháng trước và chép từng dòng ra một trang, chưa cần hiểu. Bước hai, cô xếp mỗi dòng vào một trong bốn hộp. Bước ba, cô cộng từng hộp và đặt cạnh tiền lương.
Rồi đến bước bốn, bước Hà nhớ nhất. Cô khoanh ba khoản lớn nhất trong hộp còn lại. Với mỗi khoản, cô tự hỏi một câu duy nhất: mình mua khoản này cho mình, hay cho cái nhìn của người khác.
Câu hỏi ấy nghe đơn giản, nhưng nó làm một việc mà bốn hộp không làm được. Nó đưa những khoản vô danh trở lại thành lựa chọn có tên, và có tên thì mới cân nhắc được.
Cả bài làm hết mười lăm phút, không cần bảng tính, không cần ứng dụng. Chỉ cần sao kê tháng trước và một cây bút. Mình để bốn bước này lại cho bạn thử trên sổ của chính bạn, vào lúc nào bạn rảnh.
Tháng sau, Hà làm lại bài chốt sổ y như vậy. Hộp bốn nhỏ đi, nhưng không phải vì cô tự cấm mình. Có dòng cô hỏi xong không còn muốn mua, và có dòng cô hỏi xong vẫn mua, lần này với cái đầu rõ ràng.
Hà vẫn đi ăn với nhóm bạn, vẫn trả phần của mình. Chỉ khác là dòng đó bây giờ có tên, và cô biết chính xác mình đang trả cho điều gì. Cô thấy mình đỡ phải giải thích với chính mình.
Vậy sau một tháng chốt sổ, Hà thật sự đã thay đổi điều gì?

[B9 | NEW MINDSET + CTA | THEREFORE | 149 từ | 33,9 s]
Một tháng sau, Hà không giàu lên. Điều đổi khác nhỏ hơn thế: khi người bạn hỏi lại, cô trả lời được bằng con số, và con số ấy có tên. Ba triệu hai trăm nghìn của tháng đầu giờ đã có tên cho từng dòng.
Tiền không bao giờ biến mất. Nó đi đến những chỗ mình chưa gọi tên, và chỗ nào chưa có tên thì chưa phải lựa chọn của mình. Việc của người chốt sổ chỉ là gọi tên từng khoản.
Việc đầu tiên rất nhỏ. Mười lăm phút, sao kê tháng trước, bốn hộp. Rồi khoanh ba khoản lớn nhất ở hộp cuối, và hỏi chính mình xem mình mua cho mình hay cho cái nhìn của người khác.
Trong hộp cuối của bạn, khoản nào bạn đoán là mua cho cái nhìn của người khác nhiều nhất?
Chốt sổ hôm nay ở đây.
```

## Khối 3: BẢNG FACTS

| Câu trong lời | Nguồn | Trạng thái |
|---|---|---|
| Mọi con số tiền, nhân vật Hà, chị kế toán, bạn bè | Hư cấu minh họa, tự nhất quán theo bảng số L2 | Không cần xác minh |
| "Trả sau dời cảm giác mất tiền sang ngày khác" | Quan sát mô tả hành vi, không dẫn nghiên cứu | OK, nếu muốn nói về cơ chế não thì cần nguồn [VERIFY] |
| "Sổ rối thường vì ghi theo nơi tiêu tiền" (beat 4) | Gán cho kinh nghiệm cá nhân của nhân vật, không nói như quy luật chung | OK |
| "Hơn hai mươi phần trăm", "chưa đến một phần mười", "gần một phần tư", "hơn một nửa", "hơn hai lần" | Tính từ bảng số: 3,2/15 = 21%; 1,35/15 = 9%; 3,65/15 = 24%; 8,1/15 = 54%; 3,2/1,35 = 2,4 | Đã kiểm |

```
=== LOCK RECORD: L4 SCENE PLAN (suy ra từ bảng đã duyệt; creator xác nhận bằng cách giữ file này) ===

LAYER: L4

DECISIONS
- 84 cảnh, tổng 538,6 giây, 2.371 từ, PACE 264 từ/phút.
- Mỗi cảnh một đơn vị lời; narration là bản cuối, không sửa ở bước sau.
- 11 clip animate, 73 ảnh tĩnh có hiệu ứng Remotion.
- (mới) Mỗi cảnh có Mode: IL (ILLUSTRATION) hoặc NF (NOTEBOOK-FLAT) theo nội dung cảnh. NF gồm 19 cảnh: S028 S029 S030 S037 S038 S040 S044 S047 S053 S060 S061 S068 S071 S072 S073 S076 S080 S081 S082. IL gồm 65 cảnh còn lại (kể cả S066, S070, S083).
- Trong 11 clip, 3 clip là cảnh NF (S028, S060, S076); 8 clip còn lại là IL.

RULES
1. Hook zone = 45 giây đầu: 8 cảnh bắt đầu trong vùng này, 6 là clip (75%, ≥70%).
2. Ngoài hook zone: 5 clip (S017, S028, S042, S060, S076) trong ~495 giây, tối đa 1 clip mỗi 60 giây.
3. Lý do được animate ngoài hook zone: một sự kiện lộ ra, một chuyển đổi, một đỉnh cảm xúc, một đổi chương.
4. Preset ảnh tĩnh: hold, push_in, pull_out, pan_left, pan_right, pan_down, drift_diag, focus_push; không lặp một preset 3 cảnh liên tiếp; hold chỉ dùng cho cảnh INF hoặc TTL.
5. Chuyển cảnh chỉ cut hoặc crossfade_6f.
6. Clip dùng clip_fit hold_last (không đổi tốc độ).

8. (mới) Chữ trên màn hình (cột cuối) do Remotion vẽ; ảnh và clip không chứa chữ.

BANS
- Ảnh nguồn của clip có chữ hoặc số (lý do: Veo làm méo chữ).
- Hai clip liên tiếp ngoài hook zone (lý do: vượt 1 clip/60 giây).


PARAMETERS: 84 cảnh; 538,6 s; hook zone 45 s; clip 11 (6 trong hook zone, 5 ngoài); NF 19; IL 65.

GOLDEN SAMPLE: bảng SCENE PLAN bên dưới.

CHECKS
1. Tổng giây 513-567 và mỗi cảnh khớp số từ ÷ 264 × 60 (sai số ≤ 0,2 s).
2. Hook zone có ≥70% cảnh là clip.
3. Không preset nào 3 cảnh liên tiếp.
4. Mọi cảnh có Mode; số IL + NF = 84.
5. Cảnh NF không có mặt người; cảnh IL có mặt thì miệng khép.

OPEN RISKS
- Hook zone 45 giây là [ASSUMPTION], chưa có dữ liệu retention.
- Khi đo lại PACE ở L8 mà chênh >5%, phải tính lại giây cảnh.
- Clip NF (S028, S060, S076) cần prompt Veo riêng ở L7 (chuyển động phẳng, không có người).
```

# SCENE PLAN: Lương 15 triệu, cuối tháng còn 0: tiền đi đâu?

Tổng 84 cảnh | 538.6 giây | 2371 từ | PACE 264 từ/phút | 11 clip animate | 84 ảnh nguồn | mode: 65 IL (ILLUSTRATION), 19 NF (NOTEBOOK-FLAT)

Chú thích cột Mode: IL = ILLUSTRATION (STYLE BIBLE ILLUSTRATION, nhân vật có mặt); NF = NOTEBOOK-FLAT (STYLE BIBLE NOTEBOOK-FLAT, trang sổ ô li phẳng). Chọn theo nội dung cảnh, không theo cột Loại.

| ID | Beat | Start (s) | Giây | Loại | Mode | Narration (nguyên văn) | Ý hình ảnh | Media | Hiệu ứng / clip fit | Chuyển cảnh | Chữ trên màn hình |
|---|---|---|---|---|---|---|---|---|---|---|---|
| S001 | B1 | 0 | 7.0 | OBJ | IL | Mười lăm triệu vào tài khoản đầu tháng. Cuối tháng, chỉ còn không đồng. Hà, hai mươi sáu tuổi, mở app hôm hai mươi và thấy ba trăm mười hai nghìn. | Cận từ trên xuống một trang sổ ô li trên bàn gỗ sáng: dòng đầu có vệt bút, ở dòng cuối một vòng tròn đỏ vẽ tay lớn dần (vòng "không"); cốc cà phê và chậu cây ở mép khung. [chữ 15.000.000 → 0 do Remotion] | clip | clip_fit: hold_last | cut | 15.000.000 → 0 |
| S002 | B1 | 7.0 | 5.2 | CIN | IL | Cô không nhớ tiền đã đi đâu. Cô không mua xe. Cô không mua nhà. Vậy mười lăm triệu ấy đã đi đâu? | Hà ngồi mép giường trong phòng thuê đêm (khuôn KA06), ba phần tư sau lưng, mắt nhìn xuống điện thoại, miệng khép, ánh điện thoại hắt lên má. | clip | clip_fit: hold_last | cut | 312.000 |
| S003 | B1 | 12.3 | 6.4 | OBJ | IL | Trong sổ của Hà có một khoản không mang tên, và mình sẽ chỉ ra nó sau sáu phút nữa. Mình là người chốt sổ của kênh này. | Cuốn sổ mở trên bàn, một dòng bị bỏ trống không tên, cây bút lơ lửng chưa đặt xuống. | clip | clip_fit: hold_last | cut |  |
| S004 | B1 | 18.6 | 3.0 | TTL | IL | Mỗi video, mình cộng từng khoản để xem tiền của bạn đi đâu. | Một bàn tay gập cuốn sổ trên bàn gỗ sáng; | clip | clip_fit: hold_last | cut | CHỐT SỔ CUỐI NGÀY |
| S005 | B1 | 21.6 | 7.7 | OBJ | IL | Nếu tháng nào bạn cũng hết lương mà không nhớ mình đã tiêu vào đâu, video này dành cho bạn. Trong chín phút tới, mình sẽ cộng từng khoản trong tháng lương của Hà. | Cuốn lịch để bàn lật qua vài tháng liên tiếp, bên cạnh cuốn sổ vẫn trống. | clip | clip_fit: hold_last | cut |  |
| S006 | B1 | 29.3 | 6.1 | OBJ | IL | Cuối video là một bài tự kiểm tra mười lăm phút cho chính sổ của bạn. Bây giờ, mình bắt đầu với ngày hai mươi của Hà. | Trang lịch dừng ở ngày hai mươi, một vòng tròn bút quanh con số. | image | focus_push {"from": 1.0, "to": 1.12, "focus": [0.5, 0.5]} | cut |  |
| S007 | B2 | 35.5 | 5.7 | CIN | IL | Ngày hai mươi, chín giờ tối, Hà ngồi trên giường với điện thoại. Trong app ngân hàng, số dư là ba trăm mười hai nghìn. | Hà ngồi trên giường với điện thoại, căn phòng thuê nhỏ về đêm, màn hình sáng. | clip | clip_fit: hold_last | crossfade_6f |  |
| S008 | B2 | 41.1 | 8.4 | OBJ | IL | Còn mười ngày nữa mới đến kỳ lương. Lương của Hà là mười lăm triệu, vào đều đặn mùng một mỗi tháng. Tháng đó không có biến cố nào: không ốm, không hỏng xe, không đám cưới. | Lịch tháng: ô mùng một đánh dấu, mười ô cuối tháng còn trống. | image | pan_right {"travel_pct": 6, "scale": 1.06} | cut |  |
| S009 | B2 | 49.5 | 7.0 | CIN | IL | Trên giấy, đây là một tháng không có lý do gì để hết sạch. Hà làm nhân viên văn phòng ở một công ty vừa, đi làm năm ngày một tuần. | Hà ở bàn văn phòng ban ngày, ba phần tư sau lưng, màn hình và giấy tờ gọn gàng, đồng nghiệp ở hậu cảnh. | image | pan_left {"travel_pct": 6, "scale": 1.06} | cut |  |
| S010 | B2 | 56.6 | 6.4 | CIN | IL | Cô thuê phòng chung cư nhỏ, ăn trưa gần công ty, cuối tuần đi cà phê với bạn. Nhìn từ ngoài, tháng nào của Hà cũng bình thường. | Phòng chung cư nhỏ, ban công; Hà và một người bạn (áo xanh nhạt) ngồi cà phê, hai ly trên bàn, cả hai bình thản. | image | drift_diag {"travel_pct": 5, "scale": 1.06, "dir": "tl_to_br"} | cut |  |
| S011 | B2 | 63.0 | 5.9 | OBJ | IL | Hà có một giả thuyết riêng. Cô tin tiền đã đi vào những thứ nhỏ: ly trà sữa, bữa ăn ngoài, vài đơn mua trên mạng. | Trên bàn: ly trà sữa, hộp ăn trưa mang đi, vài túi đơn hàng nhỏ. | image | pan_right {"travel_pct": 6, "scale": 1.06} | cut |  |
| S012 | B2 | 68.9 | 7.5 | OBJ | IL | Tháng trước cô cắt gần hết, và cuối tháng vẫn trống. Điều làm cô khó chịu không phải là hết tiền. Nhiều người hết tiền vì một chuyện lớn, có thể kể ra. | Cái bàn vắng đồ sau khi cắt bớt, chiếc ví mỏng dưới ánh đèn lạnh. | image | push_in {"from": 1.0, "to": 1.08} | cut |  |
| S013 | B2 | 76.4 | 7.3 | OBJ | IL | Còn Hà không kể được chuyện nào. Tối đó, Hà kéo danh sách giao dịch từ đầu tháng. Có hàng chục dòng, dòng nào cũng nhỏ, dòng nào cũng nghe có lý. | Danh sách giao dịch dài trên màn hình điện thoại, ngón tay kéo xuống. | image | pan_down {"travel_pct": 6, "scale": 1.06} | cut |  |
| S014 | B2 | 83.6 | 5.9 | CIN | IL | Cô cộng nhẩm trong đầu, cộng đến dòng thứ mười thì bỏ cuộc. Cô tự nhủ: chắc là tháng này nhiều việc. Tháng sau sẽ khác. | Hà cộng nhẩm, ngón tay dừng giữa chừng trên màn hình rồi buông. | image | push_in {"from": 1.0, "to": 1.08} | cut |  |
| S015 | B2 | 89.5 | 6.8 | CIN | IL | Nhưng tháng trước cô cũng nghĩ vậy, và tháng trước nữa cũng thế. Nếu không có biến cố nào, thì mười lăm triệu ấy đang đi qua những dòng nào? | Hà nhìn ra cửa sổ đêm, điện thoại sáng trên tay, căn phòng mở rộng dần. | image | pull_out {"from": 1.08, "to": 1.0} | cut |  |
| S016 | B3 | 96.4 | 7.3 | OBJ | IL | Nhưng đêm đó có một tin nhắn làm Hà không bỏ cuộc được nữa. Một người bạn rủ cô đi chơi cuối tuần, và cô trả lời rằng mình hết tiền rồi. | Màn hình điện thoại với một bong bóng tin nhắn mời đi chơi (không chữ đọc được), đêm. | image | push_in {"from": 1.0, "to": 1.08} | crossfade_6f |  |
| S017 | B3 | 103.6 | 5.0 | OBJ | IL | Người bạn gửi lại một câu hỏi rất ngắn, không có ý trách, rằng lương mười lăm triệu mà hết thật sao. | Một bong bóng tin nhắn ngắn trượt lên màn hình, không có chữ đọc được. | clip | clip_fit: hold_last | cut |  |
| S018 | B3 | 108.6 | 5.0 | CIN | IL | Hà nhìn câu hỏi ấy một lúc lâu, vì cô nhận ra mình không có câu trả lời nào bằng con số. | Hà ngồi lặng, ánh điện thoại hắt lên vai áo, nhìn nghiêng. | image | push_in {"from": 1.0, "to": 1.08} | cut |  |
| S019 | B3 | 113.6 | 7.0 | CIN | IL | Hai mươi sáu tuổi, cô tự lo được công việc, giấy tờ, cả lịch họp của một phòng. Vậy mà một tháng lương của chính mình, cô không theo dõi nổi. | Hà ở văn phòng xử lý giấy tờ, lịch họp của cả phòng treo sau lưng. | image | pan_right {"travel_pct": 6, "scale": 1.06} | cut |  |
| S020 | B3 | 120.7 | 7.7 | OBJ | IL | Chuyện đó làm cô thấy mình ngớ ngẩn hơn là thấy mình thiếu tiền. Cô mở một trang trống trên máy tính và kẻ hai cột, một cột tên khoản, một cột số tiền. | Laptop mở một trang trống chia hai cột, con trỏ nhấp nháy. | image | focus_push {"from": 1.0, "to": 1.12, "focus": [0.5, 0.5]} | cut |  |
| S021 | B3 | 128.4 | 7.0 | OBJ | IL | Không công thức, không màu mè. Cô chỉ muốn thấy từng dòng nằm yên ở một chỗ, thay vì trôi qua trong đầu. Mới gõ được ba dòng, cô đã bí. | Ba dòng đầu được gõ vào, phần còn lại của trang vẫn trống. | image | drift_diag {"travel_pct": 5, "scale": 1.06, "dir": "br_to_tl"} | cut |  |
| S022 | B3 | 135.5 | 8.4 | OBJ | IL | Dòng bốn mươi ba nghìn ở một quán lạ không biết ghi là ăn uống hay gì khác. Dòng một trăm tám mươi nghìn cho một tiệm cô không nhớ tên cũng không biết xếp vào đâu. | Sao kê điện thoại, hai dòng khó đoán được ngón tay chỉ vào. | image | pan_down {"travel_pct": 6, "scale": 1.06} | cut |  |
| S023 | B3 | 143.9 | 8.0 | CIN | IL | Cô thử gạch bớt, gộp bớt, đặt tên đại cho vài dòng. Càng sửa, trang giấy càng rối, và đến gần nửa đêm cô tắt máy với cảm giác mình vừa tự làm khó mình. | Gần nửa đêm, trang giấy chi chít nét gạch, Hà tắt màn hình. | image | push_in {"from": 1.0, "to": 1.08} | cut |  |
| S024 | B3 | 151.8 | 4.3 | OBJ | IL | Cô bắt đầu nghi rằng tiền của mình đang đi qua những chỗ mà chính cô không nhìn thấy. | Trang giấy rối, vài đường mảnh kéo ra ngoài mép giấy, mờ dần. | image | pull_out {"from": 1.08, "to": 1.0} | cut |  |
| S025 | B3 | 156.1 | 7.0 | CIN | IL | Sáng hôm sau, cô in trang ghi dở ấy ra rồi đến hỏi chị kế toán ngồi bàn bên cạnh. Chị kế toán sẽ chia những dòng ấy theo cách nào? | Buổi sáng, Hà cầm trang giấy in đi qua dãy bàn tới bàn chị kế toán. | image | pan_right {"travel_pct": 6, "scale": 1.06} | crossfade_6f |  |
| S026 | B4 | 163.2 | 5.2 | CIN | IL | Chị kế toán nhìn trang giấy chừng mười giây rồi bật cười, không phải cười chê, mà như gặp lại một chuyện quen. | Chị kế toán (KA02) ngồi ở bàn, nhìn trang giấy Hà đưa và cười nhẹ, miệng khép, nắng sớm bên cửa sổ; Hà đứng cạnh, ba phần tư sau lưng. | image | push_in {"from": 1.0, "to": 1.08} | crossfade_6f |  |
| S027 | B4 | 168.4 | 5.5 | OBJ | IL | Theo kinh nghiệm của chị, sổ rối thường vì ghi theo nơi tiêu tiền, chứ không ghi theo việc mà khoản đó đang làm. | Bàn tay chị chỉ dọc theo từng dòng trên trang giấy. | image | focus_push {"from": 1.0, "to": 1.12, "focus": [0.5, 0.55]} | cut |  |
| S028 | B4 | 173.9 | 6.4 | INF | NF | Chị lấy bút gạch lên trang giấy, chia thành bốn hộp. Hộp một là những khoản cố định, tức là dù tháng có ra sao vẫn phải trả. | Nét bút chia trang rối thành bốn khung hộp gọn gàng. | clip | clip_fit: hold_last | cut |  |
| S029 | B4 | 180.2 | 7.0 | INF | NF | Hộp hai là những khoản nhỏ lặp lại, tuần nào cũng có một chút. Hộp ba là những thứ mua rồi nhưng tiền chưa rời tài khoản, như ví trả sau. | Bốn hộp trên trang, ba hộp đầu có nhãn, hộp thứ tư còn bỏ ngỏ. | image | hold {} | cut | 1 CỐ ĐỊNH · 2 NHỎ LẶP LẠI · 3 TRẢ SAU |
| S030 | B4 | 187.3 | 5.7 | INF | NF | Hộp bốn là hộp còn lại, dành cho mọi dòng không biết xếp vào đâu. Chị nói hộp bốn mới là hộp đáng nhìn nhất. | Hộp thứ tư được khoanh nhẹ, nổi lên giữa ba hộp còn lại. | image | focus_push {"from": 1.0, "to": 1.12, "focus": [0.75, 0.5]} | cut | 4 CÒN LẠI |
| S031 | B4 | 193.0 | 6.1 | OBJ | IL | Rồi chị đưa Hà một phép thử cho từng dòng: bỏ dòng đó khỏi tháng sau, xem tháng có đổ hay không. Đổ thì vào hộp một. | Đầu bút của chị chỉ vào một dòng, hai ngón tay giữ mép trang. | image | drift_diag {"travel_pct": 5, "scale": 1.06, "dir": "tl_to_br"} | cut |  |
| S032 | B4 | 199.1 | 5.5 | CIN | IL | Không đổ mà tuần nào cũng quay lại thì vào hộp hai. Hà không nói gì nhiều, chỉ chép lại bốn hộp vào máy. | Hà chép lại bốn hộp vào laptop ở bàn làm việc. | image | pan_left {"travel_pct": 6, "scale": 1.06} | cut |  |
| S033 | B4 | 204.5 | 8.0 | CIN | IL | Cô thấy nhẹ đi một chút, vì lần đầu tiên những dòng rối đã có chỗ để ngồi. Chị còn thêm một câu mà cô nhớ mãi: sổ không cần đẹp, chỉ cần cộng đủ. | Hà ngả lưng nhẹ nhõm, trang sổ đã gọn trước mặt. | image | push_in {"from": 1.0, "to": 1.08} | cut |  |
| S034 | B4 | 212.5 | 7.5 | OBJ | IL | Chị cũng nói rõ rằng đây chỉ là cách nhìn, không phải đáp án. Hộp nào đầy, hộp nào vơi, tự con số sẽ cho thấy, và chị không đoán trước giúp ai. | Chị đặt bút xuống, trang giấy gấp góc, cây bút nằm cạnh. | image | pan_right {"travel_pct": 6, "scale": 1.06} | cut |  |
| S035 | B4 | 220.0 | 3.9 | CIN | IL | Khi từng dòng bắt đầu rơi vào hộp, tháng lương của Hà sẽ hiện ra thế nào? | Hà ở bàn, bốn hộp trống trên màn hình, cả căn phòng mở rộng dần. | image | pull_out {"from": 1.08, "to": 1.0} | cut |  |
| S036 | B5 | 223.9 | 7.3 | CIN | IL | Vì thế, tối hôm sau Hà bắt đầu từ hộp dễ nhất. Cô ghi mọi khoản phải trả dù tháng có ra sao: tiền phòng, điện nước, mạng, đi lại, ăn trưa. | Tối hôm sau, laptop sáng trong phòng nhỏ, Hà gõ vào hộp thứ nhất. | image | push_in {"from": 1.0, "to": 1.08} | crossfade_6f |  |
| S037 | B5 | 231.1 | 5.9 | INF | NF | Cộng lại, được tám triệu một trăm nghìn. Con số này làm cô ngạc nhiên, vì cô vẫn nghĩ phần cố định chỉ khoảng sáu triệu. | Hộp thứ nhất đầy, thanh ngang chiếm hơn một nửa chiều dài tháng lương. | image | hold {} | cut | 8.100.000 |
| S038 | B5 | 237.0 | 5.2 | INF | NF | Hóa ra hơn một nửa tháng lương đã có chủ từ ngày mùng một, trước cả khi cô kịp quyết định điều gì. | Thanh ngang mười lăm phần, tám phần đầu được tô màu đã có chủ. | image | pan_right {"travel_pct": 6, "scale": 1.06} | cut |  |
| S039 | B5 | 242.3 | 7.5 | OBJ | IL | Sang hộp thứ hai, Hà mong tìm thấy thủ phạm mà cô đã nghi suốt tháng. Trà sữa, cà phê, bữa ăn ngoài, những đơn mua trên mạng, cô cộng từng dòng một. | Các món nhỏ xếp hàng: trà sữa, cà phê, hộp ăn, túi đơn hàng. | image | pan_left {"travel_pct": 6, "scale": 1.06} | cut |  |
| S040 | B5 | 249.8 | 5.2 | INF | NF | Tổng cộng, một triệu ba trăm năm mươi nghìn. Cô nhìn con số ấy rất lâu. Chưa đến một phần mười tháng lương. | Hộp thứ hai: một thanh ngắn, chưa đến một phần mười lương. | image | hold {} | cut | 1.350.000 |
| S041 | B5 | 255.0 | 7.0 | CIN | IL | Giả thuyết riêng của cô đã sai, và ly trà sữa hóa ra chỉ là người bị nghi oan. Rồi đến hộp thứ ba, và đây là chỗ Hà khựng lại. | Ly trà sữa đặt yên trên bàn, Hà nhìn nó bình thản. | image | push_in {"from": 1.0, "to": 1.08} | cut |  |
| S042 | B5 | 262.0 | 4.8 | OBJ | IL | Trong danh sách có nhiều dòng mang chữ ví trả sau, mà cô chưa bao giờ xếp vào chuyện tiêu tiền. | Màn hình điện thoại: vài dòng giao dịch hiện ra với biểu tượng ví nhỏ. | clip | clip_fit: hold_last | cut | VÍ TRẢ SAU |
| S043 | B5 | 266.8 | 5.2 | CIN | IL | Lúc mua, cô đâu có trả đồng nào, vì thế trong đầu cô, những dòng đó chưa từng xảy ra. Cô cộng lại. | Hà chạm điện thoại thanh toán ở quầy, không có gì rời tay. | image | drift_diag {"travel_pct": 5, "scale": 1.06, "dir": "br_to_tl"} | cut |  |
| S044 | B5 | 272.0 | 7.3 | INF | NF | Một triệu chín trăm nghìn, nhiều hơn cả hộp thứ hai, mà trong đầu cô chưa từng là tiền. Mình dừng ở đây một chút, vì chỗ này rất dễ lọt qua. | Hộp thứ ba: thanh dài hơn hộp thứ hai. | image | hold {} | cut | 1.900.000 |
| S045 | B5 | 279.3 | 5.9 | OBJ | IL | Trả sau không làm tiền biến mất, nó chỉ dời cảm giác mất tiền sang một ngày khác. Đến ngày đó, tài khoản vẫn phải trả. | Hai tờ lịch cạnh nhau: ngày mua và ngày phải trả cách nhau cả tháng. | image | pan_right {"travel_pct": 6, "scale": 1.06} | cut |  |
| S046 | B5 | 285.2 | 6.1 | CIN | IL | Đã gần mười một giờ đêm. Cô cộng ba hộp lại được mười một triệu ba trăm năm mươi nghìn, trong khi lương là mười lăm triệu. | Gần mười một giờ đêm, laptop sáng, tách trà nguội bên cạnh. | image | push_in {"from": 1.0, "to": 1.08} | crossfade_6f |  |
| S047 | B5 | 291.4 | 8.2 | INF | NF | Phần còn lại, ba triệu sáu trăm năm mươi nghìn, chưa hộp nào nhận. Gần một phần tư tháng lương đang nằm trong những dòng cô chưa xếp được vào đâu. Những dòng ấy là gì? | Thanh mười lăm phần: ba hộp đã lấp đầy, phần cuối còn trống. | image | focus_push {"from": 1.0, "to": 1.12, "focus": [0.8, 0.5]} | cut | 3.650.000 |
| S048 | B6 | 299.5 | 7.0 | OBJ | IL | Nhưng hộp bốn không chịu im lặng như ba hộp kia. Hà mở từng dòng ra xem, ghi thêm ngày và thứ cô đã mua, rồi dần nhớ được hầu hết. | Hộp thứ tư mở ra, Hà ghi thêm ngày bên cạnh từng dòng. | image | pan_down {"travel_pct": 6, "scale": 1.06} | crossfade_6f |  |
| S049 | B6 | 306.6 | 7.5 | OBJ | IL | Dòng đầu tiên là một chiếc áo khoác, một triệu hai trăm nghìn, mua trước buổi họp mặt đầu tháng. Cô vẫn còn một chiếc áo khoác khác ở nhà, vẫn mặc tốt. | Một chiếc áo khoác mới treo, ở xa là chiếc áo cũ vẫn còn tốt. | image | pan_right {"travel_pct": 6, "scale": 1.06} | cut |  |
| S050 | B6 | 314.1 | 5.5 | CIN | IL | Hôm đó cô chỉ nghĩ rằng mình cần trông ổn một chút. Dòng thứ hai là bữa tối của nhóm bạn, một triệu đồng. | Hà soi gương trong chiếc áo khoác mới, nhìn nghiêng, thoáng ngập ngừng, miệng khép. | image | push_in {"from": 1.0, "to": 1.08} | cut |  |
| S051 | B6 | 319.5 | 8.2 | CIN | IL | Cô trả hết khi mọi người còn đang tính chia, vì thấy chia từng nghìn trước mặt người khác có vẻ keo kiệt. Về nhà, cô mới nhận ra mình đã trả phần của bốn người. | Bàn ăn của nhóm bạn, Hà đưa điện thoại trả cho cả bàn. | image | pan_left {"travel_pct": 6, "scale": 1.06} | cut |  |
| S052 | B6 | 327.7 | 6.6 | OBJ | IL | Dòng thứ ba gộp lại quà sinh nhật và tiền góp quỹ nhóm, một triệu nữa. Chẳng khoản nào lớn, chẳng khoản nào cô hối hận ngay lúc trả. | Hộp quà gói cẩn thận và một phong bì quỹ nhóm trên bàn. | image | drift_diag {"travel_pct": 5, "scale": 1.06, "dir": "tl_to_br"} | cut |  |
| S053 | B6 | 334.3 | 5.2 | INF | NF | Nhưng ba khoản cộng lại là ba triệu hai trăm nghìn, hơn hai lần tiền trà sữa và ăn ngoài của cả tháng. | Ba khối cộng lại cao hơn hai lần khối của hộp thứ hai. | image | hold {} | cut | 3.200.000 |
| S054 | B6 | 339.5 | 4.8 | OBJ | IL | Còn lại bốn trăm năm mươi nghìn là những dòng lẻ mà dù cố đến đâu cô cũng không nhớ nổi. | Vài dòng lẻ mờ nhạt, không dòng nào rõ ràng. | image | drift_diag {"travel_pct": 5, "scale": 1.06, "dir": "br_to_tl"} | cut | 450.000 |
| S055 | B6 | 344.3 | 6.1 | CIN | IL | Mình sẽ không bịa ra lý do cho chúng, vì có những khoản trong sổ chỉ đơn giản là đã quên. Nhưng ba dòng kia thì khác. | Hà nhìn mấy dòng lẻ rồi buông tay, không cố nhớ nữa. | image | push_in {"from": 1.0, "to": 1.08} | cut |  |
| S056 | B6 | 350.5 | 5.0 | OBJ | IL | Hà đã nhớ rất rõ lúc cô trả, nhớ cả lý do trong đầu, mà vẫn không biết gọi chúng là gì. | Ba dòng nổi lên rõ nét giữa các dòng khác, như vừa nhớ ra. | image | focus_push {"from": 1.0, "to": 1.12, "focus": [0.5, 0.5]} | cut |  |
| S057 | B6 | 355.5 | 5.9 | CIN | IL | Chúng không phải ăn uống, không phải đi lại, không phải một món cô thật sự cần. Hà đặt bút xuống và thử một cách khác. | Hà đặt bút xuống, nhìn ba dòng khoanh nhẹ trên trang. | image | pull_out {"from": 1.08, "to": 1.0} | cut |  |
| S058 | B6 | 361.4 | 5.5 | CIN | IL | Cô không hỏi ba dòng ấy là gì, mà hỏi lúc trả cô đang đứng cạnh ai. Câu trả lời làm cô im lặng. | Hà ngồi giữa bàn ăn, hai ba người bạn ở hậu cảnh (áo xanh nhạt, vàng nghệ, thun xám), mờ nhẹ, không nhìn camera; Hà nhìn xuống. | image | push_in {"from": 1.0, "to": 1.08} | cut |  |
| S059 | B6 | 366.8 | 7.5 | OBJ | IL | Áo khoác, bữa tối, món quà: lúc nào cũng có người khác ở đó, hoặc sắp nhìn thấy. Cô lấy bút khoanh tròn ba dòng ấy. Ba dòng ấy đang giữ điều gì? | Bút khoanh tròn ba dòng bằng nét đỏ, cả trang sổ hiện ra; vòng khoanh đỏ là yếu tố đỏ duy nhất của ảnh. | image | pull_out {"from": 1.08, "to": 1.0} | cut |  |
| S060 | B7 | 374.3 | 7.7 | INF | NF | Nhưng khoản không mang tên ấy thật ra có tên, và tên nó là thể diện. Không ai ghi chữ đó vào sổ, nó chỉ nằm lẫn trong áo khoác, bữa tối, quà tặng. | Dòng bỏ trống trong sổ sáng lên, như được viết tên vào. | clip | clip_fit: hold_last | crossfade_6f | THỂ DIỆN |
| S061 | B7 | 382.0 | 7.3 | INF | NF | Ba triệu hai trăm nghìn, hơn hai mươi phần trăm tháng lương, và không dòng nào mang tên nó. Đến đây, câu chuyện của Hà không còn là chuyện hết tiền nữa. | Bảng số sáu dòng trên trang sổ, dòng thứ ba nổi bật nhẹ. | image | hold {} | cut | Cố định 8,1 | Nhỏ lặp lại 1,35 | Thể diện 3,2 | Trả sau 1,9 | Không nhớ 0,45 | Tổng 15,0 (triệu) | VÍ DỤ MINH HỌA |
| S062 | B7 | 389.3 | 8.6 | CIN | IL | Cô không thiếu kỷ luật, vì cô đã ghi, đã cộng, đã chia hộp đến tận khuya. Cô vừa thấy một phần lương của mình đang trả cho cảm giác không muốn kém ai trong mắt người khác. | Hà ngồi lặng trong ánh đèn tối, trang sổ đã đủ dòng. | image | push_in {"from": 1.0, "to": 1.08} | cut |  |
| S063 | B7 | 398.0 | 7.0 | CIN | IL | Nếu nghe đến đây mà bạn thấy quen, điều đó rất con người, và không có gì để xấu hổ. Điều khó nhất là ba dòng ấy không hề vô lý. | Bàn tay Hà đặt nhẹ lên cuốn sổ, ánh đèn ấm. | image | drift_diag {"travel_pct": 5, "scale": 1.06, "dir": "tl_to_br"} | cut |  |
| S064 | B7 | 405.0 | 4.5 | OBJ | IL | Áo khoác giúp cô tự tin hơn trong buổi họp mặt, bữa tối giúp cô giữ chỗ trong nhóm bạn. | Chiếc áo khoác cạnh bàn ăn nhóm bạn, hai thứ cùng một khung. | image | pan_left {"travel_pct": 6, "scale": 1.06} | cut |  |
| S065 | B7 | 409.5 | 7.5 | OBJ | IL | Món quà giúp cô không bị nhớ là người đến tay không, và mỗi dòng đều có một lý do rất hợp lý. Vì thế chúng rất dễ lọt khỏi mọi cuốn sổ. | Món quà gói cẩn thận đang được trao tay. | image | focus_push {"from": 1.0, "to": 1.12, "focus": [0.5, 0.55]} | cut |  |
| S066 | B7 | 417.0 | 5.2 | INF | IL | Trong app ngân hàng, chúng mang tên quán ăn, tên cửa hàng, chưa bao giờ mang tên điều cô thật sự đã mua. | Danh sách sao kê với tên quán ăn và tên cửa hàng, không dòng nào có tên điều đã mua. | image | pan_down {"travel_pct": 6, "scale": 1.06} | cut |  |
| S067 | B7 | 422.3 | 6.6 | CIN | IL | Cô mua đúng thứ cô muốn, chỉ là thứ cô muốn không nằm trên hóa đơn. Cô ngồi yên rất lâu. Lần đầu, cô không thấy tiền biến mất. | Hà ngồi yên, tay đặt trên bàn, sổ đã đủ đầy. | image | push_in {"from": 1.0, "to": 1.08} | cut |  |
| S068 | B7 | 428.9 | 6.8 | INF | NF | Cô thấy tiền đã đến những nơi do chính cô chọn, chỉ là cô không biết mình đang chọn. Biết tên khoản ấy rồi, Hà sẽ làm gì với nó? | Những đường mảnh đi từ cuốn sổ tới các nơi cô đã chọn: quán, cửa hàng, nhà bạn. | image | pull_out {"from": 1.08, "to": 1.0} | cut |  |
| S069 | B8 | 435.7 | 7.0 | CIN | IL | Vì vậy, Hà quyết định không làm gì lớn lao cả. Cô chỉ giữ lại đúng phần đã cho cô thấy sự thật: mười lăm phút, một trang sổ, bốn hộp. | Buổi sáng, Hà gập laptop và mở một cuốn sổ giấy mới. | image | push_in {"from": 1.0, "to": 1.08} | crossfade_6f |  |
| S070 | B8 | 442.7 | 5.9 | INF | IL | Cô gọi đó là bài chốt sổ. Bước một, cô lấy sao kê của tháng trước và chép từng dòng ra một trang, chưa cần hiểu. | Sao kê được chép từng dòng ra một trang giấy. | image | pan_right {"travel_pct": 6, "scale": 1.06} | cut | BƯỚC 1 |
| S071 | B8 | 448.6 | 6.8 | INF | NF | Bước hai, cô xếp mỗi dòng vào một trong bốn hộp. Bước ba, cô cộng từng hộp và đặt cạnh tiền lương. Rồi đến bước bốn, bước Hà nhớ nhất. | Bốn hộp được điền, tổng các hộp đặt cạnh số lương. | image | pan_left {"travel_pct": 6, "scale": 1.06} | cut | BƯỚC 2 · BƯỚC 3 |
| S072 | B8 | 455.5 | 7.5 | INF | NF | Cô khoanh ba khoản lớn nhất trong hộp còn lại. Với mỗi khoản, cô tự hỏi một câu duy nhất: mình mua khoản này cho mình, hay cho cái nhìn của người khác. | Ba khoản lớn nhất trong hộp cuối được khoanh tròn. | image | focus_push {"from": 1.0, "to": 1.12, "focus": [0.75, 0.5]} | cut | BƯỚC 4 |
| S073 | B8 | 463.0 | 8.6 | INF | NF | Câu hỏi ấy nghe đơn giản, nhưng nó làm một việc mà bốn hộp không làm được. Nó đưa những khoản vô danh trở lại thành lựa chọn có tên, và có tên thì mới cân nhắc được. | Ba dòng vô danh được gắn thẻ tên, từ mờ thành rõ. | image | pull_out {"from": 1.08, "to": 1.0} | cut |  |
| S074 | B8 | 471.6 | 5.7 | OBJ | IL | Cả bài làm hết mười lăm phút, không cần bảng tính, không cần ứng dụng. Chỉ cần sao kê tháng trước và một cây bút. | Sao kê in, một cây bút và một chiếc đồng hồ để bàn chỉ mười lăm phút. | image | drift_diag {"travel_pct": 5, "scale": 1.06, "dir": "br_to_tl"} | cut | 15 PHÚT |
| S075 | B8 | 477.3 | 6.8 | OBJ | IL | Mình để bốn bước này lại cho bạn thử trên sổ của chính bạn, vào lúc nào bạn rảnh. Tháng sau, Hà làm lại bài chốt sổ y như vậy. | Cuốn sổ đặt trên bàn, hướng về phía người xem, bút nằm cạnh. | image | push_in {"from": 1.0, "to": 1.08} | cut |  |
| S076 | B8 | 484.1 | 8.2 | INF | NF | Hộp bốn nhỏ đi, nhưng không phải vì cô tự cấm mình. Có dòng cô hỏi xong không còn muốn mua, và có dòng cô hỏi xong vẫn mua, lần này với cái đầu rõ ràng. | Hộp thứ tư co nhỏ lại, ba dòng trong đó đã có thẻ tên. | clip | clip_fit: hold_last | crossfade_6f |  |
| S077 | B8 | 492.3 | 7.3 | CIN | IL | Hà vẫn đi ăn với nhóm bạn, vẫn trả phần của mình. Chỉ khác là dòng đó bây giờ có tên, và cô biết chính xác mình đang trả cho điều gì. | Hà ngồi ăn với nhóm bạn, trả phần của mình, ánh đèn ấm. | image | pan_right {"travel_pct": 6, "scale": 1.06} | cut |  |
| S078 | B8 | 499.5 | 5.5 | CIN | IL | Cô thấy mình đỡ phải giải thích với chính mình. Vậy sau một tháng chốt sổ, Hà thật sự đã thay đổi điều gì? | Hà khép sổ, vai thả lỏng, căn phòng mở rộng dần. | image | pull_out {"from": 1.08, "to": 1.0} | cut |  |
| S079 | B9 | 505.0 | 7.0 | CIN | IL | Một tháng sau, Hà không giàu lên. Điều đổi khác nhỏ hơn thế: khi người bạn hỏi lại, cô trả lời được bằng con số, và con số ấy có tên. | Một tháng sau, Hà đưa cuốn sổ nhỏ cho người bạn xem. | image | push_in {"from": 1.0, "to": 1.08} | crossfade_6f |  |
| S080 | B9 | 512.0 | 4.8 | INF | NF | Ba triệu hai trăm nghìn của tháng đầu giờ đã có tên cho từng dòng. Tiền không bao giờ biến mất. | Ba dòng, mỗi dòng một thẻ tên rõ ràng. | image | hold {} | cut | 3.200.000 |
| S081 | B9 | 516.8 | 7.5 | OBJ | NF | Nó đi đến những chỗ mình chưa gọi tên, và chỗ nào chưa có tên thì chưa phải lựa chọn của mình. Việc của người chốt sổ chỉ là gọi tên từng khoản. | Những vệt sáng mảnh chảy tới các chỗ đã có tên. | image | drift_diag {"travel_pct": 5, "scale": 1.06, "dir": "tl_to_br"} | cut |  |
| S082 | B9 | 524.3 | 3.2 | INF | NF | Việc đầu tiên rất nhỏ. Mười lăm phút, sao kê tháng trước, bốn hộp. | Ba biểu tượng nhỏ xếp hàng: đồng hồ, sao kê, bốn hộp. | image | hold {} | cut | 15 PHÚT · SAO KÊ · 4 HỘP |
| S083 | B9 | 527.5 | 5.7 | INF | IL | Rồi khoanh ba khoản lớn nhất ở hộp cuối, và hỏi chính mình xem mình mua cho mình hay cho cái nhìn của người khác. | Ba khoản lớn nhất ở hộp cuối được khoanh, bàn tay cầm bút. | image | focus_push {"from": 1.0, "to": 1.12, "focus": [0.5, 0.6]} | cut | CHO MÌNH hay CHO CÁI NHÌN CỦA NGƯỜI KHÁC? |
| S084 | B9 | 533.2 | 5.7 | TTL | IL | Trong hộp cuối của bạn, khoản nào bạn đoán là mua cho cái nhìn của người khác nhiều nhất? Chốt sổ hôm nay ở đây. | Cuốn sổ đóng trên bàn gỗ sáng, nền tối giản. | image | hold {} | cut | CHỐT SỔ CUỐI NGÀY |


---

```
=== LOCK RECORD: L5 v3 VISUAL LANGUAGE VÀ KEY ASSETS (ĐÃ KHÓA, thay thế v2) ===

LAYER: L5 (v3)

DECISIONS
- Hai chế độ hình: (1) ILLUSTRATION cho cảnh đời thường (CIN/OBJ/TTL); (2) NOTEBOOK-FLAT cho cảnh sơ đồ (INF): ô li phẳng, navy, một yếu tố đỏ.
- STYLE BIBLE ILLUSTRATION (54 từ, dán nguyên văn đầu prompt):
  "Clean 2D editorial illustration, manhwa-inspired: thin dark-navy outlines, flat cel shading with soft subtle shadows, warm natural palette of cream, soft blue and sand with ink navy #0F2A5C and graphite accents, one small red #D7263D accent per image, realistic Vietnamese everyday settings, calm expressive faces with closed mouths, one focal subject, generous negative space."
- STYLE BIBLE NOTEBOOK-FLAT (46 từ, cho cảnh NF; bỏ cụm "faceless geometric characters" khi cảnh không có nhân vật):
  "Flat vector design on light grid paper #EEF3F9 with thin blue ruled lines, bold geometric shapes, ink navy #0F2A5C and graphite #2B2F36 forms, single red #D7263D rubber-stamp accent with slight ink texture, hard offset shadow, crisp edges, faceless geometric characters, one focal subject, generous negative space."
- Ảnh và clip không chữ/số/logo; mọi chữ trên màn hình do Remotion vẽ.
- Danh tính Hà gồm 3 dấu hiệu bắt buộc: búi thấp có vài sợi mai; cardigan navy #0F2A5C trên blouse kem; mặt trái xoan bình thản. Quần: be hoặc xám than (không màu khác).
- Lý do đổi từ v2: hình khối không mặt bị đánh giá thô và xấu; tham khảo hướng minh họa có mặt, bối cảnh Việt đời thường của nhóm Minh Kể Tài Chính. Chỉ học định hướng, không copy nhân vật hay bố cục thumbnail.

KEY ASSETS (file chuẩn trong folder keyassets/, dùng làm Reference)
- KA01_HA.jpg: 3 toàn thân + 4 cận mặt (calm, tired, thoughtful).
- KA02_ACCOUNTANT.jpg: nữ ~42 tuổi, kính tròn, tóc xoăn nhẹ, blazer graphite; 3 toàn thân + 1 cận.
- KA03_NOTEBOOK.jpg: sổ mở, bút, cốc cà phê, chậu cây.
- KA04_PROPS.jpg: 7 vật (điện thoại, laptop, ly trà sữa, hộp cơm, áo khoác, hộp quà, lịch để bàn).
- KA05_FOURBOX_BAR.jpg: khuôn INF: 4 hộp ngang (hộp 4 viền đỏ nét đứt) + thanh 15 đoạn (8 đặc).
- KA06_ROOM_NIGHT.jpg: phòng thuê đêm (cửa sổ trăng, quạt trần, bàn laptop, giá áo, tường gạch).
- Bạn bè: tối đa 3 người, mỗi người một nét (áo xanh nhạt, vàng nghệ, thun xám), ở trung hoặc hậu cảnh.

COMPOSITION
- Tiêu điểm 1/3 trái (ngoại lệ INF theo tọa độ focus của SCENE PLAN: S030 0,75; S047 0,8; S072 0,75). Trống ≥25% (IL), ≥35% (NF).
- Vùng caption: 20% đáy khung không có đối tượng quan trọng, nhưng nền vẫn chạy hết mép khung.
- Tiền cảnh: vật cắt góc ≤25% khung, không che tiêu điểm.
- Cảnh NF: hàng hộp ở 38-45% chiều cao, thanh ở ≤62%, chừa 25% trên và 20% dưới.
- Cảnh IL: ≥5 vật dụng đời thường trong khung.
- Ảnh nguồn của clip: nội dung chính trong 84% ngang × 72% dọc.

SHOT VOCABULARY: CIN toàn / trung / qua vai / cận tay hoặc mặt (miệng khép); OBJ cận hoặc nhìn từ trên xuống, ≤4 vật; INF chính diện phẳng, ≤6 phần tử; TTL sổ 

IMAGE PROMPT ANATOMY (điền chỗ trống)
[STYLE BIBLE tương ứng theo Mode]. Shot: [cỡ + góc]. Subject: [đếm chính xác + "Total: N, no more." + vị trí x/y + biểu cảm]. Setting: foreground [..]; midground [..]; background [≥5 đồ vật]. Light: [..]. 16:9. Caption-safe: no important subject in the bottom 20%, background continues to the edge. Reference: [KA##]. Avoid: [..]. File name: [S###].
Avoid mặc định: text, letters, numbers, logo, watermark, open mouth, shocked face, pointing at camera, extra people, photorealism, 3D render, cash, coins, banknotes, upward arrows, white border, blank strip.

RULES
1. Cảnh có Hà đính Reference KA01_HA (cùng phòng thì thêm KA06); có chị kế toán đính KA02_ACCOUNTANT.
2. Biểu cảm chỉ: calm, tired, thoughtful, relieved, quietly surprised; miệng luôn khép.
3. Một yếu tố đỏ mỗi ảnh (≤10% khung); ảnh không có đỏ ghi "No red element".
4. INF dùng khuôn KA05; số đoạn tô = số tiền ÷ 15.
5. Số lượng nhỏ phải có câu khóa "Total: N, no more.".
6. Không đếm dòng kẻ trên giấy trong prompt.
7. Không dùng ảnh đối thủ làm Reference trong Flow.
8. Dấu sao Gemini ở góc dưới phải do creator xóa ở hậu kỳ bằng tool remove watermark; ảnh gốc giữ ở folder raw/.

BANS
- "Keep the bottom N% empty" (lý do: sinh dải trắng ở đáy ảnh; lỗi KA01, KA02).
- Miệng há, mắt trợn, chỉ tay vào camera (lý do: clickbait, tạo xấu hổ).
- Số lượng nhỏ mà không có câu khóa tổng (lý do: KA01 ra 4 thay vì 3).
- Cash, xu, xấp tiền, mũi tên đi lên (lý do: vùng cấm).
- Chữ giả trên điện thoại, biển, sổ (lý do: lỗi hay gặp; xác nhận ở L6).

FAILURE-FIX TABLE
| Triệu chứng | Nguyên nhân | Sửa prompt |
| Dải trắng ở đáy | "bottom 12% empty" | Dùng caption-safe; thêm "background fills the whole frame to the edges" |
| Thừa phần tử (4 thay 3) | Thiếu câu khóa tổng | Thêm "Total: N, no more." |
| Ghế/vật tiền cảnh quá lớn | "under 12%" không được tuân thủ | Chỉ định "small, partly visible at the very corner" |
| Hà lệch trang phục | Không đính Reference | Đính KA01_HA; nhắc 3 dấu hiệu danh tính |
| Thanh INF lấn vùng caption | Đặt thanh ở 68% | Hàng hộp 40%, thanh 60% |

PARAMETERS
- 16:9; đỏ ≤10% khung; trống ≥25% (IL) / ≥35% (NF); vùng caption 20% đáy; tiền cảnh ≤25%.

GOLDEN SAMPLE: KA01-KA06 trong keyassets/. Câu mô tả mẫu cho cảnh CIN: "Hà ngồi mép giường, ba phần tư sau lưng, mắt nhìn xuống điện thoại, miệng khép, ánh điện thoại hắt lên má".

CHECKS
1. Hà có đủ 3 dấu hiệu danh tính.
2. Không chữ/số/logo; miệng khép; không chỉ vào camera.
3. ≤1 yếu tố đỏ, ≤10% khung.
4. Đếm đúng theo "Total: N".
5. Không dải trắng; nền chạy hết mép; đáy 20% không có tiêu điểm.
6. ≥5 vật dụng đời thường (cảnh IL).
7. Cảnh NF: hàng hộp ≤45%, thanh ≤62%, không yếu tố lạ.
8. Ảnh đã xử lý: góc dưới phải không còn dấu sao hay vết bù.

OPEN RISKS
- Veo có thể làm miệng nhép khi animate mặt; L7 thêm "mouth stays closed, no lip movement".
- Clip Veo có thể có watermark riêng [VERIFY ở L7]; quy trình đề xuất: xóa dấu ảnh trước, dùng ảnh sạch làm khung đầu.
- Hà dễ lệch ở cảnh xa; khi lệch, tăng cỡ nhân vật hoặc đính lại KA01.
- Phong cách gần đối thủ; khác biệt nằm ở trang sổ NF
- Quần của Hà cho phép hai màu; nếu khó nhận, khóa một màu ở L6.
- Chữ giả trên màn hình điện thoại hoặc sổ chưa được thử; kiểm ở batch 1 của L6.

NEXT: L6 batch 1 = S001-S006 (cảnh hook, nguồn của 5 clip).
```

````
=== L6 LOG: BATCH 1 ===

```
FLOW RULES: Generate exactly what each prompt says and nothing else. Never add speech, dialogue, voiceover or lip-sync to any video. Sound effects are allowed only where the prompt names them. On-screen text is allowed only if the prompt gives the exact text and language; otherwise the image has no text, no logo, no watermark. Never add, remove or change any subject, count, color or setting the prompt specifies. If you cannot comply, report it; do not improvise. After generating, rename every asset to its scene ID: images as S014, clips as S014_anim. Reply with a table: scene | asset name | status.

PROMPT S001
Clean 2D editorial illustration, manhwa-inspired: thin dark-navy outlines, flat cel shading with soft subtle shadows, warm natural palette of cream, soft blue and sand with ink navy #0F2A5C and graphite accents, one small red #D7263D accent per image, realistic Vietnamese everyday settings, calm expressive faces with closed mouths, one focal subject, generous negative space. Shot: close-up, top-down view of a desk, 16:9. Subject: Total: 2 hero objects, no more: one open ruled notebook placed at the left third of the frame (x about 0.33, y about 0.42), and one thin ballpoint pen lying beside it. On the notebook's right page, the first row has one plain short pen stroke, and the last visible row has one large hand-drawn red #D7263D ring, an empty circle with nothing inside it, about 9% of the frame width. Setting: foreground a small part of a navy folder, partly visible at the very bottom-left corner; midground the notebook and pen; background a light wooden desk with a blue-and-white ceramic coffee cup, a small potted plant, a smartphone lying face down, and the base of a desk lamp at the top-right edge. Light: soft warm daylight, soft shadows. 16:9. Caption-safe: no important subject in the bottom 20% of the frame; the background continues to the edge of the frame. Reference: KA03_NOTEBOOK. Avoid: text, letters, numbers, digits, handwriting, logo, watermark, people, photorealism, 3D render, cash, coins, banknotes, upward arrows, white border, blank strip. File name: S001

PROMPT S002
Clean 2D editorial illustration, manhwa-inspired: thin dark-navy outlines, flat cel shading with soft subtle shadows, warm natural palette of cream, soft blue and sand with ink navy #0F2A5C and graphite accents, one small red #D7263D accent per image, realistic Vietnamese everyday settings, calm expressive faces with closed mouths, one focal subject, generous negative space. Shot: medium-wide eye-level shot of a small rented room at night, same room layout as reference KA06_ROOM_NIGHT, 16:9. Subject: Total: 1 person, no more: Hà, the character from reference KA01_HA (low bun with a few loose strands, cream blouse, ink-navy cardigan), seated on the edge of a single bed at the left third of the frame (x about 0.33), three-quarter back view with her calm face partly visible in profile, mouth closed, looking down at a smartphone with a red #D7263D phone case; a soft warm-white glow from the phone falls on her cheek and hands. Setting: foreground the edge of a wooden chair, small and partly visible at the very bottom-left corner; midground the bed with a patterned blanket and Hà; background a tiled wall, a window with a dark night sky and a pale crescent moon, a ceiling fan, a small desk with a closed laptop and a cup, a clothes rack with two garments. Light: dim blue night room lit by the phone glow and one small warm lamp. 16:9. Caption-safe: no important subject in the bottom 20% of the frame; the background continues to the edge of the frame. Reference: KA01_HA, KA06_ROOM_NIGHT. Avoid: text, letters, numbers, logo, watermark, open mouth, shocked face, pointing at camera, extra people, photorealism, 3D render, cash, coins, white border, blank strip. File name: S002

PROMPT S003
Clean 2D editorial illustration, manhwa-inspired: thin dark-navy outlines, flat cel shading with soft subtle shadows, warm natural palette of cream, soft blue and sand with ink navy #0F2A5C and graphite accents, one small red #D7263D accent per image, realistic Vietnamese everyday settings, calm expressive faces with closed mouths, one focal subject, generous negative space. Shot: close-up, top-down view of a desk, 16:9. Subject: Total: 3 hero objects, no more: one open hardcover ruled notebook with a navy cover, NO spiral rings, at the left third of the frame (x about 0.33, y about 0.42); one hand wearing an ink-navy cardigan cuff holding one thin ballpoint pen that hovers just above the page, not touching it. The notebook's right page has five rows, each holding a short plain horizontal bar (abstract bars, not letters), and one empty row in the middle surrounded by one red #D7263D dashed rectangle outline, the only red element in the image. Setting: foreground a small part of a navy folder, partly visible at the very bottom-left corner; midground the notebook, hand and pen; background a light wooden desk with a ceramic coffee cup, a small potted plant, a smartphone lying face down, and a stack of two books at the top-right edge. Light: soft warm daylight, soft shadows. 16:9. Full-bleed artwork: the illustration fills the entire canvas edge to edge on all four sides. Caption-safe: no important subject in the bottom 20% of the frame; the background continues to the edge of the frame. Reference: KA03_v2, KA01_HA. Avoid: stamp, seal, text, letters, numbers, digits, handwriting, logo, watermark, face, extra people, spiral rings, photorealism, 3D render, cash, coins, banknotes, white border, blank strip, footer band. File name: S003

PROMPT S004
Clean 2D editorial illustration, manhwa-inspired: thin dark-navy outlines, flat cel shading with soft subtle shadows, warm natural palette of cream, soft blue and sand with ink navy #0F2A5C and graphite accents, one small red #D7263D accent per image, realistic Vietnamese everyday settings, calm expressive faces with closed mouths, one focal subject, generous negative space. Shot: medium close-up, top-down view of a desk, 16:9. Subject: Total: 2 hero objects, no more: one hardcover notebook with a navy cover, NO spiral rings, its cover half lowered as it is being closed, at the left third of the frame (x about 0.33, y about 0.42); one hand wearing an ink-navy cardigan cuff resting on the notebook's edge. No red element in this image. Setting: foreground a small part of a navy folder, partly visible at the very bottom-left corner; midground the notebook and hand; background a light wooden desk with a ceramic coffee cup, a small potted plant at the top-right edge, a smartphone lying face down, and a desk lamp base. Light: soft warm daylight, soft shadows. 16:9. Full-bleed artwork: the illustration fills the entire canvas edge to edge on all four sides. Caption-safe: no important subject in the bottom 20% of the frame; the background continues to the edge of the frame. Reference: KA03_v2. Avoid: stamp, seal, check mark, red objects, text, letters, numbers, digits, handwriting, logo, watermark, face, extra people, spiral rings, photorealism, 3D render, cash, coins, banknotes, white border, blank strip, footer band. File name: S004

PROMPT S005
Clean 2D editorial illustration, manhwa-inspired: thin dark-navy outlines, flat cel shading with soft subtle shadows, warm natural palette of cream, soft blue and sand with ink navy #0F2A5C and graphite accents, one small red #D7263D accent per image, realistic Vietnamese everyday settings, calm expressive faces with closed mouths, one focal subject, generous negative space. Shot: close-up, slightly raised eye-level view of a desk, 16:9. Subject: Total: 3 hero objects, no more: one desk calendar at the left third of the frame (x about 0.33, y about 0.42), standing with a spiral top and a grid of empty cells (no numbers), with three already-flipped pages visible as curled sheets at its top; one open ruled notebook to the right of the calendar, its pages still empty; one thin ballpoint pen lying on the notebook. No red element in this image. Setting: foreground a small part of a navy folder, partly visible at the very bottom-left corner; midground calendar and notebook; background a light wooden desk with a ceramic coffee cup, a small potted plant, a smartphone lying face down, a desk lamp, and a window with soft daylight. Light: soft warm daylight, soft shadows. 16:9. Caption-safe: no important subject in the bottom 20% of the frame; the background continues to the edge of the frame. Reference: KA04_PROPS, KA03_NOTEBOOK. Avoid: text, letters, numbers, digits, handwriting, logo, watermark, people, photorealism, 3D render, cash, coins, banknotes, white border, blank strip. File name: S005

PROMPT S006
Clean 2D editorial illustration, manhwa-inspired: thin dark-navy outlines, flat cel shading with soft subtle shadows, warm natural palette of cream, soft blue and sand with ink navy #0F2A5C and graphite accents, one small red #D7263D accent per image, realistic Vietnamese everyday settings, calm expressive faces with closed mouths, one focal subject, generous negative space. Shot: close-up, top-down view of a desk calendar page, 16:9. Subject: Total: 3 hero objects, no more: one calendar page with an empty grid of cells (5 columns by 6 rows, no numbers), one thin ballpoint pen resting on the page edge outside the grid, and one hand-drawn red #D7263D ring around exactly one cell, an empty circle with nothing inside, about 8% of the frame width, centered in the frame at x 50%, y 45%. The red ring is the only red element. Setting: foreground a small part of a navy folder, partly visible at the very bottom-left corner; midground the calendar page and pen; background a light wooden desk with a ceramic coffee cup, a small potted plant, and a smartphone lying face down at the top edges. Light: soft warm daylight, soft shadows. 16:9. Caption-safe: no important subject in the bottom 20% of the frame; the background continues to the edge of the frame. Reference: KA04_PROPS, KA03_NOTEBOOK. Avoid: text, letters, numbers, digits, handwriting, logo, watermark, people, photorealism, 3D render, cash, coins, banknotes, white border, blank strip. File name: S006
```

RULES mới
9. Mọi prompt có câu "Full-bleed artwork: the illustration fills the entire canvas edge to edge on all four sides." đặt ngay trước "Caption-safe".
10. Sổ luôn là "hardcover notebook with a navy cover, NO spiral rings" (khớp KA03).
11. Không chỉ định số ô của lịch hay lưới (model đổi theo ý nó); chỉ nói "a grid of empty cells".

BANS mới
- Tọa độ tâm đơn lẻ cho vật cần nằm trong vùng giới hạn (lý do: S004 lệch ~14% theo chiều dọc).
- Sổ lò xo (lý do: lệch KA03, S004).

FAILURE-FIX TABLE (bổ sung)
| Dải trắng vẫn xuất hiện dù có "Avoid: blank strip" | Lỗi hệ thống của model ở vài ảnh | Thêm câu "Full-bleed"; nếu vẫn lỗi, cắt 7,5% đáy trong hậu kỳ rồi scale lên 16:9 |
| Vật phụ lấn vùng caption (S005) | Vật phụ đặt thấp | Chấp nhận nếu không phải tiêu điểm |
OPEN RISKS: tỉ lệ dải trắng ~1/3 số ảnh; nếu batch 2 còn lỗi thì chuyển sang quy trình "cắt đáy + scale" cho toàn bộ ảnh.

````

```
HAND-OFF CARD B: BATCH 2 (S007-S012)

FLOW RULES: Generate exactly what each prompt says and nothing else. Never add speech, dialogue, voiceover or lip-sync to any video. Sound effects are allowed only where the prompt names them. On-screen text is allowed only if the prompt gives the exact text and language; otherwise the image has no text, no logo, no watermark. Never add, remove or change any subject, count, color or setting the prompt specifies. If you cannot comply, report it; do not improvise. After generating, rename every asset to its scene ID: images as S014, clips as S014_anim. Reply with a table: scene | asset name | status.

PROMPT S007
Clean 2D editorial illustration, manhwa-inspired: thin dark-navy outlines, flat cel shading with soft subtle shadows, warm natural palette of cream, soft blue and sand with ink navy #0F2A5C and graphite accents, one small red #D7263D accent per image, realistic Vietnamese everyday settings, calm expressive faces with closed mouths, one focal subject, generous negative space. Shot: medium close-up, eye-level, seen from Hà's side, 16:9. Subject: Total: 1 person, no more: Hà, the character from reference KA01_HA (low bun with a few loose strands, cream blouse, ink-navy cardigan), seated on the edge of a single bed at the left third of the frame (x about 0.33), side profile facing right, both hands holding a smartphone with a red #D7263D phone case, calm tired face, mouth closed; a soft warm-white glow from the screen lights her face and hands. The phone case is the only red element. Setting: foreground the edge of a patterned blanket, small, at the very bottom-left corner; midground Hà and the bed; background a tiled wall, a window with a dark night sky and a pale crescent moon, a ceiling fan blade at the top, a small desk with a closed laptop and a cup, a clothes rack with two garments. Light: dim blue night room lit by the phone glow and one small warm lamp. 16:9. Full-bleed artwork: the illustration fills the entire canvas edge to edge on all four sides. Caption-safe: no important subject in the bottom 20% of the frame; the background continues to the edge of the frame. Reference: KA01_HA, KA06_ROOM_NIGHT. Avoid: text, letters, numbers, logo, watermark, open mouth, shocked face, pointing at camera, extra people, photorealism, 3D render, cash, coins, white border, blank strip, footer band. File name: S007

PROMPT S008
Clean 2D editorial illustration, manhwa-inspired: thin dark-navy outlines, flat cel shading with soft subtle shadows, warm natural palette of cream, soft blue and sand with ink navy #0F2A5C and graphite accents, one small red #D7263D accent per image, realistic Vietnamese everyday settings, calm expressive faces with closed mouths, one focal subject, generous negative space. Shot: close-up, straight-on view of a wall calendar, 16:9. Subject: Total: 2 hero objects, no more: one wall calendar page with a blue header strip and a grid of empty cells (no numbers), placed at the left third of the frame (x about 0.33, y about 0.42); one hand-drawn red #D7263D ring around the very first cell of the top row only, an empty circle with nothing inside. The bottom row of cells has a pale soft-blue wash. The red ring is the only red element. Setting: foreground one green plant leaf at the bottom-left corner, small; midground the calendar; background a tiled wall, a small shelf with a ceramic cup, a hanging key, and soft window light from the right. Light: soft warm daylight, soft shadows. 16:9. Full-bleed artwork: the illustration fills the entire canvas edge to edge on all four sides. Caption-safe: no important subject in the bottom 20% of the frame; the background continues to the edge of the frame. Reference: KA04_PROPS. Avoid: text, letters, numbers, digits, handwriting, logo, watermark, people, photorealism, 3D render, cash, coins, banknotes, white border, blank strip, footer band. File name: S008

PROMPT S009
Clean 2D editorial illustration, manhwa-inspired: thin dark-navy outlines, flat cel shading with soft subtle shadows, warm natural palette of cream, soft blue and sand with ink navy #0F2A5C and graphite accents, one small red #D7263D accent per image, realistic Vietnamese everyday settings, calm expressive faces with closed mouths, one focal subject, generous negative space. Shot: medium shot, eye-level from behind, 16:9. Subject: Total: 3 people, no more: Hà, the character from reference KA01_HA, seated at an office desk at the left third of the frame (x about 0.33), three-quarter back view, working calmly; two colleagues, small and softly simplified, in the far background. Setting: foreground the corner of a neat paper stack, small, at the bottom-left corner; midground Hà at a wooden office desk with a monitor showing abstract light bars, a tidy pile of papers, a pen holder and a small plant; background an open-plan office with two more desks, a tall window with city daylight, a wall clock without numbers, a filing cabinet, a water dispenser.  Light: bright soft daylight. 16:9. Full-bleed artwork: the illustration fills the entire canvas edge to edge on all four sides. Caption-safe: no important subject in the bottom 20% of the frame; the background continues to the edge of the frame. Reference: KA01_HA. Avoid: text, letters, numbers, digits, logo, watermark, open mouth, shocked face, pointing at camera, extra people, photorealism, 3D render, cash, coins, white border, blank strip, footer band. File name: S009

PROMPT S010
Clean 2D editorial illustration, manhwa-inspired: thin dark-navy outlines, flat cel shading with soft subtle shadows, warm natural palette of cream, soft blue and sand with ink navy #0F2A5C and graphite accents, one small red #D7263D accent per image, realistic Vietnamese everyday settings, calm expressive faces with closed mouths, one focal subject, generous negative space. Shot: medium-wide eye-level shot, 16:9. Subject: Total: 2 people, no more: Hà, the character from reference KA01_HA, at the left third of the frame (x about 0.33), side view, seated at a small round table on a balcony, calm; opposite her a friend with short black hair in a light blue shirt, seated, relaxed, mouth closed; two glasses of iced coffee on the table. Setting: foreground a leafy plant branch at the bottom-left corner, small; midground the table, two chairs and the two people; background a balcony railing with a few hanging clothes, potted plants, a small bicycle, tiled rooftops and a hazy city sky.  Light: soft warm afternoon daylight. 16:9. Full-bleed artwork: the illustration fills the entire canvas edge to edge on all four sides. Caption-safe: no important subject in the bottom 20% of the frame; the background continues to the edge of the frame. Reference: KA01_HA. Avoid: text, letters, numbers, digits, logo, watermark, open mouth, shocked face, pointing at camera, extra people, photorealism, 3D render, cash, coins, white border, blank strip, footer band. File name: S010

PROMPT S011
Clean 2D editorial illustration, manhwa-inspired: thin dark-navy outlines, flat cel shading with soft subtle shadows, warm natural palette of cream, soft blue and sand with ink navy #0F2A5C and graphite accents, one small red #D7263D accent per image, realistic Vietnamese everyday settings, calm expressive faces with closed mouths, one focal subject, generous negative space. Shot: close-up, top-down view of a desk, 16:9. Subject: Total: 3 hero objects, no more: one bubble-tea cup with a straw, one takeaway lunch box, one small kraft paper delivery bag, arranged in a loose row occupying the left half of the frame (center about x 0.33, y about 0.42).  Setting: foreground a small part of a navy folder at the bottom-left corner; midground the three objects; background a light wooden desk with a smartphone lying face down, a small potted plant, a ceramic cup and a pair of keys at the top-right edge. Light: soft warm daylight, soft shadows. 16:9. Full-bleed artwork: the illustration fills the entire canvas edge to edge on all four sides. Caption-safe: no important subject in the bottom 20% of the frame; the background continues to the edge of the frame. Reference: KA04_PROPS. Avoid: text, letters, numbers, digits, logo, watermark, brand marks, people, photorealism, 3D render, cash, coins, banknotes, white border, blank strip, footer band. File name: S011

PROMPT S012
Clean 2D editorial illustration, manhwa-inspired: thin dark-navy outlines, flat cel shading with soft subtle shadows, warm natural palette of cream, soft blue and sand with ink navy #0F2A5C and graphite accents, one small red #D7263D accent per image, realistic Vietnamese everyday settings, calm expressive faces with closed mouths, one focal subject, generous negative space. Shot: close-up, slightly raised view of a nearly bare desk at night, 16:9. Subject: Total: 1 hero object, no more: one thin, flat, empty brown wallet lying half-open on the desk at the left third of the frame (x about 0.33, y about 0.42), visibly empty, no cash and no cards inside.  Setting: foreground a small part of a navy folder at the bottom-left corner; midground the wallet; background an almost empty light wooden desk with a closed laptop, one cup, and a desk lamp casting cold bluish light, a dark window with a pale crescent moon at the top-right. Light: cold blue-white lamp light, soft shadows. 16:9. Full-bleed artwork: the illustration fills the entire canvas edge to edge on all four sides. Caption-safe: no important subject in the bottom 20% of the frame; the background continues to the edge of the frame. Reference: KA04_PROPS. Avoid: text, letters, numbers, digits, logo, watermark, people, photorealism, 3D render, coins, banknotes, cash, white border, blank strip, footer band. File name: S012
```