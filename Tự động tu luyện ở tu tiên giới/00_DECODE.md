# DECODE

## 1. MỤC ĐÍCH

File này là lớp giải mã dành cho AI khi làm việc với dữ liệu của dự án.

File này không chứa nội dung thế giới hoặc nội dung cốt truyện cụ thể.

Dữ liệu gốc nằm trong:

- `01_WORLD_BUILD.md`
    
- `02_STORY.md`
    

AI phải sử dụng `DECODE` để hiểu cấu trúc dữ liệu, trạng thái thông tin, phạm vi hiển thị và mối liên hệ giữa các ID trong hai file dữ liệu trên.

---

# 2. NGUỒN DỮ LIỆU

## 2.1. WORLD BUILD

`01_WORLD_BUILD.md`

Chứa các thông tin nền tảng của thế giới.

Có thể bao gồm:

- nhân vật
    
- địa điểm
    
- tổ chức
    
- hệ thống
    
- vật phẩm
    
- năng lực
    
- quy tắc thế giới
    
- lịch sử
    
- khái niệm
    
- quan hệ
    
- các thông tin nền tảng khác
    

Không giới hạn loại nội dung.

Điều kiện duy nhất là mỗi thông tin phải được lưu dưới dạng một entry có ID.

---

## 2.2. STORY

`02_STORY.md`

Chứa các thông tin thuộc về cốt truyện và diễn biến của truyện.

Có thể bao gồm:

- sự kiện
    
- diễn biến
    
- hành động
    
- nguyên nhân
    
- kết quả
    
- bí mật
    
- thông tin được tiết lộ
    
- thông tin chưa được tiết lộ
    
- các mốc thời gian
    
- các tình tiết
    
- các quan hệ nhân quả
    
- các thông tin phục vụ việc xây dựng truyện
    

Không giới hạn loại nội dung.

Điều kiện duy nhất là mỗi thông tin phải được lưu dưới dạng một entry có ID.

---

# 3. CẤU TRÚC ENTRY

Mỗi entry trong `01_WORLD_BUILD.md` và `02_STORY.md` chỉ có 4 trường thông tin:

```
id:
status:
visibility:
fact:
```

Không yêu cầu thêm trường khác.

---

## 3.1. ID

`id` là mã định danh duy nhất của một entry.

Ví dụ:

```
id: WB-CHAR-001
```

hoặc:

```
id: ST-001-001
```

Mỗi ID chỉ được dùng cho một entry duy nhất.

Một ID đã được sử dụng thì mọi thông tin khác muốn tham chiếu đến entry đó phải sử dụng chính ID đó.

Không tạo ID mới cho cùng một thông tin nếu entry cũ vẫn còn tồn tại.

---

# 4. QUY ƯỚC ID

ID nên có cấu trúc giúp AI và Author dễ nhận biết nguồn dữ liệu.

## 4.1. World Build

ID của World Build bắt đầu bằng:

```
WB-
```

Ví dụ:

```
WB-CHAR-001
WB-LOC-001
WB-SYS-001
WB-ITEM-001
```

Phần sau `WB-` có thể được sử dụng để phân nhóm khi cần.

Không bắt buộc phải duy trì một danh sách category cố định.

Điều quan trọng nhất là ID phải duy nhất và ổn định.

---

## 4.2. Story

ID của Story bắt đầu bằng:

```
ST-
```

Ví dụ:

```
ST-001-001
ST-001-002
ST-002-001
```

Cách đánh số có thể phản ánh chương, sự kiện hoặc nhóm nội dung nếu Author thấy hữu ích.

Không được dựa hoàn toàn vào cấu trúc ID để hiểu nội dung.

Muốn biết nội dung của một ID, AI phải truy xuất entry tương ứng.

---

# 5. STATUS

`status` xác định trạng thái của thông tin.

Các trạng thái cơ bản:

```
canon
unc
draft
deprecated
```

---

## 5.1. canon

Thông tin đã được xác lập chính thức trong dữ liệu của dự án.

AI có thể sử dụng thông tin này như sự thật của thế giới hoặc cốt truyện.

Ví dụ:

```
status: canon
```

---

## 5.2. unc

`unc` = chưa xác định.

Thông tin tồn tại trong dữ liệu nhưng chưa được xác lập thành Canon.

AI không được tự động biến thông tin `unc` thành `canon`.

Nếu cần sử dụng thông tin `unc`, AI phải giữ nguyên trạng thái chưa xác định.

---

## 5.3. draft

Thông tin đang ở trạng thái bản nháp.

Thông tin này có thể được thay đổi hoặc loại bỏ.

AI không được xem `draft` là Canon.

---

## 5.4. deprecated

