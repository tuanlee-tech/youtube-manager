# LOCK RECORD: L8 — ÂM THANH, PHỤ ĐỀ, NHẠC NỀN & HÒA ÂM

- Video: V01 — Lương 15 Triệu Cuối Tháng Còn 0: Tiền Của Bạn Đã Đi Đâu?
- Ngày khóa: 2026-10-14
- Trạng thái: LOCKED

---

## 1. THÔNG SỐ KỸ THUẬT ÂM THANH (AUDIO PARAMETERS)

```text
RESOLUTION: 1920x1080
FPS: 30
SAFE_MARGIN_PERCENT: 5
SCENE_LEAD_SEC: 0.2
SCENE_TAIL_SEC: 0.35
MIN_SCENE_SEC: 2.5
TRANSITIONS: cut | crossfade_6f
VOICE: vi-VN-Standard-NamTram (VieNeu-TTS local SDK)
VOICE_SPEED: 1.0
PACE_MEASURED: 264 WPM (4.4 từ/giây)
LOUDNESS_TARGET_LUFS: -16
WHISPER_MODEL: small
CAPTION_FONT: Be Vietnam Pro
CAPTION_SIZE_PX: 52
CAPTION_COLOR: #F5F0E8
CAPTION_ACTIVE_COLOR: #D7263D
CAPTION_STROKE: 3px #1F2421
CAPTION_POSITION: bottom-center, 14% from bottom
CAPTION_MAX_WORDS_PER_PAGE: 5
MUSIC_FILE: assets/music/background.mp3
MUSIC_GENRE: Calm Lo-fi Acoustic Guitar / Reflective Chillhop (75 BPM)
MUSIC_LEVEL_DB: -22
MUSIC_DUCK_DB: -8
CLIP_AUDIO_LEVEL_DB: -14
EXPORT: H.264 mp4, CRF 18
```

---

## 2. BẢNG PHIÊN ÂM CHUẨN CHO VIENEU-TTS (`tts_text`)

Để tránh VieNeu-TTS đọc sai các con số, tỷ lệ phần trăm và từ viết tắt, mọi cảnh chứa số hoặc ký tự đặc biệt đều được phiên âm chuẩn tiếng Việt thành chữ:

