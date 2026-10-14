# LOCK RECORD: L5 — TÀI SẢN NÒNG CỐT & CẤU TRÚC PROMPT (KEY ASSETS)

- Video: V01 — Lương 15 Triệu Cuối Tháng Còn 0: Tiền Của Bạn Đã Đi Đâu?
- Ngày khóa: 2026-10-14
- Trạng thái: LOCKED

## 1. NGUYÊN TẮC THẨM MỸ BẤT BIẾN (TASTE CAPTURE)
- RULE: 100% tài sản trong video (từ S001 đến S024) phải sử dụng thuần phong cách Minimalist Editorial Flat Illustration, đồng nhất bảng màu Navy `#0F2A5C`, Ice-Blue `#EEF3F9` và Terracotta `#D7263D`.
- BAN: Cấm chèn footage hoặc clip người thật điện ảnh (cinematic/photorealistic) vào video để không làm gãy nhận diện thương hiệu.

## 2. DANH MỤC TÀI SẢN TÁI SỬ DỤNG TỪ BỘ MẪU
1. `KA04_recurring_props.png` -> Dùng cho `S009` và `S015` (Sổ tay, đồng hồ cát, ly gốm)
2. `KA07_test_desk_medium.png` -> Dùng cho `S007` (Minh ngồi bàn làm việc nhìn màn hình)
3. `KA08_test_card_close.png` -> Dùng cho `S013` (Thao tác thẻ ngân hàng có ổ khóa)
4. `KA09_diagram_iceberg.png` -> Dùng cho `S019` (Sơ đồ tảng băng chìm nợ hình ảnh)
5. `KA10_thumbnail_canvas.png` -> Dùng cho `S024` (Nhân vật nữ trí thức thanh thản) và ảnh bìa Thumbnail

## 3. DANH MỤC 19 TÀI SẢN CẦN TẠO MỚI (CHIA THÀNH 3 BATCH CHO FLOW)
- **Batch 1 (S001 – S006):**
  + `S001.png`: Minh ngồi bên cửa sổ sương sớm nhìn thành phố.
  + `S002_anim.mp4`: Minh làm việc tại văn phòng tối giản (vector animation).
  + `S003.png`: Điện thoại hiển thị số dư 0đ bên tách cà phê.
  + `S004_anim.mp4`: Bóng người bước đi cô đơn trên vỉa hè lúc chạng vạng.
  + `S005.png`: Logo Tiền Có Lý Do & tảng băng chìm tối giản.
  + `S006.png`: Bảng đồ họa 4 khoản chi phí cố định (Nhà, Ăn, Dịch vụ, Xe).
- **Batch 2 (S008 – S014):**
  + `S008.png`: Sơ đồ não bộ đan xen dòng tiền đứt gãy.
  + `S010.png`: Đồ họa 3 biểu tượng icon đánh số 1, 2, 3 nổi bật.
  + `S011.png`: Bàn làm việc đêm với ly trà sữa và gói hàng online bóc dở.
  + `S012.png`: Minh tựa lưng sofa thở dài mệt mỏi sau ngày làm việc.
  + `S014.png`: Đồ họa cộng dồn 3 khoản chi nhỏ < 50k.
- **Batch 3 (S016 – S023):**
  + `S016.png`: Biểu đồ tăng trưởng lãi kép từ 3M/tháng lên 550 triệu sau 10 năm.
  + `S017.png`: Minh đứng bên cửa sổ lớn nhìn bình minh rộng thoáng.
  + `S018.png`: Điện thoại rung chuông hiển thị "Mẹ ở quê" bên hóa đơn sửa xe.
  + `S020.png`: Đồ họa thanh pin ý chí cạn kiệt (màu đỏ báo động).
  + `S021.png`: Nền Navy đậm với chữ triết lý "Hệ thống thắng ý chí".
  + `S022.png`: Đồ họa 3 chiếc hộp/hũ tài khoản ngân hàng phân bổ.
  + `S023.png`: Sơ đồ động 3 bước tự động hóa dòng tiền.

## 4. KHỐI LỆNH BẮT BUỘC FLOW RULES
```text
FLOW RULES: Generate exactly what each prompt says and nothing else. Never add speech, dialogue, voiceover or lip-sync to any video. Sound effects are allowed only where the prompt names them. On-screen text is allowed only if the prompt gives the exact text and language; otherwise the image has no text, no logo, no watermark. Never add, remove or change any subject, count, color or setting the prompt specifies. If you cannot comply, report it; do not improvise. After generating, rename every asset to its scene ID: images as S014, clips as S014_anim. Reply with a table: scene | asset name | status.
```
