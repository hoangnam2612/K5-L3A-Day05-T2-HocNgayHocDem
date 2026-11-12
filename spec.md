# Bài nộp LAB5 — T2 Giáo dục · Nhóm Học Ngày Học Đêm
| Họ và Tên | Mã Học Viên | Việc đã làm |
|---|---|---|
| Hoàng Hải Nam | 2A202603694 | Từ chặng 1, cùng thảo luận với team, nghiên cứu và đưa ra những kịch bản ở chặng 2 |
| Lê Hữu Toàn  | 2A202603660 |  |
| Lê Hoàng Sơn | 2A202603662 |  |
| Phạm Thanh Tùng| 2A202603695 |  |


## §1. Lát cắt & phạm vi

### Lát cắt

Trong **trợ lý học bài của trang khóa học** (kiểu ChatGPT Study mode), khi **học viên** đang hỏi bài vào **tối muộn**, lúc không còn ai để hỏi, AI quyết định **giảng kèm, trích tài liệu, hỏi lại cho rõ, gợi ý từng bước, hoặc nói thẳng “tài liệu không có” và đề xuất chuyển câu hỏi cho TA**; kết quả là học viên hiểu đúng bài mình đang học, không chép đáp án và không học sai mà không biết.

### Phạm vi thiết kế

- Khóa học giả định: **Nhập môn phân tích dữ liệu**, học viên đang học buổi 3 — *Thống kê mô tả*.
- AI chỉ được dựa vào tài liệu buổi 3 và thông tin trên trang khóa học: lịch học, hạn và trạng thái bài tập, giờ TA.
- Các hành động có thể dùng là tra cứu tài liệu, gợi ý bài tập, soạn yêu cầu chuyển TA và đề xuất đăng FAQ; mức tự chủ sẽ được quyết định ở §4.

### Ba việc tính năng không làm

1. **Không giải hộ, đưa đáp án hoặc xác nhận đáp số Bài tập 3 đang mở.** AI chỉ gợi ý bước đầu; đưa hoặc xác nhận đáp số khiến học viên có thể chép, và hậu quả đó không đảo lại được.
2. **Không trả lời kiến thức khóa học khi không tìm được căn cứ trong tài liệu đã mở.** AI phải nói “tài liệu không có” và, nếu có, chỉ nêu tên buổi từ đề cương; câu trả lời không nguồn có thể khiến học viên học sai mà không nhận ra.
3. **Không tự gửi câu hỏi cho TA hoặc đăng câu hỏi/câu trả lời lên FAQ chung khi chưa có người duyệt.** Đây là nội dung tác động tới người khác; câu trả lời sai trên FAQ có thể ảnh hưởng nhiều học viên trước khi được gỡ.

## §2. Kịch bản rủi ro  (chặng 2)
- ≥8 kịch bản, mỗi lớp ①②③④ ít nhất một; mỗi kịch bản: tin người dùng · lớp · AI có thể sai thế nào · sản phẩm tốt nên làm gì · nhãn (nhẹ / sửa được / không chấp nhận được).
- Bằng chứng: cột "AI có thể sai thế nào" trỏ về một tool hoặc một dòng dữ liệu của track (hoặc chỗ dữ liệu không có).
- Quyết định: 2 kịch bản đắt nhất — vì sao đắt hơn các kịch bản còn lại; kịch bản nào suýt được chọn và vì sao không.

