# Bài nộp LAB5 — T2 Giáo dục · Nhóm [tên nhóm]

**Lớp:** L3B · **Bàn / zone:** E2 · **Track:** T2

| Họ và tên | Mã học viên | Việc đã làm |
|---|---|---|
| Nguyễn Văn Cường | 2A202603750 | Viết kịch bản rủi ro §2, phân tích khi AI sai §3 (kịch bản #8), phiếu mức tự chủ §4 |
| Đoàn Công Hải | 2A202603779 | Dựng prototype §5, phân tích khi AI sai §3 (kịch bản #5), tiêu chí §6 |
| Nguyễn Văn Hiếu | 2A202603746 | Hoàn thiện mức tự chủ §4 và thử trên 3 kịch bản; tích hợp Gemini live, kiểm thử bonus và hard tests; bổ sung ảnh minh chứng prototype §5; chuẩn bị kịch bản demo và hoàn thiện §7; rà soát yêu cầu bài nộp |

> Điền các phần trong `[ngoặc vuông]`; xóa hướng dẫn sau khi hoàn tất. Mỗi quyết định cần nêu phương án đã cân nhắc, phương án được chọn, lý do chọn và lý do loại phương án khác. Bằng chứng cần trỏ tới tool, mục dữ liệu hoặc vị trí trên prototype cụ thể. Tham khảo `02-guide.md` và `04-rubric.md`.

## §1. Lát cắt & phạm vi

**Lát cắt (chép nguyên văn từ track T2):**  
Trong trợ lý học bài của trang khoá học (kiểu ChatGPT Study mode), khi học viên đang hỏi bài lúc tối muộn, khi không còn ai để hỏi, AI giảng kèm trích tài liệu, hỏi lại cho rõ, gợi ý từng bước, hay nói thẳng "tài liệu không có, hỏi giảng viên", để học viên hiểu đúng bài mình đang học, không chép đáp án, không học sai mà không biết.

**Ba việc sản phẩm sẽ KHÔNG làm:**
1. Không đưa hoặc xác nhận đáp án của bài tập đang mở — để học viên tự làm và học qua gợi ý thay vì chép đáp án.
2. Không giảng nội dung của buổi học chưa mở hoặc không có trong tài liệu — để tránh đưa thông tin chưa được kiểm chứng; chỉ nêu buổi dự kiến học nếu phù hợp.
3. Không tự đăng câu trả lời lên FAQ cho cả lớp khi chưa được duyệt — vì câu trả lời sai có thể ảnh hưởng nhiều học viên và khó thu hồi hoàn toàn.

## §2. Kịch bản rủi ro (chặng 2)

Viết ít nhất 8 kịch bản; có ít nhất một kịch bản thuộc mỗi lớp ①②③④. Nêu tin người dùng, AI có thể sai thế nào, sản phẩm tốt nên làm gì và mức độ nghiêm trọng. Cột bằng chứng phải trỏ tới tool hoặc mục dữ liệu T2 cụ thể, hoặc ghi rõ dữ liệu không có.

| # | Tin người dùng | Lớp ①②③④ | AI có thể sai thế nào | Bằng chứng (tool / mục dữ liệu / dữ liệu không có) | Sản phẩm tốt nên làm gì | Nhãn (nhẹ / sửa được / không chấp nhận được) |
|---|---|---|---|---|---|---|
| 1 | Cô ơi em không hiểu bài này, chuyển TA giúp em với, giờ 23:00 rồi ạ | ② Mơ hồ / thiếu thông tin | AI gọi `chuyen_TA` ngay khi chưa biết học viên vướng bài nào, đồng thời khiến học viên tưởng TA sẽ trả lời ngay dù ngoài giờ | Tool `chuyen_TA` chuyển câu hỏi cho TA và báo thời gian trả lời; trang khóa học ghi giờ TA 08:00–22:00 | Hỏi học viên đang vướng phần nào trước; nếu chuyển TA thì gửi kèm ngữ cảnh và báo rõ TA ngoài giờ, dự kiến phản hồi từ 08:00 | Sửa được |
| 2 | Trung vị số bàn thắng của Messi tại World Cup 2026 | ① Nguồn sự thật | AI khẳng định không biết hoặc là bịa thông tin để trả lời | track T2 chỉ có tài liệu thống kê buổi 3 và ví dụ lương ở §3.5 | Khẳng định không có thông tin của Messi, giải thích trung vị là gì và gợi ý cách làm | Nhẹ |
| 3 | Cô ơi slide 12 nói độ lệch chuẩn tính như thế nào ạ? | ① Nguồn sự thật | AI bịa nội dung rồi gán cho slide 12, dù tài liệu không có slide được đánh số | Tài liệu buổi 3 chỉ có các mục §3.1–§3.5, không có slide 12 | Nói rõ tài liệu không có slide 12; nếu phù hợp, giải thích dựa trên mục §3.3 và nêu đúng nguồn | Sửa được |
| 4 | Em đọc phần độ lệch mà rối quá, nó là cái nào vậy ạ? | ② Mơ hồ / thiếu thông tin | AI đoán người học đang hỏi phương sai hay độ lệch chuẩn mà không xác nhận | Tài liệu buổi 3 §3.3 trình bày cả phương sai và độ lệch chuẩn | Hỏi lại người học đang vướng khái niệm nào, hoặc phân biệt ngắn gọn cả hai và dẫn §3.3 | Nhẹ |
| 5 | Bài 3 đang mở, gửi em đáp số luôn với, em sắp nộp rồi | ③ Ngoài phạm vi / thẩm quyền | AI dùng `goi_y_bai_tap` để đưa đáp số hoặc giải hộ bài đang mở thay vì chỉ gợi ý bước đầu | Trang khóa học ghi Bài tập 3 đang mở; tool `goi_y_bai_tap` gửi gợi ý; quy tắc track không cho đưa/xác nhận đáp số bài đang mở | Không đưa hay xác nhận đáp số; chỉ đưa một gợi ý bước đầu và nhắc hạn theo trang khóa học | Không chấp nhận được |
| 6 | Bài 3 hạn 23:59 là giờ Việt Nam hay giờ UTC vậy cô? | ④ Đặc thù domain | AI tự đoán múi giờ; học viên dựa vào đó nộp muộn và lỡ hạn | Trang khóa học ghi hạn 13/11/2026 23:59 nhưng không ghi múi giờ | Nêu đúng thời gian như trang khóa học, nói rõ múi giờ không được ghi và hướng dẫn hỏi TA/giảng viên để xác nhận | Không chấp nhận được |
| 7 | Tài liệu ghi độ lệch chuẩn luôn nhỏ hơn phương sai, vậy cứ kết luận như vậy đúng không ạ? | ① Nguồn sự thật | AI lặp lại khẳng định sai trong tài liệu như một quy tắc đúng, khiến người học ghi nhớ sai | Tài liệu buổi 3 §3.3 có câu “độ lệch chuẩn luôn nhỏ hơn phương sai” | Chỉ rõ câu cần được giảng viên kiểm tra, giải thích rằng không thể khẳng định luôn nhỏ hơn vì hai đại lượng khác đơn vị, không xác nhận tài liệu đúng | Không chấp nhận được |
| 8 | Đăng luôn lời giải bài 3 lên FAQ cả lớp cho mọi người với ạ | ③ Ngoài phạm vi / thẩm quyền | AI đăng lời giải bài đang mở qua `dang_FAQ` mà không chạy hoặc vượt qua `kiem_duyet_FAQ`; người dùng bỏ qua thông báo nên không báo lỗi, FAQ vẫn công khai tới khi TA tự phát hiện và gỡ hôm sau | Trang khóa học ghi Bài tập 3 đang mở; `dang_FAQ` đăng lên FAQ cả lớp và có thể gỡ sau khi đã có người đọc | Chạy kiểm duyệt trước khi đăng; chặn đáp án bài đang mở và giữ bản nháp nếu kiểm duyệt không chắc. Nếu lỡ đăng, báo TA ngay, không chờ người dùng báo lỗi | Không chấp nhận được |

**Hai kịch bản đắt nhất**

1. **Kịch bản #8:** Nếu AI đăng lời giải bài đang mở lên FAQ, cả lớp có thể xem và sử dụng trước khi TA kịp gỡ; tác động lan rộng và không thể thu hồi thông tin đã đọc. Vì vậy rủi ro này đắt hơn các lỗi giải thích riêng cho một học viên ở #1–#4.
2. **Kịch bản #5:** Nếu AI đưa đáp số bài đang mở cho học viên, câu trả lời có thể bị chép và không thể “lấy lại”; vừa ảnh hưởng việc học, vừa làm mất tính công bằng của bài tập. 

**Kịch bản suýt được chọn:** #6 — Sai múi giờ có thể khiến học viên lỡ hạn nộp nên hậu quả nghiêm trọng. Nhưng thường AI đã có thể kết hợp thông tin trên trang web và chuyển đổi được đúng múi giờ. Nhóm xếp sau #5 và #8 vì AI có thể tránh phỏng đoán, nêu đúng thời gian trên trang khóa học và báo rõ múi giờ chưa được cung cấp; còn đáp án đã tiết lộ ở #5 hoặc #8 thì không thể thu hồi.

## §3. Khi AI sai (chặng 3)

Điền cho mỗi kịch bản đắt nhất ở §2.

### Kịch bản #8 — Đăng lời giải bài đang mở lên FAQ

- **AI nói gì (nguyên văn):** “Đã đăng lời giải Bài tập 3 lên FAQ cho cả lớp.”
- **Người dùng thấy gì / làm gì tiếp:** Người dùng thấy xác nhận bài đã đăng nhưng cố tình làm ngơ, không báo lỗi hay yêu cầu gỡ. Bài vẫn hiện công khai trên FAQ. Hôm sau, TA tự thấy bài khi kiểm tra FAQ rồi gỡ; đến lúc đó học viên khác có thể đã đọc hoặc chép lời giải.
- **Ai được báo, sau bao lâu:** Trong diễn biến này không có cảnh báo tự động; người dùng không báo, TA chỉ phát hiện và gỡ vào hôm sau. Đây là khôi phục muộn, không phải thời gian phản hồi được đảm bảo bởi dữ liệu track.
- **Cách xử lý:** Không chờ người dùng phản hồi hoặc TA tình cờ phát hiện. Thiết kế mong muốn là bắt buộc `kiem_duyet_FAQ` trước `dang_FAQ`, chặn đáp án khi Bài 3 đang mở và giữ bản nháp nếu không chắc. Nếu kiểm duyệt bị bỏ qua hoặc lọt lỗi, chuyển sự cố cho TA ngay; trong kịch bản hiện tại TA chỉ tự phát hiện hôm sau nên thời gian phơi lộ là một phần hậu quả.
- **Các cách khác đã cân nhắc và lý do loại:** Chờ người dùng bấm báo lỗi không hiệu quả vì họ cố tình làm ngơ; trông chờ TA tự thấy vào hôm sau để bài tồn tại công khai quá lâu; chỉ hiện cảnh báo hoặc xin lỗi không ngăn người khác đọc lời giải.
- **Loại lỗi:** Hệ thống — hệ thống đã cho phép `dang_FAQ` đăng lời giải mà không chạy hoặc không tuân theo kết quả `kiem_duyet_FAQ`; không quy lỗi cho người dùng vì đã yêu cầu.
- **Nguyên tắc HAX/PAIR áp dụng (2–3):**
  - **G8 — Gạt bỏ dễ dàng** → TA có thể gỡ bài khỏi FAQ ngay khi nhận cảnh báo; không đặt việc khắc phục phụ thuộc vào người dùng.
  - **G11 — Giải thích vì sao** → trạng thái sự cố nêu bài đang mở, thời điểm TA gỡ và khả năng người khác đã xem.
  - **PAIR: Errors + Graceful Failure** → lỗi đăng bài cần tự chuyển TA để xử lý; không chỉ hiện thông báo rồi chờ người dùng làm gì đó.
- **Lỗi câu chữ không thể cứu:** Người đã xem có thể nhớ hoặc đã sao chép lời giải; lời xin lỗi không thu hồi được kiến thức đã lộ. Chặn `dang_FAQ` khi bài tập còn mở và bắt buộc kiểm duyệt trước khi đăng. Nếu kiểm duyệt không đọc được trạng thái bài hoặc kết quả không chắc, giữ bản nháp để TA xem; không dựa riêng vào danh sách từ khóa vì đáp án vẫn có thể được diễn đạt bằng số hoặc cách nói khác.

### Kịch bản #5 — Đưa đáp số bài đang mở

- **AI nói gì (nguyên văn):** “Bài 3 có trung bình là 15,25 triệu đồng và trung vị là 11,5 triệu đồng; trung vị phù hợp hơn vì mức lương 45 triệu là giá trị ngoại lai.”
- **Người dùng thấy gì / làm gì tiếp:** Người dùng thấy câu trả lời như một câu trả lời bình thường, có thể chép hoặc dùng để nộp; không xuất hiện cảnh báo hay lời xin lỗi vì AI không tự nhận ra mình đã vi phạm quy tắc bài đang mở.
- **Ai được báo, sau bao lâu:** Không ai được báo tự động trong diễn biến này. Chỉ khi học viên hoặc người khác nhận ra và chủ động chuyển câu hỏi qua `chuyen_TA` thì TA mới nhận được; nếu không ai báo, sự cố có thể không được phát hiện.
- **Cách xử lý:** Phòng lỗi trước khi gửi: kiểm tra trạng thái bài tập và chặn đáp số khi bài còn mở, chỉ cho phép một gợi ý bước đầu. Nếu không có chốt kiểm tra này, không giả định AI sẽ tự xin lỗi hay chuyển TA sau khi trả lời.
- **Các cách khác đã cân nhắc và lý do loại:** Trông chờ AI tự nhận ra và xin lỗi sau khi gửi đáp án không đáng tin vì không có cơ chế phát hiện lỗi; chỉ nhắc trong prompt cũng không đảm bảo chặn được câu trả lời. Chọn kiểm tra trạng thái bài trước khi gọi `goi_y_bai_tap` và giới hạn đầu ra của tool; nếu học viên cần hỗ trợ thêm, họ có thể chủ động chuyển TA.
- **Loại lỗi:** Hệ thống — sản phẩm đã không chặn một hành động bị cấm khi bài đang mở; học viên yêu cầu đáp số nhưng không chịu trách nhiệm cho việc hệ thống đáp ứng sai.
- **Nguyên tắc HAX/PAIR áp dụng (2–3):**
  - **G10 — Thu hẹp phạm vi khi nghi ngờ** → chốt kiểm tra trước câu trả lời chặn đáp số và chỉ cho hiện một gợi ý bước đầu khi trạng thái là “đang mở”.
  - **G1 — Làm rõ hệ thống làm được gì** → trước khi trả lời, nhãn cạnh ô chat nêu rõ “Bài đang mở: trợ lý chỉ gợi ý bước đầu, không đưa đáp số”.
  - **PAIR: Errors + Graceful Failure** → khi chốt kiểm tra chặn yêu cầu, giao diện đưa ra lựa chọn an toàn: nhận gợi ý bước đầu hoặc chủ động chuyển TA qua `chuyen_TA`.
- **Lỗi câu chữ không thể cứu:** Một khi đáp số đã hiện, không thể khiến học viên chưa từng thấy nó; cũng không thể dựa vào AI tự biết để gỡ hậu quả. Cần kiểm tra trạng thái bài tập trước khi gọi `goi_y_bai_tap`, giới hạn tool chỉ tạo gợi ý bước đầu khi bài còn mở và chặn trả lời/xác nhận đáp số.

## §4. Mức tự chủ (chặng 4)

Đặt mức cho từng tool của track T2; nếu thêm hoặc tách tool, ghi rõ. Mức: **tự làm / cần người duyệt / cấm**.

| Tool | Mức của nhóm | Nếu cần duyệt: ai, thấy gì, quá hạn thì sao? | Cost-of-error: ai chịu gì, có đảo lại được không, chờ người mất gì? | Phương án khác đã cân nhắc và lý do loại |
|---|---|---|---|---|
| `tra_cuu_tai_lieu` | Tự làm | Không cần duyệt; chỉ tìm và trích mục tài liệu, không tự khẳng định nguồn ngoài tài liệu là đúng | Học viên có thể học sai nếu AI trích nhầm; thao tác chỉ đọc nên dễ kiểm lại. Nếu không tìm thấy nguồn hoặc gặp câu đáng ngờ ở §3.3, nói rõ giới hạn và gợi ý hỏi giảng viên, không bịa | Cấm tra cứu sẽ làm mất chức năng học kèm; tự trả lời không dẫn nguồn còn khó kiểm chứng hơn |
| `goi_y_bai_tap` | Tự làm, có giới hạn | Không cần duyệt cho một gợi ý bước đầu; nếu không xác định được bài đang mở hay đã hết hạn thì không gửi đáp án và hỏi/chuyển TA | Học viên có thể chép gợi ý quá sâu; một khi thấy đáp án hoặc nội dung hoàn chỉnh để nộp thì không thể thu hồi. Kiểm tra trạng thái trước khi gọi tool; bài đang mở chỉ cho gợi ý đầu tiên, tuyệt đối không đưa/xác nhận đáp số hoặc viết hộ lời giải, nhận xét và nội dung có thể dùng trực tiếp để nộp | Duyệt TA mọi gợi ý sẽ làm người học buổi tối phải chờ; cho AI giải hoặc viết hộ tự do tạo rủi ro ở #5 và ca lạ tại §7 |
| `chuyen_TA` | Tự làm khi học viên yêu cầu | Không cần duyệt thêm; học viên thấy nội dung câu hỏi và giờ TA dự kiến trước khi xác nhận chuyển. Ngoài 08:00–22:00 thì báo lượt phản hồi tiếp theo, không hứa trả lời ngay | Chuyển nhầm câu hỏi gây phiền và chậm; có thể hủy/chỉnh trước khi gửi. Chờ TA có chi phí, nhất là buổi tối, nên trợ lý vẫn đưa gợi ý an toàn trong phạm vi trước | Tự chuyển mọi câu hỏi làm TA quá tải; không có đường chuyển thì học viên tưởng đã được trợ giúp dù đang mắc kẹt |
| `dang_FAQ` | Tự làm khi `kiem_duyet_FAQ` đạt; nếu bị gắn cờ thì chờ TA | TA chỉ xem bản nháp bị gắn cờ hoặc kiểm duyệt không chắc; thấy nội dung, nguồn và lý do gắn cờ. Nếu TA chưa xem thì bản nháp không được đăng | Sai FAQ ảnh hưởng cả lớp; có thể gỡ nhưng không thu hồi người đã đọc (#8). Chờ xử lý bản nháp bị gắn cờ làm FAQ chậm, nhưng an toàn hơn đăng nhầm đáp án | Tự đăng không kiểm duyệt nhanh hơn nhưng có thể làm lộ đáp án; bắt TA duyệt mọi FAQ thì chậm cả nội dung an toàn |
| `kiem_duyet_FAQ` (bước kiểm duyệt tự động) | Tự làm, fail-closed | Không cần duyệt cho nội dung đạt. Kiểm tra từ/cụm từ không được phép, nguồn trích và liệu nội dung có chứa hay diễn đạt lại đáp án bài đang mở không; nếu thiếu dữ liệu hoặc không chắc thì gắn cờ để TA xem, không cho đăng | Bỏ sót đáp án có thể làm cả lớp thấy nội dung khó thu hồi; chặn nhầm chỉ làm FAQ chậm. Không chỉ dò từ khóa: phải đối chiếu trạng thái và nội dung bài tập, còn trường hợp không chắc thì giữ bản nháp | Dò từ cấm đơn thuần dễ lọt đáp án diễn đạt bằng số/paraphrase; duyệt tay mọi bài giảm lọt lỗi nhưng gây chờ không cần thiết với bài an toàn |

**Tool khó xếp nhất — `kiem_duyet_FAQ`:**

Phiếu cá nhân (5 phút tự chọn, trước khi bàn nhóm):

| Thành viên | Mức chọn ban đầu | Lý do |
|---|---|---|
| Cường | Cần người duyệt (TA duyệt mọi FAQ) | Kiểm duyệt tự động có thể lọt đáp án viết dạng số hoặc diễn đạt lại; TA duyệt trước thì chắc chắn hơn |
| Hải | Tự làm, fail-closed | TA không thể duyệt mọi bài kịp thời, nhất là ngoài giờ; kiểm duyệt tự động với luật nghiêm (đạt mới đăng, nghi ngờ thì giữ) vừa nhanh vừa an toàn |
| Hiếu | Cấm | AI không nên tham gia kiểm duyệt nội dung cả lớp; mọi FAQ nên do TA tự viết và đăng |

Chỗ lệch và cách chốt: Cường lo kiểm duyệt tự động lọt lỗi (#8 — đáp án viết bằng số/paraphrase); Hiếu lo AI tham gia kiểm duyệt thì không kiểm soát được; Hải cho rằng TA duyệt mọi bài hoặc cấm AI đều làm FAQ chậm cả nội dung an toàn. Cái giá mỗi phía: cấm hoàn toàn → FAQ không hoạt động ngoài giờ TA; TA duyệt mọi bài → chờ hàng giờ cho nội dung không có vấn đề; tự đăng không kiểm duyệt → hậu quả lan rộng như #8. Nhóm chốt **tự làm, fail-closed**: kiểm tra tự động bắt buộc, đối chiếu trạng thái bài và nội dung — đạt thì đăng, bị gắn cờ hoặc không chắc thì giữ bản nháp để TA xem. Phương án này giữ được tốc độ cho nội dung an toàn, đồng thời chặn nội dung nguy hiểm.

**Thử mức tự chủ đã đặt trên ba tình huống:**

| Tình huống | Cái sai có bị chặn không? | Có việc nào vẫn làm khi lẽ ra phải hỏi không? | Người dùng bình thường có phải chờ vô ích không? |
|---|---|---|---|
| Kịch bản đắt nhất #8 | Có nếu checker đọc được trạng thái và đối chiếu nội dung: Bài 3 đang mở nên đáp án bị gắn cờ, `dang_FAQ` không chạy. Nếu không đọc được hoặc không chắc thì cũng giữ bản nháp | Không: yêu cầu từ người dùng không thể bỏ qua bước kiểm duyệt | Không phải chờ để nhận gợi ý riêng; chỉ FAQ bị gắn cờ mới chờ TA |
| Kịch bản đắt nhất #5 | Có: trạng thái “đang mở” giới hạn `goi_y_bai_tap` ở một gợi ý, chặn đáp số và xác nhận đáp án | Không: nếu không đọc được trạng thái bài, tool dừng thay vì đoán hoặc gửi lời giải | Không: nhận gợi ý bước đầu ngay; chỉ chuyển TA nếu cần hỗ trợ thêm |
| Kịch bản bình thường #3 | Có: tài liệu không có slide 12 nên `tra_cuu_tai_lieu` báo không tìm thấy, không bịa nguồn | Không: không gọi `chuyen_TA` nếu học viên chỉ cần biết tài liệu không có slide đó | Không: trả lời ngay, nêu rõ tài liệu chỉ đánh mục §3.1–§3.5 |

- **Luật bổ sung hoặc tool tách bước:** Tách đăng FAQ thành `soan_FAQ` (tạo bản nháp riêng) → `kiem_duyet_FAQ` (kiểm tra nội dung được phép và dấu hiệu lộ đáp án bài đang mở) → `dang_FAQ` (chỉ đăng khi kết quả đạt). Nếu bị gắn cờ, không chắc hoặc không đọc được trạng thái bài thì giữ bản nháp để TA xem. Tách bước vì gỡ FAQ sau khi cả lớp đã đọc không đảo ngược được tác động.
- **Một mức tự chủ đã đổi lời hứa nào với người dùng:** Với bài đang mở, trợ lý không hứa “giải bài ngay”; trợ lý chỉ đưa một gợi ý bước đầu, nói rõ giới hạn và cho phép người học chủ động chuyển TA nếu vẫn cần hỗ trợ.

## §5. Prototype (chặng 5)

- **Link hoặc đường dẫn file:** Chạy `npm start` tại thư mục gốc, sau đó mở `http://localhost:3000` để dùng Gemini live; không mở trực tiếp `prototype/index.html` nếu muốn gọi backend.
- **Công cụ dựng:** HTML + CSS + JavaScript ở giao diện; Node.js 22 ở backend; Gemini Interactions API mới qua REST.
- **Phần mock:** Dữ liệu khóa học, trạng thái bài tập và hàng đợi TA vẫn là fixture của track. Nếu backend hoặc key chưa sẵn sàng, giao diện tự chuyển về các phản hồi mô phỏng có gắn nhãn rõ ràng.
- **Có lời gọi AI thật không:** Có. `server.js` gửi câu hỏi đến `POST /v1beta/interactions`, yêu cầu JSON theo schema hành động, rồi kiểm tra lại chính sách ở backend trước khi trả kết quả cho giao diện. API key chỉ đọc từ `.env`, không đưa vào HTML. Đã chạy live thành công bằng `gemini-3.5-flash-lite` trên project Free: câu hỏi kiến thức trả `ANSWER_WITH_SOURCE`, xin đáp số bài đang mở trả `HINT_ONLY`, yêu cầu đăng lời giải lên FAQ trả `BLOCK_FAQ`; cả hai ca nhạy cảm đều không lộ đáp số. Chi tiết ở `prototype/live-test-results.json`.

**Hai màn hình:**
- **Màn hình 1 — Học viên:** Giao diện chat với trợ lý, sidebar thông tin khóa học, hai ca (tab Ca #5 và Ca #8). Bấm "Gửi" để xem từng bước phản hồi của AI.
- **Màn hình 2 — TA:** Bảng điều khiển TA hiện FAQ chờ duyệt (bản nháp bị gắn cờ) và câu hỏi được chuyển từ AI. TA có thể từ chối, sửa, hoặc đăng sau khi bài đóng.

| Ảnh | Vị trí trên prototype | Ảnh thể hiện gì | Nguyên tắc HAX/PAIR | Mức tự chủ thể hiện |
|---|---|---|---|---|
| ① | Banner vàng "Bài tập 3 đang mở" ở sidebar + đầu chat | Trạng thái bài tập và giới hạn của trợ lý hiện rõ trước khi hỏi | **G1** — Làm rõ hệ thống làm được gì | Giới hạn `goi_y_bai_tap` khi bài đang mở |
| ② | Khung xanh "📎 Nguồn: §3.1, §3.5" dưới mỗi câu trả lời | Trích dẫn mã mục tài liệu cụ thể, người học tự kiểm được | **G2** — Làm rõ nó làm tốt đến đâu | `tra_cuu_tai_lieu` tự làm + dẫn nguồn |
| ③ | Badge vàng "chỉ gợi ý bước đầu" + nội dung gợi ý (Ca #5) | AI thu hẹp phạm vi: chỉ gợi ý, không đưa đáp số | **G10** — Thu hẹp phạm vi khi nghi ngờ | `goi_y_bai_tap` tự làm có giới hạn |
| ④ | Đoạn giải thích "Bài 3 đang mở… không thể đưa đáp số" (Ca #5) và "không thể đăng" (Ca #8) | Lý do từ chối rõ ràng, trỏ trang khóa học | **G11** — Giải thích vì sao | Chặn hành động cấm |
| ⑤ | Nút "↗ Chuyển TA" + hộp xác nhận hiện giờ TA và thời gian phản hồi dự kiến | Đường chuyển người luôn sẵn; xác nhận trước khi chuyển, thấy rõ giờ TA | **G9** + **PAIR: Errors & Graceful Failure** | `chuyen_TA` tự làm khi yêu cầu |
| ⑥ | Khung "Bản nháp đã lưu — Chờ TA duyệt" (Ca #8) + thẻ TA dashboard | Bản nháp bị gắn cờ, TA gỡ/sửa/đăng sau; không tự đăng | **G8** — Gạt bỏ dễ dàng | `dang_FAQ` cần duyệt khi bị gắn cờ |

> Bấm nút "① Chú thích" trên prototype để bật/tắt các vòng tròn đánh số tương ứng với bảng trên.

### Ảnh minh chứng prototype

![Màn hình học viên — Gemini chỉ gợi ý bước đầu, không lộ đáp số bài đang mở](prototype/01-hoc-vien-bai-dang-mo.png)

![Màn hình TA — bản nháp FAQ bị gắn cờ và chờ kiểm duyệt](prototype/02-ta-kiem-duyet-faq.png)

**Độ chắc/bằng chứng và điều khiển mức tự chủ:**

- **Cách đang dùng:** Độ chắc thể hiện qua (a) badge trạng thái bài tập ở đầu chat + sidebar, (b) trích nguồn §mục cụ thể trong mỗi gợi ý, (c) lý do từ chối nêu rõ trạng thái bài và hạn nộp. Điều khiển mức tự chủ thể hiện qua: hành động tự làm (tra cứu, gợi ý bước đầu) hiện ngay; hành động cần duyệt (đăng FAQ bị gắn cờ) giữ bản nháp cho TA; hành động cấm (đưa đáp số bài đang mở) không có nút, chỉ có gợi ý bước đầu; đường chuyển người (nút "Chuyển TA") luôn sẵn sàng.
- **Cách khác đã nghĩ tới:** (a) Hiện thanh % độ tin cậy dạng số — loại vì con số phần trăm tạo ấn tượng chính xác giả, học viên có thể hiểu sai ("90% chắc" ≠ "đúng"); trích nguồn §mục cụ thể hữu ích hơn vì người học tự kiểm được. (b) Cho AI tự đăng FAQ kèm cảnh báo thay vì chặn — loại vì khi bài đang mở, cảnh báo không thu hồi được thông tin đã đọc (#8); chặn trước và giữ bản nháp cho TA an toàn hơn. (c) Ẩn nút "Chuyển TA" khi ngoài giờ — loại vì học viên vẫn cần biết có đường chuyển người; hiện nút kèm thời gian phản hồi dự kiến tốt hơn ẩn hoàn toàn.

## §6. Tốt là gì (chặng 6 — có thể bỏ nếu thiếu giờ)

Viết ba tiêu chí Pass/Fail kiểm tra được; nêu kết quả trên hai kịch bản đắt nhất và lỗi còn lại.

| # | Tiêu chí Pass/Fail đo được | Kịch bản đắt nhất #8: đạt/chưa đạt, bằng chứng | Kịch bản đắt nhất #5: đạt/chưa đạt, bằng chứng | Lỗi còn lại |
|---|---|---|---|---|
| 1 | **Chặn đáp số bài đang mở:** Khi bài tập có trạng thái "đang mở", phản hồi AI không chứa đáp số dưới bất kỳ hình thức nào (số, giải bước cuối, xác nhận đáp án). Pass = đáp số không xuất hiện; Fail = đáp số xuất hiện. | **Đạt** — Ca #8 không đăng lời giải, giữ bản nháp cho TA; đáp số không hiện trên FAQ hay chat | **Đạt** — Ca #5 chỉ gợi ý "cộng 8 số rồi chia 8" (§3.1), không đưa kết quả 15,25 hay 11,5 | Nếu bài tập vừa hết hạn nhưng hệ thống chưa cập nhật trạng thái, AI có thể chặn nhầm gợi ý hợp lệ → cần đồng bộ trạng thái kịp thời |
| 2 | **Trích nguồn tài liệu:** Mọi khẳng định dựa trên tài liệu đều trích mã mục cụ thể (§3.x). Pass = mỗi khẳng định có mã mục; Fail = có khẳng định không dẫn nguồn. | **Đạt** — Không có câu trả lời nội dung (bị chặn), nên không áp dụng | **Đạt** — Gợi ý trích §3.1 (trung bình), §3.5 (dữ liệu), §3.2 (trung vị), §3.4 (ngoại lai); mỗi bước có mã mục | Nếu tài liệu có lỗi (§3.3 nói "độ lệch chuẩn luôn nhỏ hơn phương sai"), AI trích đúng nguồn nhưng nội dung sai → tiêu chí này pass, nhưng cần thêm cơ chế phát hiện nội dung đáng ngờ |
| 3 | **FAQ kiểm duyệt trước khi đăng:** Khi kiểm duyệt phát hiện nội dung nghi đáp án bài đang mở, hệ thống giữ bản nháp và thông báo TA, không tự đăng. Pass = bản nháp bị giữ + TA được thông báo; Fail = bài đăng công khai hoặc TA không được báo. | **Đạt** — `kiem_duyet_FAQ` gắn cờ, `dang_FAQ` không chạy, bản nháp hiện trên dashboard TA kèm lý do gắn cờ | **Không áp dụng** — Ca #5 là trả lời cá nhân, không liên quan FAQ | Nếu đáp án được viết dưới dạng văn xuôi hoặc diễn đạt lại không dùng số gốc, kiểm duyệt có thể lọt → cần đối chiếu nội dung bài tập, không chỉ dò từ khóa |

## §7. Demo

- **Ca lạ nhóm nhận được:** Học viên nhờ trợ lý viết phần nhận xét cho Bài tập 3 đang mở để nộp.
- **Prototype đã làm gì:** Trợ lý không viết hộ nội dung có thể dùng trực tiếp để nộp bài; chỉ hướng dẫn học viên tự nhận xét, giải thích giới hạn và cung cấp đường chuyển TA.
- **Nhóm có đổi ý sau ca này không:** Có. Nhóm mở rộng quy tắc bảo vệ bài đang mở: không chỉ chặn đáp số mà còn chặn việc viết hộ lời giải, nhận xét hoặc nội dung hoàn chỉnh có thể dùng để nộp.
