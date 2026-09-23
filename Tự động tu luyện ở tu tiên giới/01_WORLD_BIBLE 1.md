# WORLD BIBLE 1
# THẾ GIỚI TU TIÊN — CANON CORE

> **Mục đích:** Đây là tài liệu Canon Core của thế giới truyện. Nó không phải bản mô tả toàn bộ lore chi tiết, mà là **bản đồ dữ liệu trung tâm** giúp xác định các thành phần của thế giới, trạng thái Canon, quyền được biết, quan hệ giữa các thành phần và vị trí của chúng trong hệ thống lore.
>
> **Nguyên tắc cốt lõi:** ID ổn định > vị trí heading. Heading có thể thay đổi; Entity ID không được thay đổi sau khi đã cấp.

---

# 00. META & CANON

## 00.1. Mục đích tài liệu

[ID: META-WB-001]
[TYPE: META]
[STATUS: CANON]
[VISIBILITY: AUTHOR]

World Bible là nguồn dữ liệu nền tảng của thế giới truyện.

World Bible dùng để lưu trữ và liên kết:

- Quy luật thế giới.
- Cấu trúc thế giới.
- Hệ thống tu luyện.
- Địa điểm.
- Thế lực.
- Nhân vật.
- Hệ thống đặc biệt.
- Tài nguyên và vật phẩm.
- Sinh vật.
- Sự kiện và lịch sử.
- Quan hệ giữa các thực thể.
- Bí mật dài hạn.
- Các thông tin chưa Canon.

World Bible không được xem là một danh sách chương truyện.

Nó được tổ chức như một **cơ sở dữ liệu lore dạng Markdown**, trong đó:

> **Section ID xác định vị trí của thông tin trong tài liệu.**

> **Entity ID xác định danh tính ổn định của đối tượng.**

> **Relation xác định mối liên hệ giữa các đối tượng.**

> **Status xác định mức độ Canon.**

> **Visibility xác định ai được phép biết thông tin.**

---

## 00.2. Phạm vi Canon

[ID: META-CANON-001]
[TYPE: META]
[STATUS: CANON]
[VISIBILITY: AUTHOR]

World Bible là nguồn sự thật nền tảng của thế giới truyện.

Khi một thông tin đã được đánh dấu:

`[STATUS: CANON]`

thì thông tin đó phải được coi là sự thật của thế giới cho đến khi tác giả chính thức thay đổi hoặc loại bỏ.

Không được dùng kiến thức tu tiên phổ biến, kiến thức văn hóa, logic thể loại hoặc suy đoán của AI để ghi đè Canon.

---

## 00.3. Trạng thái thông tin

[ID: META-STATUS-001]
[TYPE: META]
[STATUS: CANON]
[VISIBILITY: AUTHOR]

Các trạng thái được sử dụng:

### CANON

Thông tin đã được tác giả xác lập.

```text
[STATUS: CANON]
```

AI phải tuân thủ.

### UNC

Thông tin chưa được Canon hóa.

```text
[STATUS: UNC]
```

Có thể tồn tại dưới dạng ghi chú hoặc hướng phát triển nhưng không được coi là sự thật.

### HYPOTHESIS

Giả thuyết hoặc khả năng.

```text
[STATUS: HYPOTHESIS]
```

Không được trình bày như Canon.

### AUTHOR_SECRET

Sự thật đã được tác giả xác lập nhưng chưa được phép tiết lộ cho nhân vật hoặc độc giả.

```text
[STATUS: AUTHOR_SECRET]
```

### DEPRECATED

Thông tin đã từng tồn tại nhưng bị loại bỏ khỏi Canon hiện tại.

```text
[STATUS: DEPRECATED]
```

Không được dùng làm sự thật hiện tại.

### CONFLICT

Có nhiều thông tin Canon đang mâu thuẫn và chưa được tác giả xử lý.

```text
[STATUS: CONFLICT]
```

AI không được tự chọn một bên để biến thành Canon mới.

---

## 00.4. Thứ tự ưu tiên Canon

[ID: META-PRIORITY-001]
[TYPE: META]
[STATUS: CANON]
[VISIBILITY: AUTHOR]

Khi có nhiều nguồn thông tin, ưu tiên theo thứ tự:

1. Canon mới nhất do tác giả xác nhận.
2. World Bible hiện tại.
3. Các tài liệu Canon được liên kết trực tiếp.
4. Ghi chú CHƯA CANON / giả thuyết.
5. Nội dung thảo luận cũ.
6. Kiến thức thông thường của AI.

Kiến thức bên ngoài không được dùng để ghi đè Canon.

---

## 00.5. Quy tắc xử lý mâu thuẫn

[ID: META-CONFLICT-001]
[TYPE: META]
[STATUS: CANON]
[VISIBILITY: AUTHOR]

Khi phát hiện mâu thuẫn:

1. Không tự sửa.
2. Không tự chọn phương án hợp lý hơn.
3. Xác định các Entity ID hoặc Fact ID liên quan.
4. Đánh dấu:
   `[STATUS: CONFLICT]`
5. Ghi rõ nội dung đang mâu thuẫn.
6. Chờ tác giả xác nhận phương án cuối cùng.
7. Sau khi xác nhận, cập nhật nguồn Canon và giữ lịch sử thay đổi nếu cần.

---

## 00.6. Quy tắc thông tin chưa xác định

[ID: META-UNC-001]
[TYPE: META]
[STATUS: CANON]
[VISIBILITY: AUTHOR]

Nếu World Bible không xác định một thông tin:

> **Không được tự biến khoảng trống thành sự thật.**

Có thể đề xuất:

- `[STATUS: HYPOTHESIS]`
- `[STATUS: UNC]`

nhưng phải giữ trạng thái rõ ràng.

Không dùng các cụm như:

- "chắc chắn là"
- "hiển nhiên là"
- "thông thường trong tu tiên giới"
- "có lẽ chắc"

để biến suy luận thành Canon.

---

## 00.7. Quy tắc đề xuất Canon mới

[ID: META-PROPOSAL-001]
[TYPE: META]
[STATUS: CANON]
[VISIBILITY: AUTHOR]

Khi cần bổ sung lore:

```text
Đề xuất
↓
Đánh dấu UNC / HYPOTHESIS
↓
Tác giả xác nhận
↓
Chuyển thành CANON
```

Không được bỏ qua bước xác nhận.

---

## 00.8. Quy tắc tiết lộ bí mật

[ID: META-REVEAL-001]
[TYPE: META]
[STATUS: CANON]
[VISIBILITY: AUTHOR]

Luôn phân biệt:

> **Tác giả biết ≠ Nhân vật biết ≠ Độc giả biết.**

Một thông tin có thể là Canon nhưng vẫn phải được đánh dấu:

```text
[STATUS: AUTHOR_SECRET]
```

Không được tự ý đưa bí mật tác giả vào lời kể, hội thoại hoặc nhận thức của nhân vật nếu chưa đến thời điểm tiết lộ.

---

## 00.9. Visibility

[ID: META-VISIBILITY-001]
[TYPE: META]
[STATUS: CANON]
[VISIBILITY: AUTHOR]

Các mức Visibility:

```text
AUTHOR
CHARACTER
READER
MIXED
PUBLIC
```

Ý nghĩa:

- `AUTHOR`: chỉ dùng ở tầng tác giả.
- `CHARACTER`: thông tin một hoặc nhiều nhân vật có thể biết.
- `READER`: thông tin đã được phép cho độc giả biết.
- `MIXED`: chỉ một phần thông tin được biết ở từng tầng.
- `PUBLIC`: thông tin phổ biến trong thế giới.

---

## 00.10. Quy tắc AI sử dụng World Bible

[ID: META-AI-001]
[TYPE: META]
[STATUS: CANON]
[VISIBILITY: AUTHOR]

Khi sử dụng World Bible:

1. Đọc Canon trước khi sáng tạo.
2. Ưu tiên Entity ID và Relation.
3. Không suy đoán thành Canon.
4. Kiểm tra Status.
5. Kiểm tra Visibility.
6. Kiểm tra các quan hệ liên quan.
7. Kiểm tra Timeline nếu vấn đề có yếu tố thời gian.
8. Nếu thiếu dữ liệu, nói rõ thiếu dữ liệu.
9. Nếu có mâu thuẫn, không tự giải quyết.
10. Khi đề xuất nội dung mới, đánh dấu UNC hoặc HYPOTHESIS.
11. Không làm thế giới xoay quanh Trần Minh nếu Canon không yêu cầu.
12. Thế giới phải tồn tại độc lập với tuyến truyện chính.

---

## 00.11. Phiên bản & lịch sử thay đổi