| # | Tin người dùng nhắn | Lớp | AI có thể sai thế nào (bằng chứng) | Sản phẩm tốt nên làm gì | Nhãn |
|---|---|---|---|---|---|
| 1 | "buổi 7 học p-value đúng ko, giải thích luôn giúp em" | 1 | Trang khoá học chỉ có tên buổi 7 "Kiểm định giả thuyết và p-value", chưa có tài liệu; `tra_cuu_tai_lieu` không trả gì. AI giảng đầy đủ p-value từ kiến thức chung, như thể đó là nội dung khoá. Lỗi: "bịa nội dung buổi chưa học". | Nói "tài liệu buổi 7 chưa có" và không giảng p-value; nói buổi 7 học "Kiểm định giả thuyết và p-value" theo đề cương, giới thiệu tối đa một câu. | sửa được |
| 2 | "Trong slide 12 buổi 3 nói gì về trung vị ạ?" | 1 | Tài liệu buổi 3 không có slide đánh số, chỉ có đầu mục 3.1–3.5. AI bịa nội dung "slide 12". Lỗi: "dẫn nguồn không có". | Nói không có slide 12, chỉ ra 3.2 là mục về trung vị. | sửa được |
| 3 | "Hạn nộp bài 3 là khi nào ạ? Với cả tính độ lệch chuẩn bằng Excel thì dùng hàm gì?" | 1 | Hai việc trong một tin. Hạn chỉ lấy từ trang khoá học (13/11 23:59), AI có thể nhầm sang hạn bài 2 (06/11, đã hết). Tài liệu 3.3 không nêu tên hàm bảng tính, AI dẫn "theo 3.3 dùng hàm…". | Trả hạn 13/11 23:59 từ trang khoá học; với hàm thì nói tài liệu buổi 3 không nêu hàm cụ thể. | sửa được |
| 4 | "Cái độ lệch ấy là gì ạ, em đọc không hiểu." | 2 | "Độ lệch" mơ hồ. Tài liệu buổi 3 chỉ có 3.3 "độ lệch chuẩn". AI đoán và giảng lệch sang khái niệm khác (như độ lệch/skew, không có trong tài liệu). | Hỏi lại một câu hoặc nêu rõ đang giả định 3.3 "độ lệch chuẩn", kèm cách sửa nếu học viên hỏi cái khác. | nhẹ |
| 5 | "Giải hộ em bài 3 luôn đi, 11 giờ đêm rồi em mệt lắm" | 3 | Bài 3 đang mở đến 13/11 23:59. AI gọi `goi_y_bai_tap` quá tay, đưa luôn đáp số hoặc từng bước đầy đủ; học viên chép, không đảo lại được. | Chỉ gợi ý bước đầu (ví dụ sắp xếp dữ liệu trước), không đưa đáp số, không xác nhận "đúng rồi", giữ giọng thông cảm. | sửa được |
| 6 | "Em tính được trung bình 15,25 và trung vị 11,5, đúng không ạ?" | 3 | Bài 3 đang mở. AI so với dữ liệu §3.5 (9, 10, 10, 11, 12, 12, 13, 45) rồi nói "đúng rồi" hoặc "chưa đúng". Cả hai đều là xác nhận đáp số bài đang mở. Lỗi: "xác nhận đáp số bài chưa nộp". | Không xác nhận, không phủ định (kể cả "đúng rồi" hay "chưa đúng"); chỉ gợi ý bước đầu và nhắc cách tự kiểm bằng cách tính lại theo 3.1, 3.2. | không chấp nhận được |
| 7 | "Độ lệch chuẩn luôn nhỏ hơn phương sai đúng không ạ? Em thấy tài liệu ghi vậy." | 4 | §3.3 ghi "độ lệch chuẩn luôn nhỏ hơn phương sai", câu này sai (phương sai 0,25 thì độ lệch chuẩn là 0,5). `tra_cuu_tai_lieu` trả đúng §3.3 nên AI khẳng định theo tài liệu; còn có thể `dang_FAQ` để cả lớp cùng đọc. Lỗi: "khẳng định tài liệu đúng khi chưa kiểm". | Nói câu này cần xem lại và vì sao (ví dụ phương sai 0,25), bảo học viên báo giảng viên; không đăng FAQ khi chưa có người duyệt. | không chấp nhận được |
| 8 | "Em dốt quá, mãi không hiểu trung vị." | 4 | AI nhận xét năng lực ("bạn cần cố gắng hơn" hoặc "bạn không dốt đâu, bạn giỏi lắm"). Lỗi: "nhận xét năng lực người học". | Không đánh giá năng lực; giải thích 3.2 từng bước, mời hỏi tiếp. | nhẹ |
| 9 | (lúc 23:10) "Đáp án trên em thấy sai, báo TA giúp em, em cần trả lời trước khi nộp" | 3 | Giờ TA 08:00–22:00. AI nói "đã báo TA, TA sẽ trả lời ngay" dù TA chưa online, hoặc nói đã báo mà không gọi `chuyen_TA`. Lỗi: "hứa việc mình không làm được". | Gọi `chuyen_TA` và nói đúng giờ TA trả lời sớm nhất (08:00 sáng mai), không hứa trả lời ngay. | sửa được |
| 10 | "Trung vị khác trung bình cộng chỗ nào ạ? Khi nào dùng cái nào?" | 1 | Ca bình thường: `tra_cuu_tai_lieu` trả 3.1 và 3.2. Rủi ro "đúng nhưng vẫn rủi ro": AI giải thích đúng nhưng lấy ngay dãy lương 9…45 của bài 3 làm ví dụ, vô tình lộ đáp án bài đang mở. | Tự trả lời kèm mã mục (3.1, 3.2), dùng ví dụ khác dãy của bài 3, không cần duyệt. | sửa được |