| Mã cảnh | Văn bản gốc (Kịch bản hiển thị) | Phiên âm `tts_text` nạp vào VieNeu-TTS |
|---|---|---|
| **S001** | ...lương 10 triệu có thể để dành được 30 triệu... lương 15 triệu, thậm chí 20 triệu... ngày 25 hàng tháng với tài khoản đúng bằng con số 0 tròn trĩnh. | Một người nhận lương mười triệu có thể để dành được ba mươi triệu sau một năm. Nhưng một người nhận lương mười lăm triệu, thậm chí hai mươi triệu, lại có thể bước vào ngày hai mươi lăm hàng tháng với tài khoản đúng bằng con số không tròn trĩnh. |
| **S002** | Minh là một người như vậy. 26 tuổi, làm việc chăm chỉ 8 tiếng mỗi ngày... | Minh là một người như vậy. Hai mươi sáu tuổi, làm việc chăm chỉ tám tiếng mỗi ngày tại văn phòng, không mua sắm đồ hiệu, cũng chẳng ăn chơi xa xỉ. |
| **S003** | Nhưng sau 3 năm đi làm... | Nhưng sau ba năm đi làm, số dư trong tài khoản của Minh vẫn chỉ đủ để duy trì cuộc sống đến kỳ lương tiếp theo. |
| **S004** | Số tiền mồ hôi nước mắt đó rốt cuộc đã âm thầm biến đi đâu? | Số tiền mồ hôi nước mắt đó rốt cuộc đã âm thầm biến đi đâu? |
| **S005** | Đằng sau mỗi quyết định về tiền bạc luôn có một lý do... | Đằng sau mỗi quyết định về tiền bạc luôn có một lý do. Và hôm nay, chúng ta cùng bóc tách lý do đó. |
| **S006** | ...4 triệu rưỡi tiền thuê nhà, 1 triệu tiền điện nước dịch vụ, 3 triệu tiền ăn uống cơ bản và 1 triệu tiền xăng xe... Tổng cộng mới chỉ có 9 triệu rưỡi. | Nếu bạn hỏi Minh tháng vừa rồi đã tiêu gì, cậu ấy sẽ kể rất vanh vách: bốn triệu rưỡi tiền thuê nhà, một triệu tiền điện nước dịch vụ, ba triệu tiền ăn uống cơ bản và một triệu tiền xăng xe gửi xe. Tổng cộng mới chỉ có chín triệu rưỡi. |
| **S007** | ...dư hơn 5 triệu đồng... | Về mặt lý thuyết, Minh phải còn dư hơn năm triệu đồng. Thế nhưng thực tế, tài khoản của cậu ấy vào cuối tháng luôn chạm đáy. |
| **S008** | Trong tâm lý học hành vi... | Trong tâm lý học hành vi, các chuyên gia chỉ ra rằng: bộ não con người có xu hướng ghi nhớ rất rõ các khoản chi cố định có hóa đơn lớn, nhưng lại hoàn toàn xóa sổ các khoản chi nhỏ lẻ phát sinh trong vô thức. |
| **S009** | Chúng ta luôn mang một ảo tưởng... | Chúng ta luôn mang một ảo tưởng rằng mình đang sống rất chừng mực, trong khi thực tế dòng tiền đang rò rỉ qua hàng chục kẽ hở li ti mỗi ngày mà không hề hay biết. |
| **S010** | ...3 cái bẫy điển hình. | Vậy những kẽ hở đó là gì? Nhìn vào sao kê thực tế của Minh, chúng ta sẽ thấy ba cái bẫy điển hình. |
| **S011** | Sau 8 tiếng chịu áp lực... một ly trà sữa 55 ngàn, một bữa lẩu tối 200 ngàn hay một món đồ 150 ngàn... | Thứ nhất, bẫy chi tiêu tự an ủi. Sau tám tiếng chịu áp lực từ sếp và khách hàng, não bộ rơi vào trạng thái cạn kiệt ý chí. Lúc này, một ly trà sữa năm mươi lăm ngàn, một bữa lẩu tối hai trăm ngàn hay một món đồ một trăm năm mươi ngàn trên sàn thương mại điện tử không còn là nhu cầu vật chất nữa. Nó trở thành liều thuốc giảm đau tinh thần nhanh nhất. |
| **S012** | Chúng ta tự nhủ: "Mình đã vất vả cả ngày rồi..." | Chúng ta tự nhủ: Mình đã vất vả cả ngày rồi, chẳng lẽ không xứng đáng được thưởng một chút niềm vui? |
| **S013** | ...quẹt thẻ tín dụng hay quét một mã QR... | Thứ hai, cái bẫy của thanh toán không tiền mặt. Khi tiền giấy rời khỏi ví, não bộ cảm nhận được nỗi đau mất mát vật lý. Nhưng khi quẹt thẻ tín dụng hay quét một mã quy rờ, cảm giác đau đớn đó gần như biến mất hoàn toàn. Tiền biến thành những con số vô hình trôi đi trên màn hình điện thoại. |
| **S014** | ...dưới 50 ngàn đồng. Một cốc cà phê 35 ngàn, phí vận chuyển đồ ăn 25 ngàn, phí đăng ký xem phim trực tuyến 70 ngàn mỗi tháng... từ 3 đến 5 triệu đồng... | Và thứ ba, cái bẫy của các khoản chi dưới năm mươi ngàn đồng. Một cốc cà phê ba mươi lăm ngàn, phí vận chuyển đồ ăn hai mươi lăm ngàn, phí đăng ký xem phim trực tuyến bảy mươi ngàn mỗi tháng. Từng khoản riêng lẻ thì quá nhỏ để bận tâm, nhưng khi cộng dồn, chúng tạo thành một dòng nước ngầm cuốn phăng từ ba đến năm triệu đồng của bạn mỗi tháng. |
| **S015** | ...3 triệu một tháng có là bao... | Nhiều người sẽ nghĩ: ba triệu một tháng có là bao, nhịn ăn nhịn mặc để tiết kiệm từng đó thì cuộc sống còn ý nghĩa gì? Nhưng hãy cùng làm một phép toán định lượng thực tế. |
| **S016** | ...lãng phí 3 triệu đồng mỗi tháng, sau 1 năm... mất 36 triệu đồng. Sau 5 năm... 180 triệu tiền gốc... sinh lời giả định khiêm tốn 8% một năm, sau 5 năm bạn sẽ có gần 230 triệu đồng. Và sau 10 năm... vượt qua ngưỡng 550 triệu đồng. | Nếu bạn lãng phí ba triệu đồng mỗi tháng, sau một năm bạn đã đánh mất ba mươi sáu triệu đồng. Sau năm năm, con số đó là một trăm tám mươi triệu tiền gốc. Nhưng nếu số tiền đó được đưa vào một quỹ tích sản tự động với mức sinh lời giả định khiêm tốn tám phần trăm một năm, sau năm năm bạn sẽ có gần hai trăm ba mươi triệu đồng. Và sau mười năm, con số đó sẽ vượt qua ngưỡng năm trăm năm mươi triệu đồng. |
| **S017** | 550 triệu không chỉ là tiền... mua lại 3 đến 5 năm tự do... những khoản tiền 30 ngàn, 50 ngàn... | Năm trăm năm mươi triệu không chỉ là tiền. Đó là số tiền đủ để bạn mua lại ba đến năm năm tự do, là khoảng thở để bạn dám nghỉ một công việc độc hại, là tấm khiên bảo vệ gia đình bạn trước những biến cố sức khỏe bất ngờ. Sự nghèo đi không bao giờ diễn ra sau một đêm. Nó là quán tính của những khoản tiền ba mươi ngàn, năm mươi ngàn bị lãng phí đều đặn suốt nhiều năm trời. |
| **S018** | ...tốn 4 triệu đồng sửa chữa... | Và bi kịch thực sự chỉ lộ diện khi biến cố đầu tiên ập đến. Tháng trước, chiếc xe máy của Minh bị hỏng động cơ, tốn bốn triệu đồng sửa chữa. Cùng lúc đó, mẹ ở quê gọi điện lên báo cần một khoản tiền thuốc men định kỳ. |
| **S019** | ...không có nổi 5 triệu tiết kiệm... trả góp 12 tháng... | Trong tài khoản không có nổi năm triệu tiết kiệm, Minh rơi vào trạng thái hoảng loạn tột độ. Để giữ thể diện và không muốn gia đình lo lắng, Minh buộc phải quẹt thẻ tín dụng và bấm chọn tính năng chia nhỏ trả góp mười hai tháng. Minh không nhận ra rằng, mình vừa chính thức bước chân vào vòng lặp nợ hình ảnh. |
| **S020** | ...thanh pin điện thoại... | Tại sao việc cố gắng dùng ý chí để giữ tiền lại luôn thất bại? Các nhà tâm lý học hành vi đã chứng minh: Ý chí con người giống như một thanh pin điện thoại, nó cạn kiệt dần sau mỗi quyết định bạn đưa ra trong ngày. |
| **S021** | ...Không có ý chí nào mạnh bằng một hệ thống tự động... | Nguyên tắc cốt tử ở đây là: Không có ý chí nào mạnh bằng một hệ thống tự động. Nếu muốn giữ được tiền, bạn phải lấy ý chí của mình ra khỏi cuộc chơi. |
| **S022** | ...quy trình 3 bước cực kỳ đơn giản sau: | Thay vì chờ đến cuối tháng xem còn thừa bao nhiêu mới đem đi tiết kiệm, bạn hãy thiết lập lại dòng tiền của mình bằng quy trình ba bước cực kỳ đơn giản sau: |
| **S023** | Bước 1: Áp dụng nguyên tắc "Trả cho mình trước", trích ngay 15% tương đương 2 triệu 200 ngàn đồng. Bước 2: Tách biệt hoàn toàn 2 tài khoản ngân hàng... Bước 3: Cài đặt lệnh chuyển khoản tự động trong đúng 30 giây đầu tiên nhận lương. | Bước một: Áp dụng nguyên tắc Trả cho mình trước, trích ngay mười lăm phần trăm tương đương hai triệu hai trăm ngàn đồng. Bước hai: Tách biệt hoàn toàn hai tài khoản ngân hàng sinh hoạt và tích lũy. Bước ba: Cài đặt lệnh chuyển khoản tự động trong đúng ba mươi giây đầu tiên nhận lương. |
| **S024** | Mục tiêu của việc quản lý tiền bạc... mua lại cho bạn một khoảng thở... Hẹn gặp lại bạn ở khoảng thở tiếp theo. | Mục tiêu của việc quản lý tiền bạc chưa bao giờ là biến bạn thành một người tằn tiện, keo kiệt. Mục tiêu của nó là mua lại cho bạn một khoảng thở, sự bình thản và quyền được lựa chọn trước cuộc đời. Sau video này, bạn nhận ra khoản chi nào đang âm thầm rút cạn tài khoản của mình nhiều nhất? Tiền nào cũng có lý do, và quyết định tiếp theo luôn nằm ở bạn. Hẹn gặp lại bạn ở khoảng thở tiếp theo. |

---

## 3. THIẾT LẬP PHỤ ĐỀ KARAOKE TRONG REMOTION

```tsx
// Cấu hình Remotion Subtitles (Captions)
const subtitleConfig = {
  fontFamily: 'Be Vietnam Pro',
  fontWeight: 600,
  fontSize: 52,
  lineHeight: 1.3,
  letterSpacing: '-0.02em',
  color: '#F5F0E8', // Giấy ngà ấm
  activeColor: '#D7263D', // Đỏ gạch Terracotta highlight từng từ
  textStroke: '3px #1F2421', // Viền đen than chống chìm chữ
  textAlign: 'center' as const,
  positionBottom: '14%',
  maxWordsPerPage: 5,
};
```
