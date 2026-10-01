---
name: exam-generator
description: Tạo đề thi tham khảo giữa kỳ hoặc cuối kỳ cho nhiều học phần từ đề thi và tài liệu Markdown/text, PDF hoặc ảnh; kiểm định, sửa đề, hoặc chuyển bản đề đã chốt sang PDF theo từng yêu cầu riêng. Dùng khi người dùng muốn luyện thi với độ khó từ ngang mức tham chiếu đến khó hơn rất nhiều, hỗ trợ trắc nghiệm, tự luận và đề hỗn hợp.
---

# Exam Generator

Tạo và hoàn thiện đề tham khảo theo tài liệu của học phần, không yêu cầu file cấu hình riêng cho từng môn. Hướng dẫn và tên file của skill dùng chung cho mọi môn; ngôn ngữ đề theo yêu cầu hoặc tài liệu học phần, mặc định tiếng Việt nếu không rõ.

[Hướng dẫn sử dụng](references/user-guide.md): tài liệu cho người dùng về cách chuẩn bị đầu vào, chọn độ khó và gọi từng bước.

## Chọn bước

| Yêu cầu | Tài liệu cần đọc | Đầu ra chính |
|---|---|---|
| Tạo đề | [sources.md](references/sources.md), [generate.md](references/generate.md) | `exam.md` và `exam-context.md` |
| Kiểm định | [sources.md](references/sources.md), [review.md](references/review.md); tra generate.md khi cần tiêu chí | `review.md` |
| Sửa đề | [revise.md](references/revise.md); tra sources.md/generate.md khi cần xác minh | `exam-final.md` |
| Xuất PDF | Chỉ [export-pdf.md](references/export-pdf.md) | `exam.pdf` |

- Mỗi prompt chỉ làm bước được gọi, không tự chạy các bước tiếp theo. Nếu người dùng chỉ nói “dùng skill” mà chưa rõ công việc, hỏi bước cần làm.
- Workflow dự kiến: phiên A tạo đề; phiên B nhận file và lần lượt kiểm định, sửa, xuất PDF bằng ba prompt riêng. Không tự mở chat, gọi subagent hoặc bắt buộc thêm phiên kiểm định. Phiên B được đọc đáp án ngay.
- Ba bước đầu (tạo đề, kiểm định, sửa đề) chỉ tạo đầu ra dạng Markdown/text; chưa dựng hình, dàn LaTeX hay xuất PDF. Vẫn đọc và phân tích tài liệu đầu vào ở dạng Markdown/text, PDF hoặc ảnh đính kèm, bao gồm chữ, công thức, bảng, đồ thị và hình minh họa. Không yêu cầu người dùng cung cấp bản text nếu có thể đọc trực tiếp nguồn. Chỉ yêu cầu bổ sung hoặc làm rõ khi nội dung cần thiết không đọc được hoặc còn mơ hồ; không tự đoán dữ kiện. Hình cần có trong đề được ghi bằng mô tả text để dựng ở bước xuất PDF.
- Bước PDF chuyển nguyên nội dung đã chốt; không giải bài, đánh giá độ khó hay sửa nội dung chuyên môn.

## Nhận đầu vào

Nếu nguồn có ảnh riêng hoặc ảnh được nhúng/liên kết trong Markdown, phải mở và xem trực tiếp toàn bộ ảnh học thuật liên quan trước khi tạo đề; đường dẫn tương đối tính từ thư mục chứa file Markdown. Không dùng văn bản, chú thích hay OCR để thay thế việc xem ảnh. Nếu ảnh không đọc được, báo rõ và hỏi khi cần; không tự bỏ qua rồi giao đề chỉ dựa trên phần chữ.

Từ prompt và ngữ cảnh đang có, xác định môn học, giữa kỳ/cuối kỳ, bước cần làm, độ khó, nguồn và nơi lưu nếu được chỉ định. Khi tạo đề, dùng mức khó 1–5 theo yêu cầu người dùng và bảng trong generate.md; nếu chưa có lựa chọn thì hỏi và chờ người dùng chọn trước khi tạo đề, không tự áp dụng mức mặc định. Người dùng có thể ghi đè số câu, dạng câu, thời lượng, phạm vi, cách trả đáp án hoặc yêu cầu nhiều đề cho một lượt. Không bắt họ điền biểu mẫu hay nhập lại thông tin đã có.

Sử dụng các file, thư mục hoặc đường dẫn người dùng cung cấp cho lượt làm việc. Không tự tìm thư mục đề thi theo cấu trúc cố định hoặc dò nguồn khác trong workspace. Nếu chưa có tài liệu nguồn, yêu cầu người dùng cung cấp trước khi tạo đề. Các bước tiếp theo có thể dùng lại nguồn đã được giao cho cùng lượt tạo; không yêu cầu người dùng thả lại khi vẫn truy cập được. Không tự tạo hay sửa thư mục tài liệu môn.

Ưu tiên yêu cầu hiện tại của người dùng, rồi yêu cầu đã chốt cho lượt đang làm, rồi bằng chứng từ tài liệu. Không mang mặc định của môn này sang môn khác. Nếu yêu cầu chủ ý khác đề chính thức, ghi nhận đó là điều chỉnh của lượt tạo. Nếu các yêu cầu không thể đồng thời đáp ứng, hỏi đúng điểm mâu thuẫn.

## Hợp đồng đầu ra

- Tiêu đề đề chỉ gồm `ĐỀ THI THAM KHẢO GIỮA KỲ <TÊN HỌC PHẦN>` hoặc `ĐỀ THI THAM KHẢO CUỐI KỲ <TÊN HỌC PHẦN>`. Không tự thêm mã môn, trường, năm học, mã đề, mức khó, lời giới thiệu hay tuyên bố kiểm định. Yêu cầu rõ ràng của người dùng có thể thay đổi mẫu này.
- Riêng bản đầu `exam.md`, đặt dòng `Mức khó yêu cầu: <mức khó áp dụng>` ngay dưới tiêu đề để phiên kiểm định nhận biết; bước sửa xóa dòng này khỏi `exam-final.md`. Đây là thông tin bàn giao tạm, không phải một phần tiêu đề.
- Sau dòng mức khó tạm thời (nếu có) là hướng dẫn làm bài thực sự cần thiết, các phần/câu theo cấu trúc đã xác định, rồi phần đáp án theo generate.md. Không thêm ghi chú quy trình hoặc căn cứ chọn cấu trúc khác vào đề.
- `exam-context.md` là bản bàn giao ngắn của một lượt tạo, không phải cấu hình môn. Nó lưu các quyết định và nguồn cho phiên B; người dùng không cần viết file này.
- Lưu đầu ra vào nơi người dùng chỉ định. Nếu chưa có, dùng folder output của chat nếu có; nếu không thì `outputs/exams/<môn>/<midterm-hoặc-final>/<lượt>/` trong workspace được phép ghi. Mỗi lượt có folder riêng; không ghi vào nguồn hay ghi đè kết quả của lượt khác.
- Ở mỗi bước, gửi link đầu ra và thông báo ngắn những giới hạn còn ảnh hưởng đến kết quả. Giữ ghi chú kỹ thuật và tệp biên dịch phụ ngoài phần đề.
