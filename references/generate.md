# Bước 1 — Tạo đề Markdown

Đọc sources.md trước. Tạo đề thi tham khảo giữa kỳ hoặc cuối kỳ cho học phần được yêu cầu; hình thức, số câu và khối lượng theo đề chính thức hoặc căn cứ thay thế đã xác định. Không giới hạn ở một môn, trắc nghiệm hay một số câu cố định.

## 1. Chốt thiết kế của lượt tạo

Xác định tên học phần, kỳ thi, phạm vi, cấu trúc phần/câu/ý, thời lượng và điểm nếu có, dạng đáp án, mức khó, quy ước và công cụ thí sinh được dùng. Lập phân bố chủ đề, kiểu suy luận và khối lượng trước khi viết. Phân bố tự nhiên theo mức độ quan trọng trong nguồn; không ép mỗi chương có số câu bằng nhau.

Với đề đọc hiểu/tình huống/lập trình, tính cả độ dài ngữ liệu, dữ liệu và phần trả lời. Nếu dạng đánh giá cần âm thanh, dụng cụ thực nghiệm hoặc thao tác ngoài văn bản, không âm thầm biến thành câu hỏi lý thuyết; xác định có thể mô phỏng hợp lệ bằng dữ liệu text hay cần người dùng bổ sung tài nguyên/yêu cầu chuyển dạng.

Không hỏi lại các quyết định đã có đủ căn cứ. Lưu thiết kế ngắn vào `exam-context.md`; không chèn bản phân tích nguồn vào phần đề.

## 2. Độ khó

Chọn độ khó theo yêu cầu người dùng, bằng số từ **1–5** hoặc mô tả tương ứng. Dùng lại lựa chọn đã chốt cho lượt tạo; không hỏi lại khi đã rõ. Nếu người dùng chưa chọn độ khó, hỏi họ chọn mức 1–5 trước khi tạo đề và chờ câu trả lời; không tự áp dụng mức mặc định. Nếu mô tả chưa đủ rõ để xác định mức, hỏi làm rõ. Có thể tiếp tục đọc và phân tích nguồn trong khi chờ.

| Mức | Khi có đề tham chiếu | Khi không có đề tham chiếu |
|---|---|---|
| **1** | **Ngang mức tham chiếu:** Khối lượng và phân bố độ khó tương đương nguồn; không làm đề tổng thể dễ hơn | **Mức chuẩn của kỳ thi:** Chủ yếu kiểm tra hiểu kiến thức và vận dụng vào tình huống quen thuộc; có một phần câu phân hóa. Sinh viên ôn tập đầy đủ có thể hoàn thành phần lớn đề trong thời gian quy định |
| **2** | **Khó hơn một chút:** Tăng vừa phải câu cần hiểu bản chất, xét điều kiện hoặc thêm bước suy luận | **Nhỉnh hơn mức chuẩn:** Tăng vừa phải câu cần giải thích bản chất, xét điều kiện hoặc vận dụng kiến thức vào tình huống có biến đổi; một số câu cần thêm bước suy luận |
| **3** | **Khó hơn rõ rệt:** Nhiều câu kết hợp kiến thức, chọn phương pháp/mô hình và phân biệt trường hợp | **Khó rõ rệt:** Nhiều câu yêu cầu kết hợp các nội dung đã học, tự chọn phương pháp và phân biệt trường hợp; sinh viên cần hiểu chắc và vận dụng linh hoạt |
| **4** | **Khó hơn nhiều:** Phần lớn câu phân loại cao, cần tự tìm hướng giải hoặc xây dựng lập luận nhiều bước | **Khó cao:** Phần lớn câu đòi hỏi tự tìm hướng giải, xử lý tình huống ít quen thuộc hoặc xây dựng lập luận nhiều bước; sinh viên học tốt vẫn cần đầu tư đáng kể để hoàn thành |
| **5** | **Khó hơn rất nhiều / chặn 10:** Hầu hết câu hướng tới phân loại nhóm học tốt nhất trong phạm vi, gồm các câu đòi hỏi tổng hợp và suy luận sâu | **Khó cao nhất / chặn 10:** Hầu hết câu hướng tới phân loại nhóm học tốt nhất; đòi hỏi tổng hợp, suy luận sâu và vận dụng sáng tạo trong phạm vi đã học. Sinh viên nắm chắc kiến thức vẫn khó đạt điểm tuyệt đối |

**Khi có đề tham chiếu:** Lấy đề tham chiếu đã chọn làm mốc và áp dụng mức độ khó 1–5 theo cột tương ứng. Ở mức 1, giữ khối lượng và phân bố độ khó tương đương đề tham chiếu; ở mức 2–5, tăng yêu cầu tư duy theo mức đã chọn. Không có mức dễ hơn đề tham chiếu trong thang này.