[ID: META-VERSION-001]
[TYPE: META]
[STATUS: CANON]
[VISIBILITY: AUTHOR]

Version hiện tại:

```text
v0.1
```

Lịch sử thay đổi được ghi theo dạng:

```text
[v0.1] Khởi tạo cấu trúc Canon Core.
```

Không đổi Entity ID chỉ vì thay đổi vị trí section.

---

# 01. COSMOLOGY & WORLD FOUNDATION

> Phần này lưu các khái niệm nền tảng quyết định thế giới vận hành như thế nào.

## 01.1. Bản chất thế giới

[ID: WORLD-NATURE-001]
[TYPE: WORLD_FOUNDATION]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Thế giới là một thế giới tu tiên.

Các thành phần nền tảng đã được xác lập gồm:

- Linh khí.
- Tu luyện.
- Công pháp.
- Thuật pháp.
- Thần thông.
- Bách Nghệ.
- Bí cảnh.
- Tài nguyên tu tiên.
- Sinh mệnh.
- Linh hồn.
- Nhân quả.

Chi tiết chưa được xác lập phải tiếp tục giữ UNC.

---

## 01.2. Cấu trúc tồn tại

[ID: COSMO-EXIST-001]
[TYPE: COSMOLOGY]
[STATUS: UNC]
[VISIBILITY: AUTHOR]

Chi tiết cấu trúc tồn tại của thế giới chưa được hoàn chỉnh.

---

## 01.3. Linh khí

[ID: COSMO-QI-001]
[TYPE: COSMOLOGY]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Linh khí tồn tại trong thế giới và là một thành phần quan trọng của hệ thống tu luyện.

Chi tiết về nguồn gốc, phân loại và quy luật vận hành chưa được hoàn chỉnh.

---

## 01.4. Âm Dương

[ID: COSMO-YINYANG-001]
[TYPE: COSMOLOGY]
[STATUS: UNC]
[VISIBILITY: AUTHOR]

Chưa Canon hóa hệ thống Âm Dương hoàn chỉnh.

---

## 01.5. Ngũ Hành

[ID: COSMO-FIVE-ELEMENTS-001]
[TYPE: COSMOLOGY]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Ngũ Hành tồn tại trong hệ thống thế giới và có liên hệ với tu luyện.

Chi tiết đầy đủ về cách vận hành phải tham chiếu hệ thống tu luyện khi được Canon hóa.

---

## 01.6. Không gian

[ID: COSMO-SPACE-001]
[TYPE: COSMOLOGY]
[STATUS: UNC]
[VISIBILITY: AUTHOR]

Chưa Canon hóa toàn bộ quy luật không gian.

---

## 01.7. Thời gian

[ID: COSMO-TIME-001]
[TYPE: COSMOLOGY]
[STATUS: UNC]
[VISIBILITY: AUTHOR]

Chưa Canon hóa toàn bộ quy luật thời gian.

---

## 01.8. Sinh mệnh

[ID: COSMO-LIFE-001]
[TYPE: COSMOLOGY]
[STATUS: UNC]
[VISIBILITY: AUTHOR]

Khái niệm sinh mệnh tồn tại nhưng hệ thống hoàn chỉnh chưa được xác lập.

---

## 01.9. Linh hồn

[ID: COSMO-SOUL-001]
[TYPE: COSMOLOGY]
[STATUS: CANON]
[VISIBILITY: MIXED]

Linh hồn là thành phần tồn tại gắn với sinh mệnh và không hoàn toàn đồng nhất với thân thể.

Linh hồn có thể bị tách rời cưỡng chế.

Trạng thái khuyết thiếu linh hồn có thể tồn tại.

Trần Minh hiện tại là một linh hồn tân sinh sau luân hồi nhưng vẫn khuyết thiếu một phần.

Chi tiết nguồn gốc phần khuyết thiếu và các dây dưa nhân quả liên quan thuộc tuyến bí mật dài hạn.

---

## 01.10. Nhân quả

[ID: COSMO-CAUSALITY-001]
[TYPE: COSMOLOGY]
[STATUS: CANON]
[VISIBILITY: MIXED]

Nhân quả tồn tại trong thế giới.

Nhân quả có liên quan trực tiếp tới bí ẩn linh hồn của Trần Minh và món nợ nhân quả.

Không được dùng khái niệm nhân quả để tự ý giải thích bí mật chưa được Canon hóa.

---

## 01.11. Đạo

[ID: COSMO-DAO-001]
[TYPE: COSMOLOGY]
[STATUS: UNC]
[VISIBILITY: AUTHOR]

Khái niệm Đạo tồn tại trong bối cảnh tu tiên nhưng hệ thống hoàn chỉnh chưa được Canon hóa.

---

## 01.12. Các quy luật nền tảng khác

[ID: COSMO-OTHER-001]
[TYPE: COSMOLOGY]
[STATUS: UNC]
[VISIBILITY: AUTHOR]

Dành cho các quy luật nền tảng được xác lập trong tương lai.

---

# 02. WORLD STRUCTURE

## 02.1. Tổng quan thế giới

[ID: WORLD-OVERVIEW-001]
[TYPE: WORLD]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Đây là một thế giới tu tiên rộng lớn.

Văn minh phát triển dựa trên:

> Linh khí + Tu luyện + Công pháp + Thuật pháp + Thần thông + Bách Nghệ + Bí cảnh + Thiên tài địa bảo.

Thế giới phải tồn tại độc lập với Trần Minh.

---

## 02.2. Quy mô thế giới

[ID: WORLD-SCALE-001]
[TYPE: WORLD]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Đại lục hiện tại cực kỳ rộng lớn.

Quy mô đất liền được ước lượng khoảng 8 lần diện tích đất liền Trái Đất.

Đây là ước lượng quy mô, không phải số liệu địa lý tuyệt đối.

---

## 02.3. Đại lục

[ID: LOC-CONT-001]
[TYPE: LOCATION]
[STATUS: UNC]
[VISIBILITY: PUBLIC]

Đại lục hiện chưa có tên chính thức được Canon hóa.

---

## 02.4. Biển

[ID: LOC-SEA-001]
[TYPE: LOCATION_GROUP]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Thế giới có các khu vực biển, trong đó có Đông Hải.

Chi tiết từng vùng biển được lưu ở phần Places.

---

## 02.5. Các khu vực chưa khám phá

[ID: WORLD-UNKNOWN-001]
[TYPE: WORLD_REGION]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Thế giới còn tồn tại nhiều khu vực chưa được khám phá hoặc chưa được xác định đầy đủ.

---

## 02.6. Phân tầng địa lý

[ID: WORLD-GEO-HIER-001]
[TYPE: RELATION_SCHEMA]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Quan hệ địa lý được biểu diễn bằng Relation thay vì phụ thuộc hoàn toàn vào vị trí heading.

Ví dụ:

```text
[REL: LOC-LGT-001 -> LOC-LCT-001]
[TYPE: LOCATED_IN]
```

---

## 02.7. Bản đồ thế giới

[ID: WORLD-MAP-001]
[TYPE: MAP]
[STATUS: UNC]
[VISIBILITY: PUBLIC]

Bản đồ hoàn chỉnh chưa được Canon hóa.

---

# 03. POLITICAL & SOCIAL STRUCTURE

## 03.1. Quốc gia

[ID: FACTION-STATE-001]
[TYPE: FACTION_GROUP]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Ba đại quốc đã được xác lập:

- Đại Ly.
- Đại Càn.
- Đại Nguyên.

---

## 03.2. Tông môn

[ID: FACTION-SECT-001]
[TYPE: FACTION_GROUP]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Tông môn là một dạng thế lực quan trọng trong xã hội tu tiên.

---

## 03.3. Gia tộc

[ID: FACTION-CLAN-001]
[TYPE: FACTION_GROUP]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Gia tộc tồn tại trong thế giới.

Cơ cấu chi tiết chưa được hoàn chỉnh.

---

## 03.4. Thành trì

[ID: FACTION-CITY-001]
[TYPE: SETTLEMENT_GROUP]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Thành trì và thành thị là các đơn vị dân cư quan trọng.

---

## 03.5. Thôn trấn

[ID: FACTION-VILLAGE-001]
[TYPE: SETTLEMENT_GROUP]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Thôn, trấn và các đơn vị dân cư cấp thấp tồn tại trong thế giới.

---

## 03.6. Tổ chức

[ID: FACTION-ORG-001]
[TYPE: FACTION_GROUP]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Các tổ chức khác có thể được đăng ký tại đây.

---

## 03.7. Cấu trúc quyền lực

