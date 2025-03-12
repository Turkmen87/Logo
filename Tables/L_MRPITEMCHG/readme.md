# L_MRPITEMCHG

nan

## Alanlar ve Açıklamaları

| Level | Product ID | Field Name | Field Type | Field Size | Field Offset | Türkçe Açıklama | Expression |
| ----- | ---------- | ---------- | ---------- | ---------- | ------------ | --------------- | ---------- |
| 0 | 0 | LOGICALREF | Longint | 4 | 0 | Değişmiş MRP Kalemleri Logical Ref. | Changed MRP Items Logical Reference |
| 0 | 0 | ITEMREF | Longint | 4 | 4 | Malzeme Kartları Referansı | Item Cards Reference |
| 0 | 0 | PARITEMREF | Longint | 4 | 8 | Malzeme Kartları Referansı | Item Cards Reference |

## İlişkiler - Relations

*Bu tablo için ilişki bulunmamaktadır.*

## Indexler

| Level | Product ID | Index Name | Attributes | Segment No | Segment Field | Sense |
| ----- | ---------- | ---------- | ---------- | ---------- | ------------- | ----- |
| 0 | 0 | Index1 | Unique + Not Null | 1 | LOGICALREF | Ascending |
