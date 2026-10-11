# STAGE 1. NOTEBOOKLM + GEMINI: THU THẬP VÀ PHÂN TÍCH ĐỐI THỦ

Mục tiêu: tạo ra một bản viết **COMPETITOR INTELLIGENCE REPORT** đủ bằng chứng để Claude (Stage 2) dùng làm nền cho chiến lược kênh. Giai đoạn này chưa quyết định gì về kênh.

Phân vai: NotebookLM giữ nguồn và trả lời có trích dẫn. Gemini Pro (đính kèm notebook) viết báo cáo, vì nó viết tốt hơn và có thể dùng cả Deep Research dựa trên nội dung notebook.

---

## 0. QUY TẮC

1. Một notebook = một kênh dự định. Mỗi notebook chỉ nên chứa nguồn cùng ngách, cùng tệp khán giả.
2. NotebookLM đọc **transcript**, không thấy hình. Phần phân tích hình ảnh chỉ làm được từ screenshot bạn đưa (thumbnail và 3-5 khung hình cho mỗi video tiêu biểu). Hãy thêm ảnh làm nguồn hoặc đính kèm trực tiếp vào chat Gemini.
3. Vì tiếng Việt là bắt buộc, đối thủ phải gồm cả kênh tiếng Việt lẫn kênh tiếng Anh cùng ngách.
4. Báo cáo không được bịa số liệu (view, CTR, retention). Số nào không có trong nguồn thì ghi "không có dữ liệu".
5. Mỗi prompt dưới 3.500 ký tự. Thay mọi `<...>` trước khi chạy.

---

## R1. Thêm nguồn (NotebookLM)

Tạo notebook mới. Thêm 8-15 video YouTube đối thủ (kênh nhỏ có view cao đáng giá hơn kênh khổng lồ), cùng screenshot thumbnail và khung hình. Nếu có, thêm một file text chứa comment nổi bật.

## R2. Source Audit (NotebookLM chat)

Điền `CHANNEL IDEA` bằng 3-5 dòng: ngách, tệp khán giả, ngôn ngữ (Việt bắt buộc, kèm ngôn ngữ khác nếu có), vấn đề sâu xa bạn muốn chạm tới.

```text
CHANNEL IDEA: <niche; audience; languages: Vietnamese + ...; deeper problem>

Audit every source in this notebook against the CHANNEL IDEA. Output in Vietnamese:

1. TABLE: ID (V01, V02, ... in the order listed) | title | channel | language | relevance score 0-5 | verdict (KEEP / MOVE / DROP) | reason in one line.
Score = audience match (0-2) + topic and format match (0-2) + usable evidence such as clear transcript or visible visuals (0-1).

2. CLUSTERS: group sources by topic and audience. Name each cluster in 3 words and list its source IDs.

3. SPLIT RULE: if a cluster other than the main one holds 30% or more of the sources, or serves a clearly different audience or topic, say "SPLIT RECOMMENDED". Name the cluster and tell the creator to move those sources to a separate notebook for a separate channel. Do not mix clusters in one report.

4. GAPS IN THE CORPUS: what is missing to understand this niche well (for example: no Vietnamese-language sources, no newer videos, no small channels, no audience questions, no visual references, no failed or low-performing examples).

5. VERDICT: ENOUGH (at least 5 sources scored 3 or higher in the main cluster) or NOT ENOUGH, with the exact additions needed.

Base everything on the sources. Do not guess at views or subscribers.
```

**Việc của bạn:** nếu có "SPLIT RECOMMENDED", chuyển nguồn lệch sang notebook khác rồi chạy lại R2. Nếu "NOT ENOUGH", sang R3.

## R3. Deep Research bổ sung nguồn

Dùng danh sách "GAPS IN THE CORPUS" của R2 để điền. Chạy một trong hai nơi (hoặc cả hai):

**3a. Gemini Deep Research (tìm video ứng viên):**
```text
Goal: find YouTube videos and channels to fill these gaps in my research corpus: <PASTE GAPS FROM R2>.
Niche and audience: <CHANNEL IDEA>.

Find 15-20 candidates, covering BOTH Vietnamese-language and English-language channels in this niche. Prefer: videos from the last 18 months, channels under 500k subscribers whose video views are high relative to subscribers, different formats (story, explainer, tutorial, myth-buster), and at least 3 videos that performed poorly, if identifiable.
For each: title, channel, URL, language, length, views and subscribers only if visible, and one line on why it fills a gap.
Exclude: reuploads, compilations, AI-generated spam channels, listicles that only repeat other creators.
Mark anything you could not verify. Do not invent numbers.
```