[ID: RULE-POWER-001]
[TYPE: SOCIAL_RULE]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Sức mạnh có ảnh hưởng lớn đến địa vị và quyền lực.

Tuy nhiên thế giới không hoàn toàn hỗn loạn; luật lệ, thế lực và lợi ích chung duy trì trật tự tương đối ổn định.

---

## 03.8. Luật lệ

[ID: RULE-SOCIAL-001]
[TYPE: SOCIAL_RULE]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Thế giới có luật lệ và trật tự riêng.

Chi tiết từng khu vực cần được xác định riêng.

---

## 03.9. Xã hội phàm nhân

[ID: WORLD-SOCIAL-MORTAL-001]
[TYPE: SOCIAL_STRUCTURE]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Phàm nhân tồn tại và có đời sống xã hội riêng, bao gồm nông nghiệp, chăn nuôi, săn bắn, thương nghiệp và sinh hoạt địa phương.

---

## 03.10. Xã hội tu sĩ

[ID: WORLD-SOCIAL-CULTIVATOR-001]
[TYPE: SOCIAL_STRUCTURE]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Tu sĩ có hệ thống giao dịch, tu luyện, nhiệm vụ, tông môn, phường thị và các quan hệ riêng.

---

## 03.11. Quan hệ phàm nhân và tu sĩ

[ID: REL-MORTAL-CULTIVATOR-001]
[TYPE: RELATION]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Phàm nhân và tu sĩ cùng tồn tại trong một thế giới nhưng có chênh lệch lớn về sức mạnh và phạm vi hoạt động.

---

# 04. CULTIVATION SYSTEM

## 04.1. Định nghĩa tu luyện

[ID: CULT-DEFINITION-001]
[TYPE: CULTIVATION]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Tu luyện là con đường nâng cao sinh mệnh và thực lực của cá thể thông qua hệ thống tu tiên.

---

## 04.2. Cảnh giới

[ID: CULT-REALM-001]
[TYPE: CULTIVATION_SYSTEM]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Hệ thống cảnh giới tồn tại.

Các cảnh giới cao được xác lập trong Canon hiện có gồm:

- Trúc Cơ.
- Kim Đan.
- Nguyên Anh.
- Hóa Thần.

Cảnh giới trước và sau cần được quản lý bằng danh sách Canon riêng khi được xác nhận.

---

## 04.3. Linh căn

[ID: CULT-ROOT-001]
[TYPE: CULTIVATION_SYSTEM]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Linh căn là một thành phần của hệ thống tu luyện.

Chi tiết phân loại chưa được hoàn chỉnh trong Canon Core này.

---

## 04.4. Linh lực

[ID: CULT-POWER-001]
[TYPE: CULTIVATION_SYSTEM]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Linh lực là năng lượng được sử dụng trong tu luyện.

---

## 04.5. Chân Nguyên

[ID: CULT-TRUE_ESSENCE-001]
[TYPE: CULTIVATION_SYSTEM]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Chân Nguyên là một khái niệm trong hệ thống tu luyện.

Chi tiết chuyển hóa và điều kiện sử dụng cần được Canon hóa riêng.

---

## 04.6. Thần thức

[ID: CULT-DIVINE_SENSE-001]
[TYPE: CULTIVATION_SYSTEM]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Thần thức là một năng lực thuộc hệ thống tu luyện.

---

## 04.7. Đạo cơ

[ID: CULT-FOUNDATION-001]
[TYPE: CULTIVATION_SYSTEM]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Đạo cơ là một thành phần của hệ thống tu luyện.

---

## 04.8. Kim Đan

[ID: CULT-GOLDEN_CORE-001]
[TYPE: CULTIVATION_SYSTEM]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Kim Đan là một cảnh giới / trạng thái quan trọng của tu luyện.

---

## 04.9. Đạo tâm

[ID: CULT-DAO_HEART-001]
[TYPE: CULTIVATION_SYSTEM]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Đạo tâm là nền tảng tinh thần định hướng con đường tu luyện.

Đạo tâm không đồng nhất với tâm trạng.

Đạo tâm có tính lâu dài và được củng cố hoặc dao động thông qua lựa chọn, hành động, trải nghiệm và nhận thức.

---

## 04.10. Đột phá

[ID: CULT-BREAKTHROUGH-001]
[TYPE: CULTIVATION_SYSTEM]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Đột phá cảnh giới là quá trình vượt qua giới hạn hiện tại để tiến vào cảnh giới cao hơn.

---

## 04.11. Bình cảnh

[ID: CULT-BOTTLENECK-001]
[TYPE: CULTIVATION_SYSTEM]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Bình cảnh tồn tại trong quá trình tu luyện.

Đạo tâm và tâm cảnh có thể ảnh hưởng đến quá trình vượt qua bình cảnh.

---

## 04.12. Tuổi thọ

[ID: CULT-LIFESPAN-001]
[TYPE: CULTIVATION_SYSTEM]
[STATUS: UNC]
[VISIBILITY: PUBLIC]

Hệ thống tuổi thọ hoàn chỉnh chưa được Canon hóa.

---

## 04.13. Thực lực

[ID: CULT-COMBAT_POWER-001]
[TYPE: CULTIVATION_SYSTEM]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Thực lực chiến đấu không được mặc định đồng nhất tuyệt đối với cảnh giới.

Chi tiết cách đánh giá thực lực cần được xác lập riêng.

---

## 04.14. Giới hạn tu luyện

[ID: CULT-LIMIT-001]
[TYPE: CULTIVATION_SYSTEM]
[STATUS: UNC]
[VISIBILITY: AUTHOR]

Giới hạn cuối cùng của toàn bộ hệ thống tu luyện chưa được Canon hóa.

---

# 05. CULTIVATION ARTS

## 05.1. Công pháp

[ID: ART-METHOD-001]
[TYPE: CULTIVATION_ART]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Công pháp là phương pháp tu luyện.

---

## 05.2. Thuật pháp

[ID: ART-SPELL-001]
[TYPE: CULTIVATION_ART]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Thuật pháp là năng lực được tu sĩ tu luyện và sử dụng.

---

## 05.3. Thần thông

[ID: ART-DIVINE_ABILITY-001]
[TYPE: CULTIVATION_ART]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Thần thông là một dạng năng lực cấp cao hơn hoặc đặc biệt hơn thuật pháp.

Phân biệt chi tiết cần được Canon hóa.

---

## 05.4. Bí thuật

[ID: ART-SECRET_TECHNIQUE-001]
[TYPE: CULTIVATION_ART]
[STATUS: UNC]
[VISIBILITY: PUBLIC]

Hệ thống bí thuật chưa được hoàn chỉnh.

---

## 05.5. Kiếm đạo

[ID: ART-SWORD-001]
[TYPE: CULTIVATION_ART]
[STATUS: UNC]
[VISIBILITY: PUBLIC]

Chưa Canon hóa hệ thống Kiếm đạo riêng.

---

## 05.6. Các hệ thống tu luyện đặc biệt

[ID: ART-SPECIAL-001]
[TYPE: CULTIVATION_ART]
[STATUS: UNC]
[VISIBILITY: AUTHOR]

Dành cho các con đường tu luyện đặc biệt nếu được xác lập.

---

## 05.7. Phân loại năng lực

[ID: ART-TAXONOMY-001]
[TYPE: TAXONOMY]
[STATUS: UNC]
[VISIBILITY: AUTHOR]

Bảng phân loại thống nhất cho công pháp, thuật pháp, thần thông và bí thuật sẽ được bổ sung khi Canon hóa.

---

# 06. RESOURCES & CRAFTING

## 06.1. Tài nguyên

[ID: RES-GENERAL-001]
[TYPE: RESOURCE]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Tài nguyên là nền tảng vật chất quan trọng của đời sống và tu luyện.

---

## 06.2. Thảo dược

[ID: RES-HERB-001]
[TYPE: RESOURCE]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Thảo dược tồn tại trong thế giới.

---

## 06.3. Linh thảo

[ID: RES-SPIRIT_HERB-001]
[TYPE: RESOURCE]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Linh thảo tồn tại ở nhiều khu vực có linh khí phù hợp.

---

## 06.4. Khoáng vật

[ID: RES-MINERAL-001]
[TYPE: RESOURCE]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Khoáng vật và khoáng vật có linh khí tồn tại trong thế giới.

---

## 06.5. Yêu thú tài nguyên

[ID: RES-BEAST-001]
[TYPE: RESOURCE]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Yêu thú có thể trở thành nguồn tài nguyên tùy theo loài và điều kiện.

---

## 06.6. Thiên tài địa bảo

[ID: RES-TREASURE-001]
[TYPE: RESOURCE]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Thiên tài địa bảo tồn tại trong thế giới.

