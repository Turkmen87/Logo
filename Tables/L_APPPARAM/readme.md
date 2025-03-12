# L_APPPARAM

nan

## Alanlar ve Açıklamaları

| Level | Product ID | Field Name | Field Type | Field Size | Field Offset | Türkçe Açıklama | Expression |
| ----- | ---------- | ---------- | ---------- | ---------- | ------------ | --------------- | ---------- |
| 0 | 0 | LOGICALREF | Longint | 4 | 0 |  |  |
| 0 | 0 | USERNR | Integer | 2 | 4 |  |  |
| 0 | 0 | TOPTENTYPE | Integer | 2 | 6 |  |  |
| 0 | 0 | TOPTENINTERVAL | Double | 8 | 8 |  |  |
| 0 | 0 | ITEMTREEVIEW | Byte | 1 | 16 |  |  |

## İlişkiler - Relations

*Bu tablo için ilişki bulunmamaktadır.*

## Indexler

| Level | Product ID | Index Name | Attributes | Segment No | Segment Field | Sense |
| ----- | ---------- | ---------- | ---------- | ---------- | ------------- | ----- |
| 0 | 0 | Index1 | Unique + Not Null | 1 | LOGICALREF | Ascending |
| 0 | 0 | Index2 | Unique + Not Null | 1 | USERNR | Ascending |