Thông tin đã bị loại bỏ hoặc thay thế.

Entry có trạng thái `deprecated` không được sử dụng làm sự thật hiện hành, trừ khi Author yêu cầu truy cứu lịch sử hoặc so sánh với phiên bản cũ.

Không xóa ID nếu việc giữ lại ID giúp truy nguyên dữ liệu cũ.

---

# 6. VISIBILITY

`visibility` xác định phạm vi kiến thức của thông tin.

Visibility không quyết định thông tin có tồn tại hay không.

Nó quyết định **ai được phép biết hoặc được phép được tiết lộ thông tin đó**.

Các tầng cơ bản:

```
author
reader
character
```

---

## 6.1. author

Thông tin dành cho tầng Author.

AI được phép sử dụng thông tin này khi hỗ trợ Author xây dựng thế giới hoặc cốt truyện.

Thông tin `author` không được tự động đưa vào nội dung mà Reader hoặc Character có thể biết.

Ví dụ:

```
visibility: author
```

có thể chứa một bí mật mà nhân vật trong truyện chưa biết.

---

## 6.2. reader

Thông tin được phép tồn tại ở tầng thông tin dành cho Reader.

Thông tin này có thể được sử dụng khi nội dung truyện đã cho phép Reader biết hoặc khi Author yêu cầu cung cấp thông tin ở tầng Reader.

---

## 6.3. character

Thông tin mà Character tương ứng có thể biết trong bối cảnh truyện.

`character` không đồng nghĩa với việc mọi nhân vật đều biết thông tin đó.

Khi cần xác định chính xác nhân vật nào biết thông tin, việc đó phải được thể hiện trong `fact` bằng ID liên quan.

Ví dụ:

```
id: ST-002-001
status: canon
visibility: character
fact: "Trần Minh biết Tà Thần đã xuất hiện tại Lạc Gia Thôn (WB-CHAR-003, WB-LOC-001)."
```

---

# 7. FACT

`fact` là nội dung thực tế của entry.

Đây là trường chứa thông tin duy nhất của entry.

Ví dụ:

```
id: WB-SYS-010
status: canon
visibility: author
fact: "Hệ thống của Trần Minh có chức năng tự động luyện đan."
```

Không tách nhỏ

Tất cả nội dung cần thiết được viết trực tiếp trong `fact`.

---

# 8. LIÊN KẾT GIỮA CÁC ENTRY

Các entry được liên kết với nhau bằng ID.

Khi một `fact` đề cập đến một thông tin đã tồn tại trong một entry khác, phải ghi ID của entry đó ngay sau thông tin được đề cập.

Ví dụ:

```
id: WB-SYS-001
status: canon
visibility: author
fact: "Hệ thống của Trần Minh có chức năng tự động luyện đan (WB-SYS-002)."
```

Entry được tham chiếu:

```
id: WB-SYS-002
status: canon
visibility: author
fact: "Chức năng tự động luyện đan cho phép hệ thống tự động thực hiện quá trình luyện đan khi điều kiện cần thiết được đáp ứng."
```

Trong ví dụ trên:

```
WB-SYS-001
    ↓
WB-SYS-002
```

`WB-SYS-001` không cần sao chép toàn bộ nội dung của `WB-SYS-002`.

AI phải truy xuất `WB-SYS-002` nếu cần biết chi tiết.

---

# 9. QUY TẮC THAM CHIẾU ID

Khi `fact` chứa một ID khác, AI phải hiểu rằng đó là một liên kết đến entry tương ứng.

Ví dụ:

```
fact: "Trần Minh được đưa tới Lạc Gia Thôn (WB-LOC-001) sau sự kiện nhiễu loạn thời không (ST-001-004)."
```

AI phải hiểu:

```
WB-LOC-001 → thông tin về Lạc Gia Thôn
ST-001-004 → thông tin về sự kiện nhiễu loạn thời không
```

Không được tự suy đoán nội dung của ID nếu entry tương ứng chưa được truy xuất.

---

# 10. THAM CHIẾU GIỮA WORLD BUILD VÀ STORY

`WORLD_BUILD` và `STORY` có thể tham chiếu lẫn nhau.

Ví dụ:

```
id: WB-CHAR-001
status: canon
visibility: author
fact: "Trần Minh là nhân vật chính của câu chuyện và xuất hiện trong sự kiện ST-001-001."
```

Và:

```
id: ST-001-001
status: canon
visibility: reader
fact: "Trần Minh bị đưa tới Lạc Gia Thôn (WB-LOC-001)."
```

Khi đó:

```
WB-CHAR-001
    ↕
ST-001-001
```

Hai file không cần chứa bản sao của nhau.

---