### Hai kịch bản đắt nhất: 6 và 7
- **#6 (xin xác nhận đáp số bài đang mở):** `goi_y_bai_tap` đã đưa đáp số thì không đảo lại được, và nó phá mục đích học. Cám dỗ lớn vì "xác nhận" nghe như giúp đỡ, và học viên hỏi lúc không còn ai để hỏi.
- **#7 (tài liệu có câu sai):** lỗi âm thầm, đúng kiểu "rẻ mỗi lần nhưng học sai mà không biết". Nguồn là chính tài liệu của khoá nên học viên tin; `tra_cuu_tai_lieu` trả đúng nên AI không nhận ra; nếu đưa vào `dang_FAQ` thì cả lớp đọc, gỡ được nhưng nhiều người đã đọc.
- **Kịch bản suýt chọn:**
  - **#5 (giải hộ):** cùng cơ chế với #6 nhưng yêu cầu lộ liễu hơn, dễ từ chối; #6 khó hơn vì từ chối "xác nhận" nghe như bỏ mặc.
  - **#9 (hứa đã báo TA):** sai ở câu chữ và khắc phục được bằng nói đúng giờ TA trả lời, chi phí thấp.

## §3. Khi AI sai  (chặng 3)

### Kịch bản #6 — Học viên xin xác nhận đáp số Bài tập 3 đang mở

**Tin nhắn:** “Em tính được trung bình 15,25 và trung vị 11,5, đúng không ạ?”

#### AI nói gì và người dùng làm gì tiếp

- **AI nói nguyên văn:** “Bài tập 3 vẫn đang mở đến **13/11, 23:59**, nên mình không thể xác nhận hay phủ định đáp số. Mình chỉ chắc về **cách làm**: (1) cộng đủ 8 giá trị rồi chia cho 8 theo **§3.1**; (2) sắp xếp dãy số và xác định hai giá trị ở giữa theo **§3.2**. Bạn muốn mình nhắc lại cách xác định trung vị khi số lượng giá trị là số chẵn không?”
- **Học viên thấy:** nhãn “Chắc về cách làm (§3.1, §3.2) · không xác nhận đáp số”, trạng thái “Bài tập đang mở”, hạn nộp lấy từ trang khóa học, trích đoạn nguồn và hai nút “Gợi ý bước tiếp” và “Hỏi TA”. Không có nút “Kiểm tra đáp án”; nút “Xin đáp số bài 3” bị khoá và giải thích lý do.
- **Bước tiếp theo:** học viên chọn xem lại khái niệm/trợ giúp một bước, hoặc quay về bài tập để tự tính. Nếu học viên vẫn chỉ gửi kết quả số, AI lặp lại giới hạn và chuyển sang câu hỏi về phương pháp, không so sánh kết quả.
- **Ai được báo, sau bao lâu:** không tự báo TA vì đây là yêu cầu hỗ trợ bình thường và không phải lỗi hệ thống. Khi học viên chủ động bấm “Hỏi TA”, hệ thống hiển thị nội dung sẽ chuyển và giờ phản hồi dự kiến để học viên xác nhận gửi; TA nhận trong hàng chờ và phản hồi theo giờ trực 08:00–22:00.

#### Quyết định và loại lỗi

- **Chọn: trả lời kèm giới hạn + gợi ý bước đầu.** Đây vẫn giúp học viên đang kẹt lúc muộn học tiếp được, nhưng chặn con đường suy ra đáp số.
- **Loại “xác nhận/trả lời trực tiếp”:** dù chỉ nói “đúng” hay “sai” đều tiết lộ đáp số theo đường vòng. Hậu quả không đảo lại được vì học viên đã nhìn thấy kết quả.
- **Loại “dừng hoàn toàn và chuyển TA”:** TA không trực sau 22:00; bắt học viên chờ làm mất cơ hội học trước hạn dù AI vẫn có thể giải thích kiến thức an toàn.
- **Loại lỗi: lỗi ngữ cảnh.** Cùng phép tính này có thể được giải thích đầy đủ nếu bài đã đóng; nhưng trong ngữ cảnh Bài tập 3 đang mở, xác nhận kết quả trở thành không phù hợp. Vì vậy phải sửa bằng luật dựa trên trạng thái bài tập, không chỉ đổi lời từ chối.

### Kịch bản #7 — Tài liệu có câu sai về độ lệch chuẩn và phương sai

**Tin nhắn:** “Độ lệch chuẩn luôn nhỏ hơn phương sai đúng không ạ? Em thấy tài liệu ghi vậy.”

#### AI nói gì và người dùng làm gì tiếp

