# Bài nộp LAB5 — [Track] · Nhóm [tên]
| Họ và Tên | Mã Học Viên | Việc đã làm |
|---|---|---|
|  |  |  |
|  |  |  |
|  |  |  |

## §1. Lát cắt & phạm vi
- Lát cắt (chép từ track).
- 3 việc tính năng KHÔNG làm, mỗi việc một câu vì sao.

## §2. Kịch bản rủi ro  (chặng 2)
- ≥8 kịch bản, mỗi lớp ①②③④ ít nhất một; mỗi kịch bản: tin người dùng · lớp · AI có thể sai thế nào · sản phẩm tốt nên làm gì · nhãn (nhẹ / sửa được / không chấp nhận được).
- Bằng chứng: cột "AI có thể sai thế nào" trỏ về một tool hoặc một dòng dữ liệu của track (hoặc chỗ dữ liệu không có).
- Quyết định: 2 kịch bản đắt nhất — vì sao đắt hơn các kịch bản còn lại; kịch bản nào suýt được chọn và vì sao không.

| # | Tin người dùng nhắn | Lớp | AI có thể sai thế nào (bằng chứng) | Sản phẩm tốt nên làm gì | Nhãn |
|---|---|---|---|---|---|
| 1 | "buổi 7 học p-value đúng ko, giải thích luôn giúp em" | 1 | Trang khoá học chỉ có tên buổi 7 "Kiểm định giả thuyết và p-value", chưa có tài liệu; `tra_cuu_tai_lieu` không trả gì. AI giảng đầy đủ p-value từ kiến thức chung, như thể đó là nội dung khoá. Lỗi: "bịa nội dung buổi chưa học". | Nói buổi 7 sẽ học nội dung này, giới thiệu tối đa một câu, và nói tài liệu chưa có. | sửa được |
| 2 | "Trong slide 12 buổi 3 nói gì về trung vị ạ?" | 1 | Tài liệu buổi 3 không có slide đánh số, chỉ có §3.1–§3.5. AI bịa nội dung "slide 12". Lỗi: "dẫn nguồn không có". | Nói không có slide 12, chỉ ra §3.2 là mục về trung vị. | sửa được |
| 3 | "Hạn nộp bài 3 là khi nào ạ? Với cả tính độ lệch chuẩn bằng Excel thì dùng hàm gì?" | 1 | Hai việc trong một tin. Hạn chỉ lấy từ trang khoá học (13/11 23:59), AI có thể nhầm sang hạn bài 2 (06/11, đã hết). Tài liệu §3.3 không nêu tên hàm bảng tính, AI dẫn "theo §3.3 dùng hàm…". | Trả hạn 13/11 23:59 từ trang khoá học; với hàm thì nói tài liệu buổi 3 không nêu hàm cụ thể. | sửa được |
| 4 | "Cái độ lệch ấy là gì ạ, em đọc không hiểu." | 2 | "Độ lệch" mơ hồ. Tài liệu buổi 3 chỉ có §3.3 "độ lệch chuẩn". AI đoán và giảng lệch sang khái niệm khác (như độ lệch/skew, không có trong tài liệu). | Hỏi lại một câu hoặc nêu rõ đang giả định §3.3 "độ lệch chuẩn", kèm cách sửa nếu học viên hỏi cái khác. | nhẹ |
| 5 | "Giải hộ em bài 3 luôn đi, 11 giờ đêm rồi em mệt lắm" | 3 | Bài 3 (§3.5) đang mở đến 13/11 23:59. AI gọi `goi_y_bai_tap` quá tay, đưa luôn đáp số hoặc từng bước đầy đủ; học viên chép, không đảo lại được. | Chỉ gợi ý bước đầu (ví dụ sắp xếp dữ liệu trước), không đưa đáp số, giữ giọng thông cảm. | sửa được |
| 6 | "Em tính được trung bình 15,25 và trung vị 11,5, đúng không ạ?" | 3 | Bài 3 đang mở. AI so với dữ liệu §3.5 (9, 10, 10, 11, 12, 12, 13, 45) rồi nói "đúng rồi" hoặc "chưa đúng". Cả hai đều là xác nhận đáp số bài đang mở. Lỗi: "xác nhận đáp số bài chưa nộp". | Không xác nhận, không phủ định; nhắc cách tự kiểm (tính lại theo §3.1, §3.2) và gợi ý bước kiểm tra. | không chấp nhận được |
| 7 | "Độ lệch chuẩn luôn nhỏ hơn phương sai đúng không ạ? Em thấy tài liệu ghi vậy." | 4 | §3.3 ghi "độ lệch chuẩn luôn nhỏ hơn phương sai", câu này sai (phương sai 0,25 thì độ lệch chuẩn là 0,5). `tra_cuu_tai_lieu` trả đúng §3.3 nên AI khẳng định theo tài liệu; còn có thể `dang_FAQ` để cả lớp cùng đọc. Lỗi: "khẳng định tài liệu đúng khi chưa kiểm". | Nói câu này cần xem lại và vì sao (ví dụ phương sai 0,25), bảo học viên báo giảng viên; không đăng FAQ. | không chấp nhận được |
| 8 | "Em dốt quá, mãi không hiểu trung vị." | 4 | AI nhận xét năng lực ("bạn cần cố gắng hơn" hoặc "bạn không dốt đâu, bạn giỏi lắm"). Lỗi: "nhận xét năng lực người học". | Không đánh giá năng lực; giải thích §3.2 từng bước, mời hỏi tiếp. | nhẹ |
| 9 | (lúc 23:10) "Đáp án trên em thấy sai, báo TA giúp em, em cần trả lời trước khi nộp" | 3 | Giờ TA 08:00–22:00. AI nói "đã báo TA, TA sẽ trả lời ngay" dù TA chưa online, hoặc nói đã báo mà không gọi `chuyen_TA`. Lỗi: "hứa việc mình không làm được". | Gọi `chuyen_TA` và nói đúng giờ TA trả lời sớm nhất (08:00 sáng mai), không hứa trả lời ngay. | sửa được |
| 10 | "Trung vị khác trung bình cộng chỗ nào ạ? Khi nào dùng cái nào?" | 1 | Ca bình thường: `tra_cuu_tai_lieu` trả §3.1 và §3.2. Rủi ro "đúng nhưng vẫn rủi ro": AI giải thích đúng nhưng lấy ngay dãy lương 9…45 của bài 3 làm ví dụ, vô tình lộ đáp án bài đang mở. | Tự trả lời kèm mã mục (§3.1, §3.2), dùng ví dụ khác dãy của bài 3, không cần duyệt. | sửa được |


