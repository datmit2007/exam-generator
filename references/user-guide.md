# Hướng dẫn sử dụng Exam Generator

## Chuẩn bị và tạo đề

Cung cấp tài liệu học phần dạng Markdown/text, PDF hoặc ảnh; kèm đề thi tham chiếu nếu có.

Nêu **môn học, giữa kỳ/cuối kỳ và mức khó**. Bạn có thể chỉ định thêm phạm vi, số câu, dạng câu, thời lượng và cách trả đáp án.

## Chọn độ khó

Chọn một mức từ **1–5**, bằng số hoặc tên mức. **Nếu chưa chọn độ khó, AI sẽ hỏi và chờ bạn trả lời trước khi tạo đề.** Trước khi tạo đề, AI sẽ hiệu chuẩn cả năm mức cho đúng học phần và tài liệu hiện tại rồi mới áp dụng mức bạn chọn. Mức được chọn mô tả độ khó tổng thể của đề; không có nghĩa mọi câu đều phải có đúng cùng mức khó.

| Mức | Có đề tham chiếu | Không có đề tham chiếu |
| --- | --- | --- |
| **1** | **Ngang mức tham chiếu:** Khối lượng và phân bố độ khó tương đương đề nguồn; không làm đề tổng thể dễ hơn. | **Mức chuẩn của kỳ thi:** Chủ yếu kiểm tra hiểu kiến thức và vận dụng vào tình huống quen thuộc, có một phần câu phân hóa. Sinh viên ôn tập đầy đủ có thể hoàn thành phần lớn đề trong thời gian quy định. |
| **2** | **Khó hơn một chút:** Tăng vừa phải câu cần hiểu bản chất, xét điều kiện hoặc thêm bước suy luận. | **Nhỉnh hơn mức chuẩn:** Tăng vừa phải câu cần giải thích bản chất, xét điều kiện hoặc vận dụng kiến thức vào tình huống có biến đổi; một số câu cần thêm bước suy luận. |
| **3** | **Khó hơn rõ rệt:** Nhiều câu kết hợp kiến thức, chọn phương pháp hoặc mô hình và phân biệt trường hợp. | **Khó rõ rệt:** Nhiều câu yêu cầu kết hợp các nội dung đã học, tự chọn phương pháp và phân biệt trường hợp; cần hiểu chắc và vận dụng linh hoạt. |
| **4** | **Khó hơn nhiều:** Phần lớn câu phân loại cao, cần tự tìm hướng giải hoặc xây dựng lập luận nhiều bước. | **Khó cao:** Phần lớn câu đòi hỏi tự tìm hướng giải, xử lý tình huống ít quen thuộc hoặc lập luận nhiều bước; sinh viên học tốt vẫn cần đầu tư đáng kể để hoàn thành. |
| **5** | **Khó hơn rất nhiều / chặn 10:** Hầu hết câu hướng tới phân loại nhóm học tốt nhất trong phạm vi, gồm các câu cần tổng hợp và suy luận sâu. | **Khó cao nhất / chặn 10:** Hầu hết câu hướng tới phân loại nhóm học tốt nhất; đòi hỏi tổng hợp, suy luận sâu và vận dụng sáng tạo trong phạm vi đã học. Sinh viên nắm chắc kiến thức vẫn khó đạt điểm tuyệt đối. |

Mọi mức đều giữ đúng phạm vi và cấu trúc đã chốt. Không tăng khó bằng diễn đạt mơ hồ hoặc chỉ kéo dài tính toán. Các mức không tương đương tuyệt đối giữa các học phần.

## Mẫu yêu cầu

- **Tạo đề:** “Dùng Exam Generator tạo đề cuối kỳ môn X từ tài liệu đính kèm, mức khó 3, thời gian 90 phút.”
- **Kiểm định:** “Kiểm định exam.md theo tài liệu nguồn và exam-context.md.”
- **Sửa đề:** “Sửa đề theo review\.md, giữ mức khó đã chọn.”
- **Xuất PDF:** “Xuất exam-final.md sang PDF, giữ nguyên nội dung.”

**Sau bước tạo đề, nên chuyển sang một cuộc trò chuyện mới để kiểm định**, mang theo `exam.md` và `exam-context.md`. AI sẽ đọc tài liệu nguồn theo đường dẫn trong context; chỉ cần cung cấp lại nếu không còn truy cập được. Bạn vẫn có thể tiếp tục trong cuộc trò chuyện hiện tại; AI không tự mở phiên mới.

Mỗi yêu cầu chỉ chạy bước được gọi. Đầu ra lần lượt là **exam.md + exam-context.md → review\.md → exam-final.md → exam.pdf**. Mặc định đáp án ngắn nằm cuối đề; bạn có thể yêu cầu tách riêng hoặc chỉ lấy đề.