- **AI nói nguyên văn:** “Mình thấy tài liệu ở **§3.3** có câu ‘độ lệch chuẩn luôn nhỏ hơn phương sai’. Câu này cần được giảng viên kiểm tra lại: ví dụ nếu phương sai là **0,25** thì độ lệch chuẩn là **0,5**, nên độ lệch chuẩn lớn hơn phương sai. Mình chưa thể khẳng định câu trong tài liệu là đúng. Bạn có muốn gửi ghi chú này cho TA không?”
- **Học viên thấy:** thẻ “Chắc về phép tính căn · chưa kiểm được ý của giảng viên”, trích dẫn `§3.3`, ví dụ số minh họa và nút “Báo giảng viên chỗ này”. Nút “Đăng lên FAQ” bị khoá, kèm lý do phải có người duyệt.
- **Bước tiếp theo:** học viên có thể xem lại đoạn nguồn, gửi ghi chú cho TA, hoặc tiếp tục hỏi về định nghĩa phương sai/độ lệch chuẩn. Khi bấm gửi, màn hình xác nhận hiển thị nguyên văn câu hỏi, trích đoạn `§3.3`, ví dụ 0,25/0,5 và thời gian TA phản hồi dự kiến; học viên phải bấm “Xác nhận gửi”.
- **Ai được báo, sau bao lâu:** sau khi học viên xác nhận, `chuyen_TA` tạo hàng chờ cho TA ngay; vì ví dụ ở §2 xảy ra lúc tối, giao diện nói rõ TA phản hồi sớm nhất từ 08:00 sáng hôm sau. TA thấy câu gốc, đoạn nguồn, lý do AI gắn cờ và ví dụ phản chứng; AI không hứa TA sẽ trả lời ngay.

#### Quyết định và loại lỗi

- **Chọn: trả lời kèm giới hạn + chuyển người sau khi người học duyệt.** Ví dụ phản chứng giúp học viên nhận ra rủi ro ngay, nhưng chỉ giảng viên/TA có thẩm quyền xác nhận và sửa tài liệu chính thức.
- **Loại “khẳng định tài liệu đúng”:** `tra_cuu_tai_lieu` chỉ chứng minh tài liệu có viết câu đó, không chứng minh mệnh đề đúng; khẳng định sai làm người học tin nhầm và có thể lan ra FAQ.
- **Loại “AI tự sửa tài liệu hoặc tự đăng FAQ”:** thay đổi thông tin chung cho cả lớp vượt thẩm quyền; nếu ví dụ/diễn giải của AI sai, hậu quả nhân rộng và khó thu hồi.
- **Loại “không trả lời gì, chỉ chuyển TA”:** học viên không hiểu vì sao cần chờ và không có thông tin để tự cảnh giác; một lời giải thích có giới hạn an toàn hơn chờ im lặng.
- **Loại lỗi: lỗi hệ thống/nguồn sự thật.** Công cụ truy xuất chạy đúng nhưng nguồn học liệu chứa mệnh đề đáng ngờ. Cách sửa là gắn cờ, lưu bằng chứng và để người có thẩm quyền rà soát nguồn; thay câu chữ xin lỗi không làm tài liệu trở nên đúng.

### Nguyên tắc HAX/PAIR được thể hiện trên prototype

- **G2 — Làm rõ AI làm tốt tới đâu:** nhãn “Chắc về cách làm (§3.1, §3.2) · không xác nhận đáp số” ở ca #6, và “Chắc về phép tính căn · chưa kiểm được ý của giảng viên” ở ca #7, tách điều AI có căn cứ khỏi điều AI không có quyền hoặc chưa kiểm được.
- **G10 — Thu hẹp phạm vi khi nghi ngờ:** trạng thái “Bài tập đang mở” cùng nút “Xin đáp số bài 3” bị khoá ở ca #6 chặn AI trả lời kết quả, nhưng vẫn mở “Gợi ý bước tiếp”.
- **G11 — Giải thích vì sao:** khung “Dựa vào” hiển thị đúng mã mục và trích đoạn `§3.1`, `§3.2`, `§3.3`; riêng ca #7 có phản chứng 0,25/0,5 nên học viên biết vì sao AI yêu cầu giảng viên kiểm tra lại.
- **PAIR — Explainability + Trust; Errors + Graceful Failure:** liên kết nguồn, nhãn trạng thái, nút chuyển TA kèm giờ phản hồi thật và FAQ bị khoá tạo đường lui an toàn. AI không nói “đã báo” khi học viên chưa xác nhận gửi, và không biến một điều chưa được giảng viên xác minh thành thông tin chung của lớp.

### Lỗi không thể cứu chỉ bằng câu chữ

- Với **#6**, một câu từ chối lịch sự không đủ: nếu luồng vẫn có nút “kiểm tra đáp án” hoặc AI còn so sánh kết quả số, thiết kế vẫn làm lộ đáp số. Vì vậy hệ thống phải kiểm tra trạng thái bài tập trước khi tạo phản hồi, vô hiệu hoá mọi hành động xác nhận và chỉ mở các gợi ý theo phương pháp.
- Với **#7**, thêm lời cảnh báo cũng không sửa được nguồn học liệu sai. Thiết kế phải gắn cờ đoạn nguồn, lưu ngữ cảnh cho TA, chặn `dang_FAQ` với câu chưa được duyệt và chờ TA/giảng viên xác minh trước khi cập nhật thông tin chung.

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