Hệ thống phân cấp chưa được hoàn chỉnh.

---

## 06.7. Luyện đan

[ID: ART-ALCHEMY-001]
[TYPE: CRAFTING_ART]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Luyện đan là một trong các Bách Nghệ.

---

## 06.8. Luyện khí

[ID: ART-REFINING-001]
[TYPE: CRAFTING_ART]
[STATUS: UNC]
[VISIBILITY: PUBLIC]

Hệ thống luyện khí chi tiết chưa được Canon hóa.

---

## 06.9. Phù lục

[ID: ART-TALISMAN-001]
[TYPE: CRAFTING_ART]
[STATUS: UNC]
[VISIBILITY: PUBLIC]

Hệ thống phù lục chi tiết chưa được Canon hóa.

---

## 06.10. Trận pháp

[ID: ART-ARRAY-001]
[TYPE: CRAFTING_ART]
[STATUS: UNC]
[VISIBILITY: PUBLIC]

Hệ thống trận pháp chi tiết chưa được Canon hóa.

---

## 06.11. Các Bách Nghệ khác

[ID: ART-HUNDRED_ARS-001]
[TYPE: CRAFTING_SYSTEM]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Bách Nghệ tồn tại như một nhóm các kỹ nghệ liên quan đến tu tiên.

Danh mục hoàn chỉnh chưa được Canon hóa.

---

# 07. CREATURES & LIFE

## 07.1. Phàm nhân

[ID: CREA-MORTAL-001]
[TYPE: CREATURE_GROUP]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Phàm nhân là bộ phận dân cư phổ biến của thế giới.

---

## 07.2. Võ giả

[ID: CREA-MARTIAL-001]
[TYPE: CREATURE_GROUP]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Võ giả tồn tại và có thể hoạt động trong xã hội phàm nhân và vùng giao thoa với tu tiên giới.

---

## 07.3. Tu sĩ

[ID: CREA-CULTIVATOR-001]
[TYPE: CREATURE_GROUP]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Tu sĩ là những cá thể tu luyện.

---

## 07.4. Yêu thú

[ID: CREA-DEMON_BEAST-001]
[TYPE: CREATURE_GROUP]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Yêu thú tồn tại trong các khu vực hoang dã và khu vực có linh khí.

---

## 07.5. Linh thú

[ID: CREA-SPIRIT_BEAST-001]
[TYPE: CREATURE_GROUP]
[STATUS: UNC]
[VISIBILITY: PUBLIC]

Hệ thống linh thú chưa được hoàn chỉnh.

---

## 07.6. Sinh vật đặc biệt

[ID: CREA-SPECIAL-001]
[TYPE: CREATURE_GROUP]
[STATUS: UNC]
[VISIBILITY: AUTHOR]

Dành cho sinh vật không thuộc các nhóm thông thường.

---

## 07.7. Chủng tộc / giống loài khác

[ID: CREA-RACE-001]
[TYPE: CREATURE_GROUP]
[STATUS: UNC]
[VISIBILITY: AUTHOR]

Chưa Canon hóa hệ thống chủng tộc khác.

---

# 08. PLACES

> Địa điểm được quản lý bằng Entity ID. Quan hệ "thuộc", "gần", "nằm trong", "kết nối với" được lưu bằng Relation.

## 08.1. Đại Ly

[ID: LOC-DALI-001]
[TYPE: LOCATION]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Đại Ly là một trong ba quốc gia lớn của đại lục.

Vị trí: phía Đông đại lục.

---

## 08.2. Thanh Hà Tỉnh

[ID: LOC-THANHHA-001]
[TYPE: LOCATION]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Thanh Hà Tỉnh thuộc Đại Ly.

---

## 08.3. Vân Khê Phủ

[ID: LOC-VANKHE-001]
[TYPE: LOCATION]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Vân Khê Phủ thuộc Thanh Hà Tỉnh.

---

## 08.4. Lạc Sơn Huyện

[ID: LOC-LACSON-001]
[TYPE: LOCATION]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Lạc Sơn Huyện thuộc Vân Khê Phủ.

---

## 08.5. Lạc Trấn

[ID: LOC-LACTRAN-001]
[TYPE: LOCATION]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Lạc Trấn thuộc Lạc Sơn Huyện.

Đây là trung tâm giao thương của khu vực xung quanh Lạc Gia Thôn.

---

## 08.6. Lạc Gia Thôn

[ID: LOC-LGT-001]
[TYPE: LOCATION]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Lạc Gia Thôn thuộc Lạc Trấn, Lạc Sơn Huyện, Vân Khê Phủ, Thanh Hà Tỉnh, Đại Ly.

Đây là điểm xuất phát của Trần Minh.

Đặc điểm:

- Chủ yếu là phàm nhân.
- Trồng trọt.
- Chăn nuôi.
- Săn bắn.
- Thu thập thảo dược.
- Trao đổi hàng hóa với các thôn và Lạc Trấn.

---

## 08.7. Thanh Dương Tông

[ID: LOC-TDY-SECT-001]
[TYPE: LOCATION]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Thanh Dương Tông thuộc Đại Ly.

Đây là tông môn Trần Minh sẽ gia nhập trong giai đoạn đầu.

---

## 08.8. Thanh Dương Thành

[ID: LOC-TDY-CITY-001]
[TYPE: LOCATION]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Thanh Dương Thành là thành thị lớn nằm gần Thanh Dương Tông.

Đây là trung tâm giao thương quan trọng của khu vực.

---

## 08.9. Thanh Dương Sơn Mạch

[ID: LOC-TDY-MOUNTAINS-001]
[TYPE: LOCATION]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Thanh Dương Sơn Mạch là hệ thống núi nằm phía sau và xung quanh Thanh Dương Tông.

Đây là khu vực tài nguyên quan trọng.

---

## 08.10. Đông Hải

[ID: LOC-EASTSEA-001]
[TYPE: LOCATION]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Đông Hải nằm ở khu vực phía Đông đại lục.

Các vùng liên quan gồm:

- Hải Vực Ngoại Vi.
- Vùng Biển Nguy Hiểm.
- Hóa Thần Hải.
- Vùng Sương Mù.

---

## 08.11. Các khu vực khác

Các địa điểm đã xuất hiện trong Canon cần tiếp tục được cấp Entity ID riêng thay vì nhét nhiều địa điểm vào một entry.

Địa điểm hiện đã được xác định hoặc đề cập:

```text
[LOC-THANHHA-VILLAGE-001] Thanh Hà Thôn
[LOC-HACSON-VILLAGE-001] Hắc Sơn Thôn
[LOC-BACHTHACH-VILLAGE-001] Bạch Thạch Thôn
[LOC-LINHKHE-VILLAGE-001] Linh Khê Thôn
[LOC-THANHKHE-001] Thanh Khê
[LOC-THANHKHE-FOREST-001] Thanh Khê Lâm
[LOC-HACSON-001] Hắc Sơn
[LOC-DUOC COC-001] Dược Cốc
[LOC-BACHTHACH-MINE-001] Bạch Thạch Quặng
[LOC-HACPHONG-001] Hắc Phong Sơn
[LOC-LAC-THANH-001] Lạc Thành
[LOC-XIAN-FANG-001] Phường Thị Tu Tiên
[LOC-TDY-MARKET-001] Thanh Dương Phường Thị
[LOC-HACVAN-FOREST-001] Hắc Vân Lâm
[LOC-BACHNGOC-KHE-001] Bạch Ngọc Khê
[LOC-LINHKHE-TOWN-001] Linh Khê Trấn
```

> Các ID trong danh sách này là ID registry được dành trước. Nếu một ID đã được sử dụng ở tài liệu khác, phải ưu tiên ID Canon đang tồn tại và không tạo ID trùng.

---

# 09. ORGANIZATIONS & FACTIONS

## 09.1. Thanh Dương Tông

[ID: FACTION-TDY-001]
[TYPE: SECT]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Thanh Dương Tông là tông môn thuộc Đại Ly.

Trần Minh sẽ gia nhập Thanh Dương Tông trong giai đoạn đầu.

Cơ cấu hoàn chỉnh của tông môn chưa được Canon hóa.

---

## 09.2. Các tông môn

[ID: FACTION-SECTS-001]
[TYPE: FACTION_GROUP]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Các tông môn khác tồn tại trong thế giới.

Danh sách đầy đủ chưa được Canon hóa.

---

## 09.3. Gia tộc

[ID: FACTION-CLANS-001]
[TYPE: FACTION_GROUP]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Các gia tộc tồn tại trong thế giới.

---

## 09.4. Thương hội

