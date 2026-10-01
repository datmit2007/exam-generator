# Bước 4 — Chuyển nguyên bản Markdown sang PDF

## Giới hạn công việc

Chỉ dùng bản Markdown người dùng chỉ định làm chuẩn, cùng các tài nguyên hình và yêu cầu trình bày liên quan. Có thể xuất trực tiếp từ `exam.md` hoặc `exam-final.md`; không bắt buộc có báo cáo kiểm định. Nếu không rõ bản nào là bản chốt, xác định trước khi xuất.

Thông thường `exam-final.md` đã được bước sửa bỏ dòng `Mức khó yêu cầu`. Nếu người dùng chọn xuất trực tiếp bản đầu còn dòng này, giữ nguyên theo nguồn; không tự xóa tại bước PDF. Chỉ bỏ dòng khi người dùng yêu cầu rõ ràng.

Không đọc lại đề chính thức, giải bài, chấm đáp án, đánh giá phạm vi/độ khó hoặc viết lại câu hỏi. Giữ nguyên tiêu đề, chữ, dữ kiện, công thức, ký hiệu, câu/ý, ngữ liệu, code, thứ tự lựa chọn, điểm và đáp án. Nếu nguồn thiếu phần đáp án hoặc chỉ có đề, không tự tạo thêm.

Được chuyển cú pháp Markdown/toán sang định dạng tương đương và thay block mô tả hình bằng hình đúng mô tả. Được điều chỉnh phông, khoảng cách, dòng, cột và ngắt trang. Nghi vấn về nội dung phải báo riêng, không tự sửa. Nếu không thể chuyển trung thành vì dữ liệu/mô tả mơ hồ, nêu chính xác phần cần làm rõ.

## Công cụ và phông chữ

Ưu tiên dùng LuaLaTeX hoặc XeLaTeX để dàn trang và xuất PDF.

Môi trường phát triển chính của skill hiện sử dụng TeX Live 2026 tại `D:\texlive\2026`, với các executable:

- `D:\texlive\2026\bin\windows\lualatex.exe`
- `D:\texlive\2026\bin\windows\xelatex.exe`

Nếu các đường dẫn trên tồn tại và sử dụng được, ưu tiên bản cài này.

Nếu không tìm thấy, xác định công cụ theo thứ tự sau:

1. Tìm `lualatex` hoặc `xelatex` trong `PATH` của hệ thống.
2. Nếu chưa có, kiểm tra các bản TeX Live hoặc MiKTeX đã được cài trong môi trường hiện tại bằng đường dẫn, biến môi trường hoặc cơ chế phát hiện phần mềm phù hợp với hệ điều hành.
3. Nếu môi trường đã cung cấp một công cụ dựng tài liệu/PDF khác, chỉ sử dụng khi công cụ đó có thể bảo toàn đầy đủ nội dung Unicode, công thức toán, phông chữ, hình, bảng và bố cục với chất lượng tương đương yêu cầu của bước xuất.
4. Không tự cài TeX Live, MiKTeX, phông chữ hoặc phần mềm bổ sung chỉ để hoàn thành bước xuất, trừ khi người dùng yêu cầu rõ ràng.
5. Nếu không có công cụ phù hợp, giữ lại Markdown và các tệp trung gian có thể sử dụng được, báo rõ rằng chưa thể tạo PDF hoàn chỉnh và không tuyên bố đã xuất thành công.

Không coi đường dẫn `D:\texlive\2026` là yêu cầu bắt buộc đối với máy hoặc môi trường khác. Luôn kiểm tra công cụ thực tế trước khi sử dụng.

Với công việc tạo hoặc sửa tài liệu LaTeX độc lập trong môi trường có compiler tích hợp, có thể sử dụng compiler sẵn có nếu đáp ứng các yêu cầu tương đương. Phân biệt biên dịch xem trước với việc tạo file PDF cuối cùng có thể bàn giao.

Nếu dùng LaTeX, thiết lập `fontspec` và `unicode-math` khi tương thích:

- Văn bản: Times New Roman.
- Toán: New Computer Modern Math.
- Nhãn hình cùng phông tương ứng với văn bản/toán của đề.

Mã chương trình dùng phông đơn cách rõ ràng, giữ thụt lề và ký tự. Nếu hệ chữ của đề cần phông bổ sung, chọn phông hỗ trợ và thông báo lựa chọn; không để mất glyph. Thiếu phông mặc định hoặc công cụ xuất phải báo rõ, không âm thầm thay hoặc tự cài phần mềm.

Mặc định ưu tiên LaTeX cho việc dàn trang và dựng hình khi có một TeX engine phù hợp. Chỉ dùng công cụ khác khi công cụ đó đã có sẵn trong môi trường và có lợi ích rõ ràng về độ chính xác, khả năng dựng hình hoặc chất lượng trình bày mà không làm giảm tính trung thành với nguồn. Nếu chưa có căn cứ rõ ràng, tiếp tục dùng LaTeX. Tích hợp kết quả vào PDF sao cho nội dung trung thành với Markdown, phông chữ và cách trình bày nhất quán, chất lượng hiển thị rõ ràng. Nếu công cụ hiện có chưa đáp ứng yêu cầu đầu ra, giữ nguồn và nêu giới hạn, không tuyên bố đã có PDF hoàn chỉnh.

