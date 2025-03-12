# LG_TOOLREQ

Tool Requirements

## Alanlar ve Açıklamaları

| Level | Product ID | Field Name | Field Type | Field Size | Field Offset | Türkçe Açıklama | Expression |
| ----- | ---------- | ---------- | ---------- | ---------- | ------------ | --------------- | ---------- |
| 1 | 0 | LOGICALREF | Longint | 4 | 0 | Araç gereksinimi log. Ref. | Tool Requirement Logical Reference |
| 1 | 0 | OPREQREF | Longint | 4 | 4 | Operasyon İhtiyaçları Ref. | Operation Requirement Reference |
| 1 | 0 | LINENO_ | Longint | 4 | 8 | Satır Numarası | Line Number |
| 1 | 0 | TOOLREF | Longint | 4 | 12 | Araç ref. | Tool Reference |
| 1 | 0 | AMOUNT | Double | 8 | 16 | Miktar | Quantity |
| 1 | 0 | UOMREF | Longint | 4 | 24 | Birim referansı | Unit Reference |

## İlişkiler - Relations

| Level | Product ID | Source Field | Destination Table | Destination Field | Relation Type | Extra Condition |
| ----- | ---------- | ------------ | ---------------- | ---------------- | ------------- | --------------- |
| 1 | 0 | OPREQREF | L_OPRTREQ | LOGICALREF | one-to-one |  |
| 1 | 0 | TOOLREF | L_ITEMS | LOGICALREF | one-to-many |  |
| 1 | 0 | UOMREF | L_UNITSETL | LOGICALREF | one-to-one |  |

## Indexler

| Level | Product ID | Index Name | Attributes | Segment No | Segment Field | Sense |
| ----- | ---------- | ---------- | ---------- | ---------- | ------------- | ----- |
| 1 | 0 | Index1 | Unique + Not Null | 1 | LOGICALREF | Ascending |
| 1 | 0 | Index2 | Unique + Not Null | 1 | OPREQREF | Ascending |
| 1 | 0 | Index2 | Unique + Not Null | 2 | LINENO_ | Ascending |
| 1 | 0 | Index3 | Unique + Not Null | 1 | OPREQREF | Ascending |
| 1 | 0 | Index3 | Unique + Not Null | 2 | TOOLREF | Ascending |