**Khi không có đề tham chiếu:** Xác định mức 1 là mức chuẩn của một kỳ thi giữa kỳ hoặc cuối kỳ, dựa trên mục tiêu học phần, phạm vi kiến thức, tài liệu, bài tập và thời lượng đã xác định. Đề phù hợp để sinh viên ôn tập đầy đủ, hiểu kiến thức và vận dụng được các nội dung cơ bản có thể hoàn thành phần lớn trong thời gian quy định, đồng thời vẫn có câu phân hóa. Mức 2–5 tăng yêu cầu tư duy từ nền này theo cột tương ứng. Ghi căn cứ thiết kế vào `exam-context.md`; không khẳng định mức chuẩn dự kiến tương đương đề thi thực tế khi chưa có bằng chứng.

Trong cả hai trường hợp, tự lựa chọn cách thiết kế câu hỏi phù hợp học phần và mức khó đã chọn, giữ đúng phạm vi và cấu trúc đã xác định. Không tăng khó bằng diễn đạt mơ hồ hoặc chỉ kéo dài tính toán. Các mức không tương đương tuyệt đối giữa các học phần; mức 1 của một đề tham chiếu vốn rất khó có thể khó hơn mức cao hơn của học phần khác.

## 3. Câu hỏi và tính nguyên bản

Dựa trên phạm vi đã chốt từ tài liệu và đề mẫu, chủ động vận dụng khả năng suy luận, kiến thức nền và hiểu biết chuyên môn của học phần để thiết kế câu hỏi mới. Không giới hạn ý tưởng vào ví dụ hay dạng bài đã xuất hiện trong tài liệu; giữ đúng phạm vi, cấu trúc và mức khó đã xác định. Với kiến thức quá chuyên sâu hoặc chưa chắc chắn, chủ động tham khảo nguồn uy tín trên internet khi cần để bảo đảm tính chính xác.

- Tạo câu mới về góc hỏi, quan hệ cần suy luận, dữ liệu hoặc cách kết hợp kiến thức. Không sao chép câu nguồn rồi chỉ đổi số, đối tượng, chất hoặc tên nhân vật. Các kỹ thuật giải cơ bản vẫn có thể lặp giữa nhiều bài, nhưng không giữ nguyên bộ khung một câu cụ thể dưới lớp diễn đạt mới.
- Giữ thuật ngữ, mức hình thức hóa, cách hỏi và độ dài phù hợp học phần. Nêu rõ dữ kiện, giả thiết, mô hình, quy ước và kết quả cần tìm khi chúng quyết định cách hiểu.
- Trắc nghiệm một đáp án: số lựa chọn theo thiết kế; đúng một lựa chọn đúng trong điều kiện đã cho. Trắc nghiệm nhiều đáp án/đúng-sai: hướng dẫn rõ thao tác trả lời và biểu diễn đáp án theo dạng đó, không ép về một chữ cái.
- Phương án nhiễu xuất phát từ lỗi hiểu hoặc lỗi lập luận thực tế. Tránh lựa chọn vô lý, trùng nghĩa, chứa nhau ngoài chủ ý, hoặc để đáp án lộ qua độ dài, ký hiệu, văn phong, độ chính xác số liệu. Không ép phân bố chữ cái cân bằng bằng cách làm hỏng câu.
- Tự luận/tính toán/chứng minh: xác định rõ sản phẩm cần nộp và độ sâu mong muốn. Với câu mở, có thể có nhiều cách trả lời hợp lệ; tiêu chí đánh giá phải cho phép chúng. Không dùng yêu cầu “một đáp án đúng duy nhất” cho bài nghị luận hoặc phân tích mở.
- Đề hỗn hợp: giữ số phần, tỷ lệ dạng câu, điểm và quy tắc chọn câu theo thiết kế. Kiểm tra tổng điểm khi có thang điểm và số câu thí sinh phải làm khi có lựa chọn.
- Ngữ liệu/tình huống/dữ liệu dùng chung phải đủ để làm các câu; không để câu trước vô tình tiết lộ câu sau. Nếu dữ liệu được giả lập, diễn đạt phù hợp, không gán nguồn hoặc sự kiện thật chưa xác minh. Với yêu cầu dựa trên trích đoạn cụ thể, dùng nguồn được phép và không bịa trích dẫn.
- Bài lập trình/thuật toán cần rõ đầu vào, đầu ra, ràng buộc và môi trường nếu ảnh hưởng đến lời giải. Ví dụ minh họa không được vô tình thay toàn bộ công việc cần làm của thí sinh.

## 4. Hình, bảng và nội dung có cấu trúc

Bảng dữ liệu và mã chương trình được viết trực tiếp bằng Markdown/text. Công thức dùng ký hiệu nhất quán, ưu tiên cú pháp toán tương thích Markdown; chưa tạo tài liệu LaTeX.

