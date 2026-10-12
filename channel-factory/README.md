# Channel Factory

Repo md để đi từ ý tưởng thô về một kênh YouTube đến video đầu tiên và skill cho agent yếu hơn, theo một master prompt duy nhất. Bản v2 đã thêm nghiên cứu đối thủ, đủ lớp L0-L11 của video đầu tiên và bước đóng gói skill.

## Cách dùng
1. Mở chat mới, dán nguyên `MASTER_PROMPT.md`.
2. Điền form A0 (trả lời thô cũng được). Master prompt chạy mỗi lần một stage; bạn trả lời `ok`, `revise: <note>`, `back`, `skip` hoặc `jump <stage>`.
3. Sau mỗi stage, lưu khối LOCKED vào repo của kênh (gợi ý bên dưới).
4. Từ B1 trở đi, dán thêm `BIBLE.md` của kênh vào đầu chat để agent giữ đúng DNA.

## Luồng
| Stage | Việc | Kết quả khóa |
|---|---|---|
| R0 | Nhập ý tưởng thô, tạo khối CHANNEL IDEA | Recap + CHANNEL IDEA |
| R1 | Chạy research kit ngoài chat (NotebookLM + Gemini), hoặc LITE bằng web search | COMPETITOR INTELLIGENCE REPORT (V##, F##, G##) |
| R2 | Thử thách báo cáo, mỗi giai đoạn hành trình một verdict | SUFFICIENT / INSUFFICIENT |
| A1 | Gợi ý tên + mô tả | NAME BLOCK |
| A2 | Chiến lược (trích F##, G##) | STRATEGY |
| A3 | DNA | DNA |
| A4 | Câu mở đầu và câu kết | SIGNATURE BLOCK |
| A5 | SEO, avatar, banner, cài đặt Studio | SETUP SHEET |
| A6 | Gộp lại | CHANNEL BIBLE v1 |
| B1 | Kế hoạch 10 video để đo dữ liệu | VIDEO PLAN |
| B2 | Prompt tạo mẫu asset, chốt visual | VISUAL v1 |
| B3 | Video đầu tiên, lớp L0-L11, kết bằng hand-off cho Remotion | LOCK RECORDS, SCENE_PLAN.json, PARAMETERS, SEO |
| B4 | Chat mới: đóng gói skill cho agent yếu hơn | SKILL package |

## Hướng dẫn chi tiết
Xem `docs/HUONG_DAN.md` (từng bước, lệnh, việc làm ngoài chat, gỡ rối).

## Cấu trúc
- `MASTER_PROMPT.md`: prompt chính (dán vào chat Claude).
- `phases/`: các prompt gốc đã chạy tốt, dùng khi cần chạy đầy đủ từng giai đoạn: `STAGE1_RESEARCH_KIT.md` (NotebookLM + Gemini), `STAGE2_CHANNEL_ARCHITECT.md`, `STAGE3_FIRST_COMMIT_DIRECTOR.md`, `STAGE4_SKILL_COMPILER.md`, `REMOTION_ASSEMBLY_AGENT_PROMPT.md`.
- `templates/`: khung điền cho Bible, kế hoạch 10 video, khóa visual, video đầu tiên, nhật ký đo.
- `examples/tien-co-ly-do.seed.md`: các quyết định đã có cho kênh Tiền Có Lý Do và khối CHANNEL IDEA để chạy nghiên cứu.
- `docs/LESSONS.md`: bài học từ kênh Chốt Sổ Cuối Ngày, gồm danh sách phải làm lại khi đổi tên.

## Gợi ý lưu kết quả
```
channels/<handle>/
  research/REPORT.md
  BIBLE.md
  plan/VIDEO_PLAN.md
  visual/VISUAL_LOCK.md  (+ ảnh đã duyệt)
  videos/V01/{SCRIPT.md, SCENE_PLAN.md, PUBLISH.md}
  metrics/VIDEO_REVIEW.md
```
