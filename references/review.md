# Bước 2 — Kiểm định Markdown/text

## Đầu vào và phạm vi

Đọc toàn bộ đề cần kiểm định, `exam-context.md` nếu có, yêu cầu hiện tại, các nguồn đã chọn và tài liệu bổ trợ liên quan theo sources.md. Có thể đọc đáp án ngay; không yêu cầu che đáp án hoặc thêm phiên mới.

Đọc dòng `Mức khó yêu cầu` ngay dưới tiêu đề bản đề đầu để xác định mục tiêu kiểm định; đây là ghi chú bàn giao tạm, không phải lỗi trình bày của đề. Đối chiếu với context nếu có; yêu cầu mới rõ ràng của người dùng được ưu tiên. Nếu dòng này và context mâu thuẫn mà chưa rõ bản nào mới hơn, hỏi lại. Nếu không có thông tin mức khó ở bất kỳ đầu vào nào, không tự áp mặc định của bước tạo; vẫn kiểm tra nội dung và hỏi mức khó khi cần kết luận đạt yêu cầu. Ghi mức khó đã dùng để đánh giá vào phần tổng quan của báo cáo.

Nếu `exam-context.md` có thang hiệu chuẩn 1–5, dùng chính thang đó làm chuẩn đánh giá và không tự tạo một cách hiểu mới về các mức. Nếu context không có thang nhưng đủ nguồn để đánh giá độ khó, tái dựng thang theo nguyên tắc trong generate.md trước khi kết luận đề có đạt mức mục tiêu hay không.

Nếu người dùng giao đề có sẵn không có context, khôi phục yêu cầu từ prompt và nguồn; không bắt buộc chạy lại bước tạo. Đề cần kiểm định là đầu vào bắt buộc. Khi thiếu nguồn, vẫn kiểm tra được nội dung nội tại nhưng phải phân biệt phần chưa đủ căn cứ kết luận về phạm vi, phong cách hoặc độ khó so với chuẩn.

## Cách kiểm định

Tự giải hoặc đánh giá từng câu với các điều kiện thực tế; không mặc định đáp án có sẵn là đúng. Trọng tâm bao gồm chất lượng ra đề, phạm vi, tính mới và độ khó, không chỉ so bảng đáp án. Nếu gặp nội dung chuyên sâu chưa chắc chắn, chủ động xác minh bằng nguồn uy tín trên internet.

- Kiểm tra đủ dữ kiện, mô hình/quy ước, ký hiệu, đơn vị, độ chính xác, ngữ liệu, bảng/code và mô tả hình. Câu phải làm được với kiến thức/công cụ được phép.
- Với trắc nghiệm: kiểm tra từng lựa chọn, số đáp án đúng theo dạng câu, chất lượng phương án nhiễu và dấu hiệu vô tình lộ đáp án.
- Với tự luận/câu mở: kiểm tra độ rõ của yêu cầu, tiêu chí/ý đáp án, cách trả lời thay thế hợp lệ và điểm nếu có. Không bác đáp án chỉ vì nó khác cách giải dự kiến.
- Kiểm tra thực chất mức khó: đòi hỏi suy luận gì, có vượt phạm vi không, có chỉ tăng độ dài tính toán hay đánh đố câu chữ không. Đánh giá từng câu hoặc nhóm câu theo thang đã hiệu chuẩn, xét độ sâu suy luận, mức tự lựa chọn phương pháp, mức kết hợp kiến thức, độ mới của tình huống và xử lý điều kiện/trường hợp; không coi việc tăng tải tính toán đơn thuần là tăng mức tương ứng. Đánh giá tương đối với mốc đã ghi trong context; không áp chuẩn ngang đề gốc khi người dùng đã chọn chặn 10.
- Đánh giá phạm vi theo kiến thức và kỹ năng thực sự cần để giải, không theo việc câu hỏi, bối cảnh hoặc dạng bài đã xuất hiện trong slides/đề mẫu hay chưa. Chấp nhận câu mới khai thác kiến thức trong phạm vi; nếu có kiến thức bổ sung ngoài phạm vi, kiểm tra đề đã cung cấp đủ để suy luận và trọng tâm đánh giá vẫn thuộc học phần/phạm vi đã chốt.
- Đối chiếu tính nguyên bản với nguồn đã đọc; chỉ ra câu nguồn cụ thể khi nhận xét về trùng lặp. Không tuyên bố mới so với mọi đề từng tồn tại.
- Xem toàn đề về số phần/câu/ý, khối lượng đọc và viết, chủ đề, kiểu suy luận, điểm số, câu tùy chọn, phụ thuộc giữa câu, phân bố độ khó thực tế so với profile mục tiêu và thời gian nếu biết.

Chủ động xem xét vấn đề khác phát sinh từ môn/dạng đề thực tế. Danh sách trên không giới hạn phạm vi kiểm định. Chỉ nêu nhận xét có căn cứ; không tạo lỗi hoặc đề xuất thay đổi cho đủ số lượng. Phân biệt lỗi cần sửa, đề xuất cải thiện và điểm chưa xác minh. Phần đạt yêu cầu được ghi nhận ngắn gọn.

## Đầu ra

Xuất `review.md`, gồm:

1. Tổng quan, phiên bản/file đề đang kiểm định và các giới hạn nguồn còn có ảnh hưởng.
2. Nhận xét theo từng câu/ý/nhóm ngữ liệu, kể cả mô tả hình. Câu đạt ghi ngắn; câu có vấn đề nêu vị trí, căn cứ, ảnh hưởng và hướng xử lý. Không cần chép lại đề hoặc lời giải dài.
3. Đánh giá toàn đề về cấu trúc, bao phủ, độ khó, thời lượng nếu có, tính nguyên bản và đáp án.
4. Danh sách ưu tiên: lỗi làm câu không hợp lệ hoặc ngoài phạm vi trước, rồi vấn đề chất lượng, sau đó gợi ý tùy chọn.

Chỉ phân tích và viết báo cáo. Không sửa file đề, không xuất đề thay thế, không dựng hình hoặc PDF. Không đánh dấu toàn đề “đạt” khi vẫn còn phần quan trọng chưa kiểm tra.
