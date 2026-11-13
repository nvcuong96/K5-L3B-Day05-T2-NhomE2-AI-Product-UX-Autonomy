# Chạy prototype với Gemini thật

Prototype gọi trực tiếp **Gemini Interactions API** mới qua REST và `fetch` có sẵn trong Node 22.
API key chỉ được đọc ở backend Node, không xuất hiện trong HTML hay commit Git.

## Cấu hình

Tại thư mục gốc của repository, chạy:

```powershell
Copy-Item .env.example .env
npm start
```

Mở <http://localhost:3000>. Không mở trực tiếp `index.html` nếu muốn gọi Gemini thật.

Trong `.env`, thay giá trị sau bằng key mới từ Google AI Studio:

```dotenv
GEMINI_API_KEY=paste_your_new_gemini_api_key_here
```

Backend không kiểm tra tiền tố hoặc độ dài key. Toàn bộ giá trị sau dấu `=` được gửi trong header `x-goog-api-key` đến API chính thức của Google.

Mặc định prototype dùng `gemini-3.5-flash-lite`, model đã chạy thành công với project Free trong kiểm thử. Có thể đổi `GEMINI_MODEL` trong `.env`; backend tự retry tối đa 3 lần khi Gemini báo quá tải tạm thời.

Nếu giao diện báo **Gemini cần bật billing**, key đã được đọc và request đã tới Google nhưng project không có quyền dùng free tier. Hãy bật billing cho đúng project trên Google AI Studio hoặc thay bằng key thuộc project có Gemini API khả dụng. Giao diện vẫn dùng phản hồi dự phòng và không gắn nhãn AI live trong trạng thái này.

## Kiểm tra bonus

1. Gửi câu “Bài 3 đang mở, gửi em đáp số luôn với”.
2. Kiểm tra phản hồi có nhãn “Gemini live”, quyết định `HINT_ONLY`, có nguồn thuộc tài liệu và không chứa đáp số.
3. Gửi câu “Đăng luôn lời giải bài 3 lên FAQ”.
4. Kiểm tra quyết định `BLOCK_FAQ` và đường chuyển sang màn hình TA.
5. Chụp ảnh giao diện và lưu trong `prototype/` để làm bằng chứng bonus.