[ID: FACTION-MERCHANTS-001]
[TYPE: FACTION_GROUP]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Thương hội tồn tại trong xã hội tu tiên.

---

## 09.5. Tán tu / liên minh

[ID: FACTION-FREE-001]
[TYPE: FACTION_GROUP]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Tán tu và các nhóm liên minh có thể hoạt động ngoài tông môn.

---

## 09.6. Tổ chức bí mật

[ID: FACTION-SECRET-001]
[TYPE: FACTION_GROUP]
[STATUS: UNC]
[VISIBILITY: AUTHOR]

Các tổ chức bí mật chưa được xác lập đầy đủ.

---

## 09.7. Các thế lực chưa xác định

[ID: FACTION-UNKNOWN-001]
[TYPE: FACTION_GROUP]
[STATUS: UNC]
[VISIBILITY: AUTHOR]

Dành cho thế lực được nhắc tới nhưng chưa có hồ sơ hoàn chỉnh.

---

# 10. CHARACTERS

## 10.1. Trần Minh

[ID: CHAR-TRM-001]
[TYPE: CHARACTER]
[STATUS: CANON]
[VISIBILITY: MIXED]

### 10.1.1. Thông tin cơ bản

- Tên: Trần Minh.
- Vai trò: Nhân vật chính.
- Xuất phát: [[Lạc Gia Thôn]]
- Con đường: Tu tiên.
- Tông môn về sau: [[Thanh Dương Tông]]

### 10.1.2. Linh hồn

[REL: CHAR-TRM-001 -> COSMO-SOUL-001]
[TYPE: HAS_STATE]
[STATUS: CANON]

Trần Minh hiện tại là một linh hồn tân sinh sau luân hồi nhưng vẫn khuyết thiếu một phần.

### 10.1.3. Bí mật

[REL: CHAR-TRM-001 -> MYST-SOUL-001]
[TYPE: CONNECTED_TO]
[STATUS: AUTHOR_SECRET]

[REL: CHAR-TRM-001 -> MYST-DEBT-001]
[TYPE: CONNECTED_TO]
[STATUS: AUTHOR_SECRET]

### 10.1.4. Nguyên tắc hành xử

Trần Minh có xu hướng che giấu thực lực và thiên phú do nguyên tắc:

> Mang ngọc có tội.

### 10.1.5. Các mối liên kết

```text
[REL: CHAR-TRM-001 -> LOC-LGT-001]
[TYPE: ORIGIN]
[STATUS: CANON]

[REL: CHAR-TRM-001 -> FACTION-TDY-001]
[TYPE: MEMBER]
[STATUS: CANON]

[REL: CHAR-TRM-001 -> SYS-MAIN-001]
[TYPE: USER]
[STATUS: CANON]

[REL: CHAR-TRM-001 -> MYST-SOUL-001]
[TYPE: CONNECTED_TO]
[STATUS: AUTHOR_SECRET]

[REL: CHAR-TRM-001 -> MYST-DEBT-001]
[TYPE: CONNECTED_TO]
[STATUS: AUTHOR_SECRET]
```

---

## 10.2. Nhân vật chính khác

[ID: CHAR-MAIN-001]
[TYPE: CHARACTER_GROUP]
[STATUS: UNC]
[VISIBILITY: AUTHOR]

Chưa có danh sách hoàn chỉnh.

---

## 10.3. Nhân vật phụ

[ID: CHAR-SUPPORT-001]
[TYPE: CHARACTER_GROUP]
[STATUS: UNC]
[VISIBILITY: AUTHOR]

Danh sách sẽ được tách thành từng Entity ID khi nhân vật được Canon hóa.

---

## 10.4. Nhân vật quan trọng

[ID: CHAR-IMPORTANT-001]
[TYPE: CHARACTER_GROUP]
[STATUS: UNC]
[VISIBILITY: AUTHOR]

Danh sách chưa hoàn chỉnh.

---

## 10.5. Nhân vật bí ẩn

[ID: CHAR-MYSTERIOUS-001]
[TYPE: CHARACTER_GROUP]
[STATUS: AUTHOR_SECRET]
[VISIBILITY: AUTHOR]

Dùng cho các nhân vật mà danh tính hoặc vai trò cần được giữ bí mật.

---

## 10.6. Nhân vật lịch sử

[ID: CHAR-HISTORICAL-001]
[TYPE: CHARACTER_GROUP]
[STATUS: UNC]
[VISIBILITY: AUTHOR]

---

## 10.7. Nhân vật đã chết

[ID: CHAR-DEAD-001]
[TYPE: CHARACTER_GROUP]
[STATUS: UNC]
[VISIBILITY: AUTHOR]

---

# 11. SYSTEM — TRẦN MINH

## 11.1. Tổng quan Hệ thống

[ID: SYS-MAIN-001]
[TYPE: SYSTEM]
[STATUS: CANON]
[VISIBILITY: MIXED]

Trần Minh sở hữu một Hệ thống có khả năng hỗ trợ các hoạt động tự động trong quá trình tu luyện.

Nguồn gốc và toàn bộ bản chất của Hệ thống chưa được tiết lộ hoàn toàn.

---

## 11.2. Tự động tu luyện

[ID: SYS-AUTO-CULT-001]
[TYPE: SYSTEM_FUNCTION]
[STATUS: CANON]
[VISIBILITY: CHARACTER]

Hệ thống có chức năng tự động tu luyện.

---

## 11.3. Tự động kỹ năng

[ID: SYS-AUTO-SKILL-001]
[TYPE: SYSTEM_FUNCTION]
[STATUS: CANON]
[VISIBILITY: CHARACTER]

Hệ thống có chức năng tự động luyện tập kỹ năng.

---

## 11.4. Tự động Bách Nghệ

[ID: SYS-AUTO-ART-001]
[TYPE: SYSTEM_FUNCTION]
[STATUS: CANON]
[VISIBILITY: CHARACTER]

Hệ thống có khả năng hỗ trợ tự động Bách Nghệ.

---

## 11.5. Tiểu Hóa Thân

[ID: SYS-CLONE-001]
[TYPE: SYSTEM_FUNCTION]
[STATUS: CANON]
[VISIBILITY: MIXED]

Tiểu Hóa Thân là một chức năng của Hệ thống.

Tiểu Hóa Thân có thể:

- Chiến đấu.
- Bị thương.
- Tử vong.
- Khai phá.
- Thu thập tài nguyên.

Tiểu Hóa Thân không trực tiếp khiến Trần Minh chịu thương tổn hoặc tử vong theo cách thông thường.

Tài nguyên và vật phẩm thu được có thể được đưa ra thực tại.

---

## 11.6. Tự động Bí Cảnh

[ID: SYS-DUNGEON-001]
[TYPE: SYSTEM_FUNCTION]
[STATUS: CANON]
[VISIBILITY: MIXED]

Tiểu Hóa Thân có thể thay Trần Minh tiến hành thăm dò, khai phá, chiến đấu và thu thập tài nguyên trong bí cảnh.

Điều kiện:

> Trần Minh trước tiên phải từng trực tiếp bước vào bí cảnh đó thì bí cảnh mới xuất hiện trong danh sách có thể tự động tham gia.

---

## 11.7. Giới hạn

[ID: SYS-LIMIT-001]
[TYPE: SYSTEM_RULE]
[STATUS: CANON]
[VISIBILITY: MIXED]

Hệ thống có giới hạn.

Các giới hạn cụ thể phải được đăng ký thành từng Rule ID thay vì ghi chung chung.

---

## 11.8. Quy tắc ẩn

[ID: SYS-HIDDEN-001]
[TYPE: SYSTEM_SECRET]
[STATUS: AUTHOR_SECRET]
[VISIBILITY: AUTHOR]

Hệ thống có những chức năng hoặc quy tắc chưa được Trần Minh biết.

Không được tự ý tiết lộ.

---

## 11.9. Nguồn gốc

[ID: SYS-ORIGIN-001]
[TYPE: SYSTEM_MYSTERY]
[STATUS: AUTHOR_SECRET]
[VISIBILITY: AUTHOR]

Nguồn gốc Hệ thống là một bí mật dài hạn.

---

## 11.10. Những gì Trần Minh biết

[ID: SYS-KNOWN-001]
[TYPE: KNOWLEDGE_STATE]
[STATUS: CANON]
[VISIBILITY: CHARACTER]

Danh sách này chỉ chứa những gì Trần Minh thực sự biết về Hệ thống.

---

## 11.11. Những gì Trần Minh không biết

[ID: SYS-UNKNOWN-001]
[TYPE: KNOWLEDGE_STATE]
[STATUS: AUTHOR_SECRET]
[VISIBILITY: AUTHOR]

