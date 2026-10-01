# Bước 3 — Sửa đề Markdown

## Đọc và xác minh

Đọc bản đề được chỉ định, báo cáo kiểm định hoặc phản hồi cụ thể của người dùng, context của lượt tạo nếu có và nguồn cần thiết để xác minh. Nếu có nhiều bản đề/báo cáo, đối chiếu số câu và nội dung để bảo đảm báo cáo áp dụng đúng bản; không sửa nhầm vì cùng số câu.

Nếu thiếu đề hoặc chưa biết cần sửa theo nhận xét nào, hỏi phần thiếu. Có thể sửa theo phản hồi trực tiếp của người dùng mà không cần một file review riêng. Khi thiếu nguồn chỉ ảnh hưởng đến một số nhận xét, xử lý phần đủ căn cứ và báo rõ phần phụ thuộc chưa làm được.

## Sửa có căn cứ

- Xác minh lại từng nhận xét, không sửa theo nhận xét sai hoặc chưa đủ chứng cứ. Giữ các câu tốt; chỉ chỉnh hoặc thay câu khi cần. Gợi ý tùy chọn chỉ áp dụng nếu cải thiện rõ và không làm thay đổi yêu cầu đã chốt.
- Giữ phạm vi, số câu/ý, cấu trúc, mức khó, dạng câu, điểm số và cách cung cấp đáp án của lượt tạo, trừ điều chỉnh được người dùng yêu cầu.
- Nếu thay câu, bảo toàn vai trò của nó trong phân bố chủ đề và khối lượng toàn đề. Tránh sửa thành câu dễ hơn chỉ để loại bỏ lỗi.
- Cập nhật đồng bộ lời dẫn, ngữ liệu chung, bảng/code, các lựa chọn, mô tả hình và đáp án. Câu dùng chung dữ kiện phải được kiểm tra cùng nhóm; đánh số lại phải cập nhật mọi tham chiếu liên quan.
- Với câu mở/tự luận, sửa cả ý chính và tiêu chí chấp nhận các cách trả lời hợp lệ. Với trắc nghiệm, xác nhận số lựa chọn đúng theo dạng câu thực tế.

## Rà soát và đầu ra

Sau khi sửa, giải/đánh giá lại toàn bộ đề, tập trung vào câu thay đổi và các phần phụ thuộc; đối chiếu với báo cáo để bảo đảm không sót lỗi đã xác minh. Kiểm tra lại độ bao phủ, mức khó và tính nguyên bản của câu thay thế.

Xuất `exam-final.md` hoàn chỉnh, gồm tiêu đề, mọi câu/ý và phần đáp án theo cấu hình lượt tạo. Xóa dòng bàn giao `Mức khó yêu cầu` dưới tiêu đề khỏi bản này, nhưng vẫn giữ đúng mức khó đó khi sửa; yêu cầu được lưu trong context hoặc báo cáo kiểm định để dùng lại. Không chỉ xuất các đoạn sửa. Hình vẫn là block mô tả text tại đúng câu, chưa dựng hình hay xuất PDF. Đọc lại chính file cuối để kiểm tra thứ tự và đồng bộ đáp án.

Giữ nguyên bản trước đó; nếu đã có bản final và cần sửa tiếp, dùng tên phiên bản rõ ràng hoặc cập nhật đúng file khi người dùng yêu cầu. Chỉ cập nhật `exam-context.md` khi các quyết định của lượt thực sự thay đổi; không thêm file cấu hình môn. Báo ngắn những nhận xét bị bác hoặc phần chưa xử lý vì thiếu căn cứ, nếu có, ngoài file đề.