## Chuyển đổi và hình

- Dùng công cụ dựng hình chính xác phù hợp sơ đồ/đồ thị/cấu trúc, ưu tiên vector khi thích hợp. Dựng đúng nhãn, chiều, quan hệ, trục, tỷ lệ và số liệu trong block; không tự suy ra kết quả bài toán để bổ sung vào hình.
- Hình thay hoàn toàn block text trong PDF, tại câu hoặc nhóm câu tương ứng. Không thêm hình trang trí, đánh dấu đáp án hoặc bước giải.
- Giữ đúng dấu tiếng Việt, chỉ số, số mũ, vectơ, đơn vị, chữ Hy Lạp, phân số, căn, ma trận và các ký hiệu chuyên ngành. Công thức hóa học cần chữ đứng, chỉ số/điện tích đúng nguồn; ký hiệu code phải được bảo toàn. Không “chuẩn hóa” ký hiệu theo cách làm đổi ý nghĩa.
- Với bảng, giữ từng ô, tiêu đề hàng/cột, đơn vị và thứ tự; không đổi số liệu để vừa trang. Với câu ghép nối hoặc bảng đúng/sai, giữ quan hệ giữa nhãn và nội dung.

## Bố cục

Khổ A4, bố cục tối giản như đề thi thực tế. Không thêm trang bìa, logo, tên trường, ghi chú AI, thông tin lượt tạo hoặc lời hướng dẫn không có trong Markdown. Tiêu đề theo đúng nguồn, không tự sửa theo mẫu của bước tạo.

Với bốn lựa chọn ngắn, ưu tiên: cùng một dòng → hai cột hai hàng (A–B trên, C–D dưới) → mỗi lựa chọn một dòng. Chọn theo chiều rộng thực tế, kể cả công thức; với số lựa chọn khác, áp dụng nguyên tắc dễ đọc và đúng thứ tự. Không đổi thứ tự lựa chọn để vừa cột.

Giữ lời dẫn cùng phần đầu câu và các lựa chọn khi hợp lý. Câu/hình ngắn ưu tiên cùng trang. Câu tự luận hoặc ngữ liệu dài có thể tiếp trang ở chỗ tự nhiên, không thu nhỏ chữ quá mức để ép vừa. Không tự chèn khoảng trống làm bài dài nếu nguồn/yêu cầu không có.

Giữ công thức tự nhiên, tử/mẫu, căn và chỉ số không chạm nhau hoặc dòng bên cạnh. Với nội dung dài, đổi bố cục/ngắt dòng phù hợp trước khi thu nhỏ. Nhãn hình và chữ trong bảng phải đọc được và không ra ngoài lề.

Sau toàn bộ đề, phần đáp án đầu tiên bắt đầu ở trang mới nếu có. Giữ các phần BẢNG ĐÁP ÁN/GỢI Ý ĐÁP ÁN/LỜI GIẢI theo đúng nguồn và thứ tự, không tự thêm phần còn thiếu.

## Kiểm tra bản xuất và bàn giao

Render và quan sát từng trang của chính PDF đã xuất. Đối chiếu với Markdown về tính trung thành và trình bày, không kiểm định chuyên môn:

1. Đủ phần, câu/ý, ngữ liệu, lựa chọn, bảng/code và đáp án; đúng thứ tự, nhãn, số liệu và ký hiệu.
2. Mỗi block hình được thay bằng hình đúng mô tả tại đúng vị trí, không thêm hoặc mất dữ kiện.
3. Phông, dấu, công thức, khoảng cách, lề, ngắt trang và bảng không lỗi; không có chữ cắt, nhãn chồng hoặc dòng tràn.
4. Đáp án khớp nguồn, nằm sau toàn đề và bắt đầu trang mới; không có lời giải bị chèn vào phần câu hỏi.

Sửa lỗi chuyển đổi/dàn trang trong tệp trung gian rồi biên dịch và xem lại trang bị ảnh hưởng; nếu bố cục dồn trang thay đổi, kiểm tra cả các trang tiếp theo. Không sửa Markdown đầu vào. Nếu không render/quan sát được, nói rõ phần kiểm tra hình thức chưa thực hiện, không khẳng định đã kiểm tra đầy đủ.

Nếu xuất thành công, giao link `exam.pdf` cuối cùng. Giữ tệp trung gian trong folder riêng của lượt xuất để có thể sửa bố cục khi cần. Nếu không thể tạo PDF vì thiếu công cụ hoặc phụ thuộc cần thiết, giao các tệp nguồn/trung gian sử dụng được và nêu rõ giới hạn thay vì tạo một đầu ra thay thế kém trung thành.