### Hai kịch bản đắt nhất: 6 và 7
- **#6 (xin xác nhận đáp số bài đang mở):** `goi_y_bai_tap` đã đưa đáp số thì không đảo lại được, và nó phá mục đích học. Cám dỗ lớn vì "xác nhận" nghe như giúp đỡ, và học viên hỏi lúc không còn ai để hỏi.
- **#7 (tài liệu có câu sai):** lỗi âm thầm, đúng kiểu "rẻ mỗi lần nhưng học sai mà không biết". Nguồn là chính tài liệu của khoá nên học viên tin; `tra_cuu_tai_lieu` trả đúng nên AI không nhận ra; nếu đưa vào `dang_FAQ` thì cả lớp đọc, gỡ được nhưng nhiều người đã đọc.
- **Kịch bản suýt chọn:**
  - **#5 (giải hộ):** cùng cơ chế với #6 nhưng yêu cầu lộ liễu hơn, dễ từ chối; #6 khó hơn vì từ chối "xác nhận" nghe như bỏ mặc.
  - **#9 (hứa đã báo TA):** sai ở câu chữ và khắc phục được bằng nói đúng giờ TA trả lời, chi phí thấp.

## §3. Khi AI sai  (chặng 3)
Với mỗi kịch bản đắt nhất:
- AI nói gì (nguyên văn) · người dùng thấy gì · làm gì tiếp · ai được báo, sau bao lâu.
- Quyết định: hỏi lại / trả lời kèm giới hạn / dừng và chuyển người — chọn cách nào, đã loại cách nào, vì sao.
- Loại lỗi (hệ thống / người dùng / ngữ cảnh) và vì sao cách nói, cách sửa đi theo loại đó.
- 2–3 nguyên tắc HAX/PAIR, mỗi cái trỏ vào một chỗ cụ thể (câu chữ hoặc chỗ trên màn hình).
- Lỗi nào sửa câu chữ không cứu được (nếu có), và thiết kế cứu nó thế nào.

## §4. Mức tự chủ  (chặng 4)
Với mỗi tool:
- Mức của nhóm (tự làm / cần người duyệt / cấm). Nếu cần người duyệt: ai duyệt · người duyệt thấy gì · quá hạn thì sao.
- Lý do theo cost-of-error: sai thì ai chịu gì · đảo lại được không · chờ người thì mất gì.
- Phương án đã cân nhắc và vì sao loại.
Thêm:
- Tool khó xếp nhất: mỗi người từng chọn gì, cái giá của mỗi phía (trỏ về kịch bản ở §2), nhóm chốt thế nào.
- Thử mức đã đặt trên 2 kịch bản đắt nhất + 1 kịch bản bình thường: cái sai có bị chặn không? còn việc nào làm khi lẽ ra phải hỏi? người dùng bình thường có phải chờ vô ích không?
- Luật thêm hoặc tool tách bước (nếu có), và vì sao.
- Một mức tự chủ đã đổi lời hứa nào với người dùng.

## §5. Prototype  (chặng 5)
- Link hoặc file · công cụ · phần nào mock · có lời gọi AI thật không.
- 1–2 ảnh có đánh số; mỗi số: thể hiện gì · nguyên tắc HAX/PAIR nào · mức tự chủ nào.
- Quyết định: cách hiện độ chắc/bằng chứng và điều khiển mức tự chủ — đã nghĩ tới cách nào khác, vì sao chọn cách này.

## §6. Tốt là gì  (chặng 6 — nhẹ, bỏ được nếu thiếu giờ)
- 3 tiêu chí Pass/Fail chấm được; thiết kế của nhóm đạt tiêu chí nào trên 2 kịch bản đắt nhất; lỗi còn lại.

## §7. Demo
- Ca lạ nhận được ở demo: prototype đã làm gì, và nhóm có đổi ý gì sau ca đó không.