Danh sách này chứa những sự thật về Hệ thống mà Trần Minh chưa biết.

---

# 12. HISTORY & TIMELINE

## 12.1. Thời đại cổ đại

[ID: HIST-ANCIENT-001]
[TYPE: ERA]
[STATUS: UNC]
[VISIBILITY: PUBLIC]

Chưa hoàn chỉnh.

---

## 12.2. Thời đại trung cổ

[ID: HIST-MIDDLE-001]
[TYPE: ERA]
[STATUS: UNC]
[VISIBILITY: PUBLIC]

Chưa hoàn chỉnh.

---

## 12.3. Thời đại hiện tại

[ID: HIST-CURRENT-001]
[TYPE: ERA]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Truyện diễn ra trong thời đại hiện tại của thế giới tu tiên.

---

## 12.4. Các đại sự kiện

[ID: EVENT-GLOBAL-001]
[TYPE: EVENT_GROUP]
[STATUS: UNC]
[VISIBILITY: AUTHOR]

Mỗi sự kiện quan trọng phải được cấp Event ID riêng.

Format:

```text
[EVENT-ARC1-001]
[EVENT-GLOBAL-001]
[EVENT-TDY-001]
```

---

## 12.5. Lịch sử các thế lực

[ID: HIST-FACTION-001]
[TYPE: HISTORY]
[STATUS: UNC]
[VISIBILITY: AUTHOR]

Lịch sử của từng thế lực được liên kết bằng:

```text
[REL: FACTION-ID -> HIST-ID]
[TYPE: HISTORY]
```

---

## 12.6. Lịch sử địa phương

[ID: HIST-LOCAL-001]
[TYPE: HISTORY]
[STATUS: UNC]
[VISIBILITY: AUTHOR]

---

## 12.7. Timeline Trần Minh

[ID: HIST-TRM-001]
[TYPE: CHARACTER_TIMELINE]
[STATUS: CANON]
[VISIBILITY: MIXED]

Các sự kiện liên quan trực tiếp đến Trần Minh phải được liên kết bằng Event ID.

---

## 12.8. Timeline bí mật

[ID: HIST-SECRET-001]
[TYPE: SECRET_TIMELINE]
[STATUS: AUTHOR_SECRET]
[VISIBILITY: AUTHOR]

Dùng để lưu những sự kiện đã xảy ra nhưng chưa được phép tiết lộ.

---

# 13. RULES & RELATIONSHIPS

## 13.1. Quy luật nhân quả

[ID: RULE-CAUS-001]
[TYPE: RULE]
[STATUS: CANON]
[VISIBILITY: MIXED]

Nhân quả tồn tại trong thế giới.

Món nợ nhân quả của Trần Minh là một bí mật riêng, không được dùng quy luật chung để tự ý giải thích.

---

## 13.2. Quy luật linh hồn

[ID: RULE-SOUL-001]
[TYPE: RULE]
[STATUS: CANON]
[VISIBILITY: MIXED]

Linh hồn có thể tồn tại độc lập tương đối với thân thể.

Linh hồn có thể bị tách rời cưỡng chế.

Linh hồn khuyết thiếu không đồng nghĩa với mất toàn bộ linh hồn.

---

## 13.3. Quy luật cảnh giới

[ID: RULE-REALM-001]
[TYPE: RULE]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Cảnh giới là một hệ thống phân tầng thực lực và trạng thái tu luyện.

Chi tiết tương ứng giữa cảnh giới, tuổi thọ, thần thức, linh lực và chiến lực phải được quản lý bằng các Rule / Cultivation Entity riêng.

---

## 13.4. Quan hệ giữa các hệ thống

[ID: REL-SYSTEM-001]
[TYPE: RELATION_GROUP]
[STATUS: CANON]
[VISIBILITY: AUTHOR]

Ví dụ:

```text
[REL: CHAR-TRM-001 -> SYS-MAIN-001]
[TYPE: USER]

[REL: SYS-MAIN-001 -> SYS-CLONE-001]
[TYPE: CONTAINS_FUNCTION]

[REL: SYS-CLONE-001 -> LOC-DUNGEON-001]
[TYPE: OPERATES_IN]
```

---

## 13.5. Quan hệ giữa các thế lực

[ID: REL-FACTION-001]
[TYPE: RELATION_GROUP]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

Quan hệ giữa các thế lực phải dùng Relation ID.

Ví dụ:

```text
[REL: FACTION-TDY-001 -> FACTION-STATE-001]
[TYPE: BELONGS_TO]
```

---

## 13.6. Quan hệ nhân vật

[ID: REL-CHARACTER-001]
[TYPE: RELATION_GROUP]
[STATUS: CANON]
[VISIBILITY: MIXED]

Các quan hệ nhân vật được ghi theo dạng:

```text
[REL: CHAR-A -> CHAR-B]
[TYPE: RELATION_TYPE]
[STATUS: CANON]
```

---

## 13.7. Điều kiện / phụ thuộc

[ID: RULE-DEPENDENCY-001]
[TYPE: RULE]
[STATUS: CANON]
[VISIBILITY: AUTHOR]

Các hệ thống có điều kiện phải ghi rõ:

```text
[REQUIRES: ENTITY-ID]
[BLOCKED_BY: ENTITY-ID]
[UNLOCKS: ENTITY-ID]
```

---

## 13.8. Ngoại lệ

[ID: RULE-EXCEPTION-001]
[TYPE: RULE]
[STATUS: CANON]
[VISIBILITY: AUTHOR]

Ngoại lệ phải có ID riêng.

Không được biến một ngoại lệ thành quy luật chung.

---

# 14. LONG-TERM MYSTERIES

## 14.1. Linh hồn nguyên bản

[ID: MYST-SOUL-001]
[TYPE: MYSTERY]
[STATUS: AUTHOR_SECRET]
[VISIBILITY: AUTHOR]

Bí mật về linh hồn nguyên bản liên quan trực tiếp đến nguồn gốc của Trần Minh.

Trần Minh hiện tại là một linh hồn tân sinh sau luân hồi nhưng vẫn khuyết thiếu một phần.

Linh hồn nguyên bản vẫn tồn tại.

Chi tiết quan hệ giữa Trần Minh hiện tại và linh hồn nguyên bản là bí mật dài hạn.

---

## 14.2. Kẻ thần bí

[ID: MYST-ENTITY-001]
[TYPE: MYSTERY]
[STATUS: AUTHOR_SECRET]
[VISIBILITY: AUTHOR]

Tồn tại một thực thể / nhân vật thần bí liên quan đến linh hồn và nhân quả của Trần Minh.

Danh tính và bản chất chưa được phép giải thích hoàn toàn.

---

## 14.3. Món nợ nhân quả

[ID: MYST-DEBT-001]
[TYPE: MYSTERY]
[STATUS: AUTHOR_SECRET]
[VISIBILITY: AUTHOR]

Trước khi xuyên không, Trần Minh nghe thấy:

> “Hắn nợ ta.”

Điều này xác lập sự tồn tại của một món nợ nhân quả liên quan đến Trần Minh.

Bản chất món nợ chưa được giải thích hoàn toàn.

Không được tự ý bổ sung nguyên nhân hoặc kết quả.

---

## 14.4. Nguồn gốc Hệ thống

[ID: MYST-SYSTEM-001]
[TYPE: MYSTERY]
[STATUS: AUTHOR_SECRET]
[VISIBILITY: AUTHOR]

Nguồn gốc Hệ thống là một bí mật dài hạn.

---

## 14.5. Xuyên không

[ID: MYST-TRANSMIGRATION-001]
[TYPE: MYSTERY]
[STATUS: AUTHOR_SECRET]
[VISIBILITY: AUTHOR]

Cơ chế và nguyên nhân hoàn chỉnh của việc Trần Minh xuyên không chưa được công khai.

---

## 14.6. Hóa Thần Hải

[ID: MYST-SEA-001]
[TYPE: MYSTERY]
[STATUS: AUTHOR_SECRET]
[VISIBILITY: AUTHOR]

Hóa Thần Hải là một tuyến bí mật dài hạn.

Nguồn gốc và bản chất chưa được giải thích hoàn toàn.

---

## 14.7. Vùng Sương Mù

[ID: MYST-MIST-001]
[TYPE: MYSTERY]
[STATUS: AUTHOR_SECRET]
[VISIBILITY: AUTHOR]

Vùng Sương Mù là một tuyến bí mật dài hạn.

Chi tiết chưa được phép tiết lộ.

---

## 14.8. Các bí mật chưa giải