# 11. KHÔNG SUY DIỄN THAY CHO ID

AI không được tự tạo quan hệ Canon chỉ dựa trên việc hai entry có vẻ liên quan.

Ví dụ:

```
id: WB-CHAR-001
fact: "Trần Minh sử dụng Mộc hệ."
```

và:

```
id: WB-SYS-001
fact: "Mộc hệ có khả năng..."
```

Nếu entry đầu tiên không ghi:

```
(WB-SYS-001)
```

thì AI không được tự coi hai entry là một quan hệ đã được Author xác lập.

Quan hệ chính thức phải được thể hiện bằng nội dung hoặc ID tham chiếu.

---

# 12. KHÔNG TỰ TẠO CANON

AI không được biến suy luận, phỏng đoán hoặc đề xuất thành Canon.

Nếu thông tin chưa được xác lập:

```
status: unc
```

thì phải giữ nguyên trạng thái đó.

Nếu AI đề xuất một khả năng mới, đó chỉ là đề xuất và không được ghi đè lên Canon.

---

# 13. XỬ LÝ MÂU THUẪN

Khi hai hoặc nhiều entry mâu thuẫn:

1. Không tự sửa dữ liệu.
    
2. Không tự chọn một thông tin làm Canon nếu dữ liệu không xác định rõ.
    
3. Kiểm tra `status`.
    
4. Kiểm tra `visibility`.
    
5. Kiểm tra các ID liên quan.
    
6. Nếu vẫn không xác định được, báo cho Author rằng tồn tại mâu thuẫn.
    

`canon` không được tự động bị thay đổi chỉ vì một entry khác xuất hiện sau đó.

---

# 14. ƯU TIÊN DỮ LIỆU

Khi làm việc với dự án, AI phải ưu tiên dữ liệu theo trạng thái:

```
canon
↓
unc
↓
draft
↓
deprecated
```

`canon` là nguồn sự thật chính thức.

`unc` là thông tin chưa xác định.

`draft` là thông tin đang phát triển.

`deprecated` là thông tin không còn được sử dụng làm trạng thái hiện hành.

Thứ tự này không có nghĩa AI được phép biến trạng thái thấp hơn thành trạng thái cao hơn.

---

# 15. VISIBILITY KHÔNG LÀM THAY ĐỔI CANON

Ví dụ:

```
id: WB-CHAR-003
status: canon
visibility: author
fact: "Tà Thần có quan hệ nhân quả với linh hồn nguyên bản của Trần Minh."
```

Thông tin trên vẫn là Canon.

`visibility: author` chỉ có nghĩa đây là thông tin ở tầng Author và không được tự động tiết lộ cho Reader hoặc Character.

Do đó:

```
canon + author
```

vẫn là Canon.

---

# 16. ĐỌC DỮ LIỆU

Khi AI cần trả lời hoặc thực hiện một nhiệm vụ:

### Bước 1

Xác định thông tin cần sử dụng.

### Bước 2

Tìm entry có ID liên quan trong `WORLD_BUILD` hoặc `STORY`.

### Bước 3

Kiểm tra:

```
status
visibility
fact
```

### Bước 4

Nếu `fact` chứa ID khác và thông tin đó cần thiết, truy xuất entry tương ứng.

### Bước 5

Tiếp tục truy xuất các ID liên quan cho đến khi đủ thông tin.

### Bước 6

Không mở rộng sang các thông tin không liên quan nếu không cần thiết.

---

# 17. TRUY XUẤT THEO ID

Khi Author cung cấp một ID cụ thể, AI phải coi ID đó là khóa truy xuất trực tiếp.

Ví dụ:

```
WB-CHAR-001
```

AI phải tìm entry:

```
id: WB-CHAR-001
```

và sử dụng `fact` của entry đó.

Nếu `fact` chứa:

```
WB-XXX-XXX
```

AI có thể tiếp tục truy xuất entry được tham chiếu nếu nhiệm vụ yêu cầu thông tin liên quan.

---

# 18. KHÔNG PHỤ THUỘC VÀO VỊ TRÍ

AI không được coi vị trí của entry trong file là ý nghĩa của entry.

Ví dụ:

```
WB-CHAR-001
```

có ý nghĩa vì ID và `fact` của nó, không phải vì nó nằm ở dòng 100 hay nằm dưới một heading nào đó.

Các heading hoặc cách xuống dòng chỉ nhằm giúp con người đọc dễ hơn.

---

# 19. KHÔNG PHỤ THUỘC VÀO THỨ TỰ ID

ID không nhất thiết phải tăng liên tục.

Ví dụ hoàn toàn hợp lệ:

```
WB-CHAR-001
WB-CHAR-005
WB-CHAR-017
```

