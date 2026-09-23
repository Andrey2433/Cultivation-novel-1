# WORLD BUILD

Đây là nguồn dữ liệu nền tảng của thế giới truyện.

File này chỉ lưu **dữ liệu thế giới** dưới dạng các entry có ID.

Quy tắc đọc dữ liệu, ý nghĩa của `id`, `status`, `visibility`, `fact` và cách liên kết giữa các entry được quy định trong:

> `00_DECODE.md`

Không sao chép các quy tắc của `00_DECODE.md` vào file này.

---

# 01. WORLD FOUNDATION

Các đặc điểm và quy tắc nền tảng định nghĩa bản chất chung của thế giới.

Có thể chứa:

- bản chất thế giới
- nguyên lý vận hành chung
- trạng thái văn minh
- quy luật xã hội
- quy luật tự nhiên đã xác lập
- các nguyên tắc nền tảng

Mỗi thông tin là một entry có ID.

---

# 02. COSMOLOGY

Cấu trúc vũ trụ và các tầng tồn tại.

Có thể chứa:

- thế giới
- giới
- đại lục
- không gian đặc biệt
- tầng tồn tại
- khu vực ngoài thế giới
- cấu trúc không-thời gian đã được xác lập

Không dùng phần này để ghi diễn biến cốt truyện.

---

# 03. GEOGRAPHY

Dữ liệu địa lý cụ thể.

Có thể chứa:

- quốc gia
- tỉnh
- phủ
- huyện
- thành
- trấn
- thôn
- núi
- sông
- hồ
- rừng
- biển
- khu vực tài nguyên
- địa điểm đặc biệt
- bí cảnh có vị trí cố định

Mỗi địa điểm quan trọng nên có entry riêng.

Quan hệ địa lý được thể hiện bằng ID tham chiếu trong `fact`.

---

# 04. FACTIONS

Các thế lực và tổ chức có quyền lực hoặc phạm vi ảnh hưởng riêng.

Có thể chứa:

- quốc gia
- triều đình
- tông môn
- gia tộc
- thương hội
- bang phái
- tổ chức bí mật
- liên minh
- thế lực đặc biệt

Thông tin tập trung vào bản thân thế lực, không phải diễn biến cốt truyện của nó.

---

# 05. CHARACTERS

Các cá thể có danh tính hoặc vai trò riêng trong thế giới.

Có thể chứa:

- nhân vật chính
- nhân vật phụ
- phàm nhân
- tu sĩ
- cường giả
- nhân vật lịch sử
- nhân vật đã chết
- thực thể có ý thức
- cá thể đặc biệt

Thông tin nền của nhân vật đặt tại đây.

Các hành động hoặc sự kiện cụ thể của nhân vật đặt trong `02_STORY.md` và tham chiếu ID nhân vật.

---

# 06. CULTIVATION

Hệ thống tu luyện và các khái niệm trực tiếp cấu thành con đường tu luyện.

Có thể chứa:

- cảnh giới
- tiểu cảnh giới
- tu vi
- đột phá
- bình cảnh
- linh căn
- thể chất
- căn cơ
- linh lực
- thần thức
- đạo tâm
- tâm cảnh
- các quy tắc tu luyện
- các con đường tu luyện

Nếu một cơ chế là quy luật chung của thế giới, đặt tại đây.

---

# 07. WORLD SYSTEMS

Các hệ thống siêu nhiên hoặc quy luật lớn không thuộc riêng một cảnh giới hay nghề nghiệp.

Có thể chứa:

- nhân quả
- linh hồn
- luân hồi
- thiên đạo
- quy luật sinh tử
- không gian
- thời gian
- cơ duyên
- quy luật đặc biệt
- hệ thống bí ẩn

Một sự kiện cụ thể xảy ra trong truyện không nên đặt ở đây; chỉ đặt cơ chế nền tảng làm cho sự kiện đó có thể xảy ra.

---

# 08. ABILITIES & TECHNIQUES

Các năng lực và phương thức tác động có tính cụ thể.

Có thể chứa:

- công pháp
- thuật pháp
- thần thông
- bí thuật
- kỹ năng
- thiên phú
- năng lực bẩm sinh
- phương thức sử dụng năng lực

Nếu một năng lực chỉ thuộc một nhân vật, có thể tham chiếu nhân vật đó bằng ID.

---

# 09. CULTIVATION ARTS & CRAFTS

Các lĩnh vực kỹ nghệ, nghề nghiệp và tri thức chuyên môn của tu tiên giới.

Có thể chứa:

- luyện đan
- luyện khí
- phù lục
- trận pháp
- y đạo
- độc đạo
- chế tạo
- giám định
- các bách nghệ khác

Các quy tắc chung của một lĩnh vực đặt ở đây; kỹ năng cụ thể có thể tham chiếu sang `08. ABILITIES & TECHNIQUES`.

---

# 10. ITEMS & RESOURCES

Các vật thể, nguyên liệu và tài nguyên có danh tính hoặc quy tắc riêng.

Có thể chứa:

- pháp bảo
- pháp khí
- đan dược
- linh thảo
- thảo dược
- khoáng vật
- thiên tài địa bảo
- nguyên liệu
- phù lục
- tiền tệ
- tài nguyên tu luyện

Vật phẩm quan trọng nên có ID riêng.

---

# 11. CREATURES & SPECIES

Các loài sinh vật và các dạng tồn tại phi nhân.

Có thể chứa:

- dã thú
- yêu thú
- linh thú
- chủng tộc
- sinh vật đặc biệt
- thực thể phi nhân
- hệ thống phân loại sinh vật

Một cá thể có danh tính và vai trò như nhân vật có thể tham chiếu sang `05. CHARACTERS`.

---

# 12. HISTORY

Lịch sử nền tảng của thế giới, tức những gì đã tồn tại hoặc xảy ra trước thời điểm truyện hiện tại.

Có thể chứa:

- thời đại
- nền văn minh cổ
- chiến tranh cổ đại
- sự sụp đổ của thế lực
- lịch sử hình thành quốc gia
- lịch sử hình thành tông môn
- lịch sử hình thành địa điểm
- các sự kiện lịch sử đã hoàn thành

Không biến phần này thành timeline diễn biến của `02_STORY.md`.

---

# 13. CULTURE & SOCIETY

Dữ liệu về đời sống, xã hội và văn hóa.

Có thể chứa:

- phong tục
- tập quán
- đạo đức
- luật lệ
- tín ngưỡng
- hôn nhân
- tang lễ
- lễ hội
- giáo dục
- quan hệ phàm nhân và tu sĩ
- sinh hoạt thường ngày
- cấu trúc xã hội

Mục này giúp thế giới có thể tự vận hành ngay cả khi Trần Minh không xuất hiện.

---

# 14. ECONOMY & TRADE

Dữ liệu chuyên sâu về kinh tế và giao dịch.

Có thể chứa:

- tiền tệ
- đơn vị giá trị
- thị trường
- thương mại
- tuyến buôn bán
- giá trị tương đối của tài nguyên
- trao đổi
- thuế
- phí
- nền kinh tế địa phương

Các thông tin chưa xác định có thể để `status: unc`.

---

# 15. INSTITUTIONS & SERVICES

Các thiết chế hoặc dịch vụ mang tính tổ chức nhưng không nhất thiết là một thế lực độc lập.

Có thể chứa:

- học viện
- võ quán
- tiêu cục
- phường thị
- hiệp hội
- cơ quan quản lý
- hệ thống nhiệm vụ
- hệ thống tuyển dụng
- dịch vụ công cộng
- thiết chế địa phương

Nếu một entity đồng thời là một thế lực, có thể tham chiếu entry ở `04. FACTIONS`.

---

# 16. CONCEPTS & TERMINOLOGY

Các thuật ngữ và khái niệm có ý nghĩa riêng trong Canon.

Có thể chứa:

- thuật ngữ riêng của thế giới
- định nghĩa chuyên môn
- khái niệm dễ gây nhầm lẫn
- tên gọi đặc biệt
- cách phân biệt các khái niệm gần nhau

Mục này đặc biệt hữu ích khi một từ có nghĩa khác với cách hiểu thông thường.

---

# 17. RELATIONSHIPS

Các quan hệ nền tảng giữa các entity khi bản thân quan hệ có giá trị như một dữ liệu độc lập.

Có thể chứa:

- huyết thống
- sư đồ
- chủ tớ
- đồng minh
- đối địch
- hôn nhân
- quan hệ nhân quả
- quan hệ giữa tổ chức và cá nhân
- quan hệ giữa địa điểm và tổ chức

Không bắt buộc tạo entry riêng cho mọi quan hệ.

Nếu quan hệ đơn giản, có thể ghi trực tiếp trong `fact` của entity liên quan.

Chỉ tạo entry riêng khi quan hệ cần được tham chiếu hoặc quản lý độc lập.

---

# 18. SECRETS & HIDDEN TRUTHS

Các sự thật tồn tại trong thế giới nhưng đang bị giới hạn phạm vi biết hoặc chưa được tiết lộ.

Có thể chứa:

- bí mật của thế giới
- nguồn gốc thật sự của entity
- thân phận ẩn
- cơ chế ẩn
- sự thật chỉ Author biết
- bí mật dài hạn

`visibility` quyết định phạm vi kiến thức của entry.

Phần này lưu **sự thật**.

Việc bí mật được hé lộ trong truyện phải được ghi ở `02_STORY.md`.

---

# 19. UNRESOLVED WORLD DATA

Dữ liệu thế giới đã được ghi nhận nhưng chưa được xác lập đầy đủ.

Các entry ở đây phải dùng:

```text
status: unc
```

Không được coi dữ liệu `unc` là Canon hoàn chỉnh.

Khi được xác lập, giữ nguyên ID nếu vẫn là cùng một entity hoặc information.

---

# 20. DEPRECATED WORLD DATA

Dữ liệu thế giới cũ đã bị thay thế hoặc không còn là trạng thái hiện hành.

Các entry ở đây phải dùng:

```text
status: deprecated
```

Không sử dụng làm sự thật hiện hành.

Giữ lại khi cần truy nguyên lịch sử dữ liệu hoặc khi entry khác còn tham chiếu đến ID cũ.

---

# 21. ENTRY INDEX

Mục tra cứu ID tùy chọn.

Dùng để giúp Author tìm nhanh entry thuộc nhóm nào.

Ví dụ:

```text
WB-CHAR-001 → 05. CHARACTERS
WB-LOC-001  → 03. GEOGRAPHY
WB-SYS-001  → 07. WORLD SYSTEMS
```

Index không phải nguồn nội dung chính.

Khi index mâu thuẫn với entry thực tế, phải truy xuất entry theo ID.

---

# 22. WORLD BUILD BOUNDARY

`01_WORLD_BUILD.md` trả lời câu hỏi:

> **Thế giới này là gì, có những gì, và những thứ đó vận hành theo những quy tắc nào?**

`02_STORY.md` trả lời câu hỏi:

> **Điều gì đã xảy ra, đang xảy ra hoặc sẽ được kể trong diễn biến truyện?**

Ví dụ:

```text
WORLD BUILD:
"Lạc Gia Thôn thuộc Lạc Trấn, Lạc Sơn Huyện, Vân Khê Phủ, Thanh Hà Tỉnh, Đại Ly."

STORY:
"Trần Minh được đưa tới Lạc Gia Thôn sau sự kiện nhiễu loạn thời không."
```

Không chép cùng một thông tin vào cả hai file nếu chỉ có thể tham chiếu bằng ID.

---

# 23. ENTRY FORMAT

Mọi dữ liệu trong World Build dùng cấu trúc:

```text
id: WB-XXX-001		status: canon		visibility: author
fact: "..."
```

Các trường và quy tắc sử dụng được định nghĩa trong `00_DECODE.md`.

---

# 24. END OF WORLD BUILD