Nếu thông tin trong câu hỏi đã rõ ràng, đủ để làm bài và dạng câu không yêu cầu đọc hình thì không thêm hình. Với dạng câu cần đọc hình như trong nguồn, không thay toàn bộ hình bằng mô tả chữ. Mật độ và phân bố các câu cần đọc hình để có đủ thông tin làm bài phải tương đương với nguồn.

Chỉ yêu cầu hình khi cần xác định cấu hình hoặc truyền tải dữ liệu. Đặt mô tả ngay sau lời dẫn của câu hoặc trước nhóm câu cùng sử dụng hình:

```text
[MÔ TẢ HÌNH – CÂU <số câu hoặc nhóm câu>]
- Đối tượng và nhãn cần thể hiện: ...
- Bố trí, chiều, cấu trúc, quan hệ hoặc trục/tỷ lệ: ...
- Dữ liệu, ký hiệu và đơn vị cần ghi: ...
- Quy ước thể hiện cần thiết, nếu có: ...
[/MÔ TẢ HÌNH]
```

Mô tả phải đủ để người dàn trang dựng hình mà không phải giải bài hoặc tự chọn mô hình. Với đồ thị, xác định miền, trục, các điểm/đường và tỷ lệ khi chúng ảnh hưởng đến đáp án. Không ghi kết quả cần tìm, đường phụ của lời giải hay dấu hiệu nhận diện đáp án đúng. Không tạo file hình trong bước này.

## 5. Tự rà soát và đầu ra

Giải/đánh giá lại từng câu trước khi xuất. Kiểm tra dữ kiện, quy ước, tính hợp lệ của đáp án, đơn vị, ký hiệu và độ chính xác; áp dụng các kiểm tra chuyên môn phù hợp với môn thực tế. Với câu mở, thử tiêu chí trên hơn một cách trả lời có thể hợp lệ. Kiểm tra lời dẫn, bảng, code, mô tả hình và các lựa chọn khớp nhau.

Rà toàn đề về phạm vi, khối lượng, mức khó, độ bao phủ, trùng lặp và tính nguyên bản. Sửa câu có vấn đề trước khi hoàn tất. Không coi việc tự kiểm tra là bằng chứng đề không thể có lỗi.

Xuất `exam.md` theo tiêu đề quy định trong SKILL.md. Ngay dưới tiêu đề, ghi `Mức khó yêu cầu: <số mức 1–5 và tên mức theo cột áp dụng>` theo lựa chọn đã chốt của người dùng. Dòng này giúp phiên kiểm định đọc được yêu cầu ngay trong file đề và sẽ được xóa ở bước sửa; ghi cùng mức khó và trường hợp có/không có đề tham chiếu trong `exam-context.md`.

Phần câu hỏi không chứa lời giải, đánh dấu đáp án đúng, nguồn của từng câu hay ghi chú cho người tạo đề. Hướng dẫn chọn câu/chọn nhiều đáp án và ngữ liệu cần làm bài được phép xuất hiện.

Sau toàn bộ câu hỏi, mặc định thêm **BẢNG ĐÁP ÁN** cho phần khách quan: số câu/ý và đáp án tương ứng. Với tự luận hoặc câu mở, thêm **GỢI Ý ĐÁP ÁN** ngắn: kết quả/ý chính/tiêu chí chấp nhận, điểm theo ý nếu thang điểm đã xác định; không tự thêm lời giải dài. Đề hỗn hợp dùng cả hai phần khi cần. Nếu người dùng yêu cầu chỉ có đề, tách đáp án hoặc lời giải chi tiết, làm đúng yêu cầu đó.

Đọc lại file đã xuất để đối chiếu số câu, các phần và đáp án với bản rà soát. `exam-context.md` phải đủ ngắn để phiên B đọc nhanh, gồm:

- Yêu cầu thực tế: học phần, kỳ thi, ngôn ngữ, phạm vi, cấu trúc, độ khó và mốc so sánh, thời lượng/điểm/công cụ nếu đã biết.
- Các nguồn đã dùng: đường dẫn tuyệt đối đến file/folder khi có, hoặc tên/định danh tệp đính kèm; vai trò, bản chính được chọn, phạm vi đã đọc và lý do chọn nếu có khác biệt. Không bịa đường dẫn cho tệp đính kèm. Nếu biết nguồn có thể thay đổi, ghi phiên bản/kỳ thi của nguồn đã sử dụng.
- Căn cứ hoặc giả định khi thiếu đề chính thức; điểm còn chưa xác minh và thay đổi do người dùng chỉ định.
- Tên file đề, cách cung cấp đáp án và các yêu cầu trình bày đặc biệt của lượt này.

Nếu tạo nhiều đề, ghi chung bối cảnh khi phù hợp nhưng đặt tên riêng rõ ràng; mỗi đề đáp ứng cấu trúc và mức khó, tránh chỉ hoán đổi câu hoặc thay số giữa các đề trừ khi người dùng muốn các mã đề tương đương.