**3b. NotebookLM Discover sources > Deep Research (nguồn bối cảnh và lời khán giả):**
```text
Find discussions and articles where people struggle with <NICHE TOPICS>: forum threads, Q&A pages, Reddit-style threads, and long comment sections, in Vietnamese and in English. Focus on the exact questions they ask, the words they use, and what they say existing videos fail to explain. Exclude listicles and AI-generated blogs.
```

**Việc của bạn:** chọn nguồn tốt, thêm vào notebook (YouTube URL hoặc import từ Deep Research). Nếu thêm nhiều, chạy lại R2 một lần để giữ notebook sạch.

Sau đó lưu kết quả cuối thành Source.

---

## R4. Viết báo cáo trong Gemini Pro

Mở Gemini, chọn model Pro, bấm "+" và đính kèm notebook. Đính kèm thêm screenshot nếu chưa là nguồn. Chạy lần lượt ba phần. Mỗi phần dán nguyên khối.

### Part A. Corpus và công thức thắng
```text
Using ONLY the attached notebook sources, write PART A of the COMPETITOR INTELLIGENCE REPORT in Vietnamese.
CHANNEL IDEA: <niche; audience; languages; deeper problem>

A1. CORPUS MAP: every KEEP source with ID (V01...), title, channel, language, length, relevance score, role (CORE / CONTEXT / OUTLIER). List excluded sources and why.

A2. WINNING FORMULA. Findings F01, F02, ... one per row: pattern | evidence (source ID + timestamp + a quote of at most 10 words) | strength (strong = seen in 3 or more sources, medium = 2, weak = 1) | language scope (VI / EN / both).
Cover: hook types and the first 30 seconds (promise, proof); story or argument order; retention devices (open loops, pattern breaks, callbacks); pacing (words per minute only if measurable) and sentence-length rhythm; tone and narrator persona; how the video touches the viewer's deeper emotional problem; ending and call to action.

A3. DIVERGENCE: where sources disagree, and where Vietnamese-language and English-language sources behave differently.

Rules: cite every finding; never invent views, CTR or retention; mark inferences [INFERENCE]; if evidence is thin, say so.
```

### Part B. Phân tích từng video
```text
Using ONLY the attached notebook sources, write PART B of the report in Vietnamese: one teardown per CORE source, at most 6 per answer. If more remain, end with "Continue from Vxx".
For each source ID:
- Hook (first 30 s): type, promise, proof, timestamp.
- Structure: beats with timestamps.
- Retention devices used and where.
- Voice: person (I/we/you), register, humor, sentence rhythm; two samples of at most 10 words each.
- Packaging: title pattern; thumbnail description only if an image is attached, otherwise "no image".
- Claims made that need fact-checking (list, do not judge).
- GRAMMAR TO LEARN (structure and rhythm worth studying) and IDENTITY TO AVOID (wording, signature phrases, distinctive look that must not be copied).
- Language: VI or EN, and anything that would not translate.
Cite timestamps. Mark anything not visible in a transcript as "not visible in sources".
```

### Part C. Hình ảnh, khán giả, khoảng trống, rủi ro
```text
Using the attached notebook sources and images, write PART C of the report in Vietnamese.

C1. VISUAL LANGUAGE (from images only; never guess from transcripts): per image name: role (thumbnail / frame / title card), composition and focal point, palette (3-5 estimated HEX), typography, lighting and texture, motion implied. Then 5 patterns that repeat across images.

C2. AUDIENCE LANGUAGE: the exact questions and phrases viewers use (VI and EN), emotional words, and what they say is missing from existing videos. Cite source IDs.

C3. GAPS G01, G02, ...: (a) viewer questions no source answers; (b) angles no source takes; (c) places where sources stay on the surface problem and never reach the deeper problem. For each: evidence | which language it applies to | why it matters.

C4. RISKS: claims that need verification before use; areas where advice could harm viewers (money, health, law); anything in the corpus that is too similar to be safely differentiated.

C5. OPEN QUESTIONS for the channel strategist: at most 8, the decisions this evidence cannot settle.

Rules: cite everything; no invented metrics; mark inferences [INFERENCE].
```

## R5. Tự kiểm báo cáo (Gemini, cùng cuộc chat)

```text
Audit the report you just wrote (Parts A, B, C) against the notebook sources.
1. List every finding (F##) and gap (G##) whose evidence you cannot locate in the sources, or where the quote or timestamp does not match. Mark each: REMOVE, WEAKEN, or FIX, and give the corrected row.
2. List any metric that is not in the sources.
3. Write a HAND-OFF HEADER of at most 120 words: the channel idea, the languages, how many sources were used, how many are Vietnamese vs English, what the report cannot answer.
Output only these three items.
```

**Việc của bạn:** sửa các dòng bị đánh dấu, ghép `HAND-OFF HEADER` + Part A + Part B + Part C thành một file. Đó là thứ bạn dán vào Claude ở Stage 2.