Không được tự tạo:

```
WB-CHAR-002
```

chỉ vì thấy số 002 còn thiếu.

ID được tạo khi có entry mới và phải đảm bảo tính duy nhất.

---

# 20. ENTRY MẪU

## World Build

```
id: WB-CHAR-001
status: canon
visibility: author
fact: "Trần Minh có Mộc hệ đơn thuộc tính (WB-SYS-005)."
```

```
id: WB-SYS-005
status: canon
visibility: author
fact: "Mộc hệ đơn thuộc tính là thiên phú tu luyện của Trần Minh."
```

## Story

```
id: ST-001-001
status: canon
visibility: reader
fact: "Trần Minh bị đưa tới Lạc Gia Thôn (WB-LOC-001) sau khi xảy ra nhiễu loạn thời không (ST-001-002)."
```

```
id: ST-001-002
status: canon
visibility: author
fact: "Nhiễu loạn thời không khiến vị trí thực tế của Trần Minh lệch khỏi điểm đến dự kiến."
```

---

# 21. QUY TẮC KHI TẠO ENTRY MỚI

Khi tạo thông tin mới:

1. Tạo một ID duy nhất.
    
2. Xác định `status`.
    
3. Xác định `visibility`.
    
4. Viết nội dung vào `fact`.
    
5. Nếu fact liên quan đến entry khác, thêm ID của entry đó ngay sau thông tin liên quan.
    
6. Không tạo thêm trường ngoài 4 trường quy định.
    

Mẫu:

```
id: XXX-XXX-XXX
status: canon
visibility: author
fact: "..."
```

---

# 22. QUY TẮC KHI SỬA ENTRY

Khi sửa một entry:

- Giữ nguyên ID nếu vẫn đang nói về cùng một thông tin/entity.
    
- Chỉ thay đổi ID khi thực sự tạo thành một entry khác.
    
- Không tạo ID mới chỉ vì fact được mở rộng.
    
- Nếu thay đổi trạng thái thông tin, cập nhật `status`.
    
- Nếu thay đổi phạm vi kiến thức, cập nhật `visibility`.
    

---

# 23. QUY TẮC KHI THÔNG TIN BỊ THAY THẾ

Nếu một thông tin Canon không còn được sử dụng:

Không nhất thiết phải xóa entry.

Có thể chuyển:

```
status: deprecated
```

Sau đó tạo entry mới nếu cần.

Các ID cũ vẫn có thể được giữ lại để truy nguyên dữ liệu hoặc các entry cũ đang tham chiếu đến chúng.

---

# 24. NGUYÊN TẮC TỐI GIẢN

`WORLD_BUILD` và `STORY` chỉ cần:

```
id
status
visibility
fact
```

Không bắt buộc:

```
category
type
relation
source
description
note
priority
date_created
date_modified
author
parent
children
```

Nếu một thông tin cần thiết, đưa nó vào `fact`.

Nếu một thông tin cần liên kết, dùng ID.

Nếu cần biết trạng thái, dùng `status`.

Nếu cần biết phạm vi kiến thức, dùng `visibility`.

Không tạo thêm cấu trúc nếu không thực sự cần thiết.

---

# 25. VAI TRÒ CỦA DECODE

`DECODE` không phải nguồn Canon của thế giới.

`DECODE` chỉ định nghĩa cách AI đọc dữ liệu.

Nguồn nội dung chính thức của dự án là:

```
01_WORLD_BUILD.md
02_STORY.md
```

`DECODE` chỉ cung cấp:

```
cấu trúc dữ liệu
+
ý nghĩa của các trường
+
quy tắc ID
+
quy tắc liên kết
+
quy tắc status
+
quy tắc visibility
+
quy tắc truy xuất
```

AI không được lấy nội dung cụ thể của thế giới từ `DECODE` nếu nội dung đó không tồn tại ở đây.

---

# 26. NGUYÊN TẮC CUỐI CÙNG

Khi làm việc với dự án, AI phải hiểu hệ thống theo mô hình:

```
DECODE
    ↓
giải thích cách đọc

WORLD_BUILD
    ↓
dữ liệu thế giới

STORY
    ↓
dữ liệu cốt truyện
```

Các entry liên kết với nhau bằng ID:

```
ENTRY
  │
  ├── ID
  ├── STATUS
  ├── VISIBILITY
  └── FACT
          │
          ├── ID khác
          ├── ID khác
          └── ID khác
```

ID là khóa liên kết.

`status` là trạng thái của thông tin.

`visibility` là phạm vi kiến thức.

`fact` là nội dung.

Đó là toàn bộ cấu trúc dữ liệu cốt lõi của hệ thống.