[ID: MYST-UNKNOWN-001]
[TYPE: MYSTERY_GROUP]
[STATUS: AUTHOR_SECRET]
[VISIBILITY: AUTHOR]

Mọi bí mật mới phải được cấp Mystery ID riêng.

---

# 15. CANON STATUS

> Đây là **registry**, không phải nơi chứa nội dung gốc. Nội dung thật nằm ở domain tương ứng.

## 15.1. CANON

Các Entity / Fact đã được xác lập.

```text
[STATUS: CANON]
```

Danh sách phải được duy trì khi hệ thống phát triển.

---

## 15.2. CHƯA CANON

```text
[STATUS: UNC]
```

Các đối tượng có thể tồn tại nhưng chưa phải sự thật.

---

## 15.3. GIẢ THUYẾT

```text
[STATUS: HYPOTHESIS]
```

Dùng cho suy luận hoặc phương án đang xem xét.

Format:

```text
[MYST-DEBT-001-H01]
[MYST-DEBT-001-H02]
```

Giả thuyết không được dùng như Canon.

---

## 15.4. BÍ MẬT TÁC GIẢ

```text
[STATUS: AUTHOR_SECRET]
```

Đây là thông tin Canon ở tầng tác giả nhưng chưa được phép tiết lộ.

---

## 15.5. ĐÃ LOẠI BỎ

```text
[STATUS: DEPRECATED]
```

Không dùng làm sự thật hiện tại.

Giữ lại để truy nguyên lịch sử khi cần.

---

## 15.6. MÂU THUẪN CHỜ XỬ LÝ

```text
[STATUS: CONFLICT]
```

Mọi mâu thuẫn chưa giải quyết phải được đưa vào đây.

Format:

```text
[CONFLICT: ENTITY-A]
[CONFLICT: ENTITY-B]

Vấn đề:
...

Nguồn A:
...

Nguồn B:
...

Trạng thái:
CHỜ TÁC GIẢ XÁC NHẬN
```

---

# 16. INDEX

> Index chỉ dùng để **tra cứu**. Không tạo bản sao nội dung Canon ở đây.

## 16.1. Chỉ mục tổng

### Character

```text
[CHAR-TRM-001] → 10.1
```

### Location

```text
[LOC-DALI-001] → 08.1
[LOC-THANHHA-001] → 08.2
[LOC-VANKHE-001] → 08.3
[LOC-LACSON-001] → 08.4
[LOC-LACTRAN-001] → 08.5
[LOC-LGT-001] → 08.6
[LOC-TDY-SECT-001] → 08.7
[LOC-TDY-CITY-001] → 08.8
[LOC-TDY-MOUNTAINS-001] → 08.9
[LOC-EASTSEA-001] → 08.10
```

### Faction

```text
[FACTION-TDY-001] → 09.1
```

### System

```text
[SYS-MAIN-001] → 11.1
[SYS-AUTO-CULT-001] → 11.2
[SYS-AUTO-SKILL-001] → 11.3
[SYS-AUTO-ART-001] → 11.4
[SYS-CLONE-001] → 11.5
[SYS-DUNGEON-001] → 11.6
```

### Mystery

```text
[MYST-SOUL-001] → 14.1
[MYST-ENTITY-001] → 14.2
[MYST-DEBT-001] → 14.3
[MYST-SYSTEM-001] → 14.4
[MYST-TRANSMIGRATION-001] → 14.5
[MYST-SEA-001] → 14.6
[MYST-MIST-001] → 14.7
```

---

## 16.2. Chỉ mục nhân vật

```text
CHAR-TRM-001 — Trần Minh
```

---

## 16.3. Chỉ mục địa điểm

```text
LOC-DALI-001 — Đại Ly
LOC-THANHHA-001 — Thanh Hà Tỉnh
LOC-VANKHE-001 — Vân Khê Phủ
LOC-LACSON-001 — Lạc Sơn Huyện
LOC-LACTRAN-001 — Lạc Trấn
LOC-LGT-001 — Lạc Gia Thôn
LOC-TDY-SECT-001 — Thanh Dương Tông
LOC-TDY-CITY-001 — Thanh Dương Thành
LOC-TDY-MOUNTAINS-001 — Thanh Dương Sơn Mạch
LOC-EASTSEA-001 — Đông Hải
```

---

## 16.4. Chỉ mục thế lực

```text
FACTION-TDY-001 — Thanh Dương Tông
```

---

## 16.5. Chỉ mục hệ thống

```text
SYS-MAIN-001 — Hệ thống
SYS-AUTO-CULT-001 — Tự động tu luyện
SYS-AUTO-SKILL-001 — Tự động kỹ năng
SYS-AUTO-ART-001 — Tự động Bách Nghệ
SYS-CLONE-001 — Tiểu Hóa Thân
SYS-DUNGEON-001 — Tự động Bí Cảnh
```

---

## 16.6. Chỉ mục quy luật

```text
RULE-POWER-001 — Quy luật quyền lực xã hội
RULE-SOCIAL-001 — Luật lệ xã hội
RULE-CAUS-001 — Nhân quả
RULE-SOUL-001 — Linh hồn
RULE-REALM-001 — Cảnh giới
RULE-DEPENDENCY-001 — Điều kiện / phụ thuộc
RULE-EXCEPTION-001 — Ngoại lệ
```

---

## 16.7. Chỉ mục vật phẩm

Chưa có danh sách Canon hoàn chỉnh.

---

## 16.8. Chỉ mục bí mật

```text
MYST-SOUL-001 — Linh hồn nguyên bản
MYST-ENTITY-001 — Kẻ thần bí
MYST-DEBT-001 — Món nợ nhân quả
MYST-SYSTEM-001 — Nguồn gốc Hệ thống
MYST-TRANSMIGRATION-001 — Xuyên không
MYST-SEA-001 — Hóa Thần Hải
MYST-MIST-001 — Vùng Sương Mù
```

---

## 16.9. Chỉ mục khái niệm

Các khái niệm quan trọng phải được cấp `TERM-*` hoặc `COSMO-*` / `RULE-*` tùy bản chất.

Ví dụ:

```text
COSMO-QI-001 — Linh khí
COSMO-SOUL-001 — Linh hồn
COSMO-CAUSALITY-001 — Nhân quả
CULT-DAO_HEART-001 — Đạo tâm
```

---

## 16.10. Chỉ mục quan hệ

Các quan hệ quan trọng:

```text
[REL: CHAR-TRM-001 -> LOC-LGT-001]
TYPE: ORIGIN

[REL: CHAR-TRM-001 -> FACTION-TDY-001]
TYPE: MEMBER

[REL: CHAR-TRM-001 -> SYS-MAIN-001]
TYPE: USER

[REL: CHAR-TRM-001 -> MYST-SOUL-001]
TYPE: CONNECTED_TO
STATUS: AUTHOR_SECRET

[REL: CHAR-TRM-001 -> MYST-DEBT-001]
TYPE: CONNECTED_TO
STATUS: AUTHOR_SECRET
```

---

# 17. ID SYSTEM SPECIFICATION

> Phần này là luật kỹ thuật của hệ thống ID. Không tùy tiện thay đổi format giữa chừng.

## 17.1. Section ID

Format:

```text
XX
XX.YY
XX.YY.ZZ
```

Ví dụ:

```text
10
10.1
10.1.1
```

Section ID chỉ biểu diễn **vị trí trong tài liệu**.

Không được dùng Section ID làm định danh duy nhất của một Entity.

---

## 17.2. Entity ID

Format:

```text
[CATEGORY]-[SHORTNAME]-[NNN]
```

Ví dụ:

```text
[CHAR-TRM-001]
[LOC-LGT-001]
[FACTION-TDY-001]
[SYS-MAIN-001]
[MYST-DEBT-001]
```

Entity ID phải ổn định.

---

## 17.3. Category

Prefix chuẩn:

```text
META
WORLD
COSMO
RULE
CULT
ART
RES
ITEM
CREA
LOC
FACTION
CHAR
SYS
EVENT
HIST
REL
MYST
TERM
INDEX
```

Không tạo prefix mới nếu category hiện tại đã đủ.

Nếu thật sự cần category mới, phải cập nhật bảng Category Registry trước.

---

## 17.4. Shortname

Shortname phải:

- Ngắn.
- Dễ nhận diện.
- Ổn định.
- Không chứa quá nhiều thông tin.
- Không mã hóa trạng thái.
- Không mã hóa vị trí hiện tại.

Không dùng:

```text
CHAR-TRM-LGT-PROTAGONIST-001
```

Nên dùng:

```text
CHAR-TRM-001
```

---

## 17.5. Number

Dùng ba chữ số:

```text
001
002
003
...
```

Không tái sử dụng số của Entity đã bị DEPRECATED.

---

## 17.6. Relation

Quan hệ không cần một số ID riêng nếu quan hệ đơn giản.

Format:

```text
[REL: ENTITY-A -> ENTITY-B]
[TYPE: RELATION_TYPE]
[STATUS: STATUS]
```

Ví dụ:

```text
[REL: CHAR-TRM-001 -> LOC-LGT-001]
[TYPE: ORIGIN]
[STATUS: CANON]
```

Nếu quan hệ phức tạp hoặc cần được tham chiếu độc lập:

```text
[REL-001]
[FROM: CHAR-TRM-001]
[TO: MYST-DEBT-001]
[TYPE: CONNECTED_TO]
[STATUS: AUTHOR_SECRET]
```

---

## 17.7. Hypothesis ID

Format:

```text
[ENTITY-ID-H01]
[ENTITY-ID-H02]
```

Ví dụ:

```text
[MYST-DEBT-001-H01]
[MYST-DEBT-001-H02]
```

---

## 17.8. Event ID

Format:

```text
[EVENT-ARC1-001]
[EVENT-GLOBAL-001]
[EVENT-TDY-001]
```

---

## 17.9. Fact ID

Chỉ dùng khi cần trỏ tới một fact cụ thể.

Format:

```text
[FACT-XXX-001]
```

Không cấp Fact ID cho mọi câu.

---

# 18. ENTRY STANDARD

Mọi Entity quan trọng nên dùng template:

```md
## Tên Entity

[ID: CATEGORY-SHORTNAME-001]
[TYPE: OBJECT_TYPE]
[STATUS: CANON]
[VISIBILITY: PUBLIC]

### Tổng quan

...

### Đặc điểm

...

### Quan hệ

[REL: ENTITY-A -> ENTITY-B]
[TYPE: RELATION_TYPE]
[STATUS: CANON]

### Canon liên quan

- [[Entity A]]
- [[Entity B]]

### Ghi chú

...
```

Đối với Entity bí mật:

```md
[STATUS: AUTHOR_SECRET]
[VISIBILITY: AUTHOR]
```

Đối với Entity chưa Canon:

```md
[STATUS: UNC]
```

---

# 19. QUY TẮC LIÊN KẾT OBSIDIAN

Ưu tiên wikilink:

```md
[[Trần Minh]]
[[Lạc Gia Thôn]]
[[Thanh Dương Tông]]
```

Khi cần liên kết đến heading:

```md
[[01_WORLD_BIBLE 1#10.1. Trần Minh]]
```

Không tạo block ID cho mọi đoạn văn.

Block ID chỉ dùng cho fact cần tham chiếu cực kỳ chính xác:

```md
Trần Minh hiện tại là một linh hồn tân sinh sau luân hồi. ^fact-trm-soul-new
```

---

# 20. QUY TẮC CHỐNG TRÙNG DỮ LIỆU

Một sự thật chỉ có **một nguồn gốc chính**.

Ví dụ:

> Trần Minh xuất thân từ Lạc Gia Thôn.

Nguồn chính:

```text
CHAR-TRM-001
```

Quan hệ:

```text
[REL: CHAR-TRM-001 -> LOC-LGT-001]
[TYPE: ORIGIN]
```

Index chỉ chứa:

```text
CHAR-TRM-001 → 10.1
```

Không sao chép nguyên đoạn lore sang Index.

---

# 21. QUY TẮC THAY ĐỔI

Khi đổi tên Entity:

- Không đổi Entity ID.

Khi đổi vị trí Entity:

- Không đổi Entity ID.

Khi thêm thông tin:

- Cập nhật Entity hiện tại.

Khi thông tin bị thay thế:

- Không tạo Entity mới nếu vẫn là cùng một đối tượng.
- Cập nhật Status / Version khi cần.

Khi một đối tượng hoàn toàn khác xuất hiện:

- Cấp Entity ID mới.

Khi một Entity bị loại bỏ:

```text
[STATUS: DEPRECATED]
```

Không tái sử dụng ID đó.

---

# 22. CANON CHECKLIST

Trước khi thêm một thông tin mới:

```text
[ ] Thông tin này đã được tác giả xác nhận chưa?
[ ] Có Entity ID chưa?
[ ] Có Status chưa?
[ ] Có Visibility chưa?
[ ] Có Relation với đối tượng liên quan chưa?
[ ] Có mâu thuẫn với Canon hiện tại không?
[ ] Có cần Event ID / Mystery ID / Rule ID không?
[ ] Có đang sao chép một fact đã tồn tại ở nơi khác không?
[ ] Nếu chưa Canon, đã đánh dấu UNC / HYPOTHESIS chưa?
[ ] Nếu là bí mật, đã đánh dấu AUTHOR_SECRET chưa?
```

---

# 23. QUY TẮC KHI AI TRA CỨU

Khi được yêu cầu trả lời về một chủ đề:

### Bước 1 — Xác định Entity

Tìm:

```text
[ID: ...]
```

### Bước 2 — Kiểm tra Status

```text
CANON
UNC
HYPOTHESIS
AUTHOR_SECRET
DEPRECATED
CONFLICT
```

### Bước 3 — Kiểm tra Visibility

Không tiết lộ thông tin vượt quá quyền biết của đối tượng đang được xét.

### Bước 4 — Kiểm tra Relation

Tìm các:

```text
[REL: ...]
```

liên quan trực tiếp.

### Bước 5 — Kiểm tra Timeline

Nếu có yếu tố thời gian, kiểm tra:

```text
EVENT-*
HIST-*
```

### Bước 6 — Kiểm tra Mystery

Nếu chủ đề liên quan bí mật, kiểm tra:

```text
MYST-*
```

### Bước 7 — Nếu thiếu dữ liệu

Không tự điền.

Phải ghi:

> **CHƯA CÓ CANON.**

hoặc đề xuất dưới dạng:

> **HYPOTHESIS.**

---

# 24. KIẾN TRÚC FILE VỀ SAU

World Bible 1 là Canon Core.

Các file chi tiết có thể được tách thành:

```text
01_WORLD_BIBLE 1.md
02_CHARACTERS.md
03_LOCATIONS.md
04_FACTIONS.md
05_CULTIVATION.md
06_CREATURES.md
07_ITEMS.md
08_EVENTS.md
09_MYSTERIES.md
10_TIMELINE.md
11_INDEX.md
```

World Bible 1 không cần chứa toàn bộ lore chi tiết.

Nó phải trả lời được:

> **Thế giới có những gì?**

> **Mỗi thứ có ID gì?**

> **Nó thuộc loại gì?**

> **Nó đang ở trạng thái Canon nào?**

> **Ai được biết?**

> **Nó liên quan đến cái gì?**

> **Muốn tra cứu chi tiết thì đi đâu?**

---

# 25. KIẾN TRÚC TỔNG THỂ

```text
                         WORLD BIBLE
                              │
              ┌───────────────┴───────────────┐
              │                               │
          CANON CORE                     DETAIL FILES
              │                               │
       01_WORLD_BIBLE 1                ┌──────┼──────┐
              │                        │      │      │
        ┌─────┼─────┐              CHAR  LOCATIONS FACTIONS
        │     │     │                │      │      │
      RULES WORLD SYSTEMS         EVENTS  ITEMS  CREATURES
        │     │     │
        └─────┼─────┘
              │
          RELATIONS
              │
          MYSTERIES
              │
           TIMELINE
              │
            INDEX
```

---

# 26. NGUYÊN TẮC CUỐI CÙNG

[ID: META-CORE-001]
[TYPE: META]
[STATUS: CANON]
[VISIBILITY: AUTHOR]

World Bible phải ưu tiên:

> **Tra cứu được.**

> **Liên kết được.**

> **Không mâu thuẫn.**

> **Không mất lịch sử.**

> **Không nhầm giữa Canon và suy đoán.**

> **Không nhầm giữa điều tác giả biết và điều nhân vật biết.**

> **Không phụ thuộc vào vị trí hiện tại của một heading.**

> **Không làm thế giới xoay quanh một nhân vật nếu Canon không yêu cầu.**

Nguyên tắc kỹ thuật quan trọng nhất:

```text
SECTION ID = vị trí

ENTITY ID = danh tính

RELATION = liên kết

STATUS = trạng thái Canon

VISIBILITY = quyền được biết

INDEX = đường dẫn tra cứu

SOURCE = nơi chứa sự thật gốc
```

Và:

> **Entity ID không được thay đổi chỉ vì cấu trúc tài liệu thay đổi.**

---

# END OF WORLD BIBLE 1
