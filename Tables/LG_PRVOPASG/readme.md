# LG_PRVOPASG

Operation Relations

## Alanlar ve Açıklamaları

| Level | Product ID | Field Name | Field Type | Field Size | Field Offset | Türkçe Açıklama | Expression |
| ----- | ---------- | ---------- | ---------- | ---------- | ------------ | --------------- | ---------- |
| 1 | 1 | LOGICALREF | Longint | 4 | 0 | Önceki operasyon ilişkisi log. ref. | Previous Operation Relation Logical Reference |
| 1 | 1 | ROUTINGREF | Longint | 4 | 4 | Üretim rotası ref. | Production Route Reference |
| 1 | 1 | ROUTLINEREF | Longint | 4 | 8 | Rota satır ref. | Route Line Reference |
| 1 | 1 | LINEOPREF | Longint | 4 | 12 | Satır İşlem Ref. | Line Operation Reference |
| 1 | 1 | PREVOPREF | Longint | 4 | 16 | Önceki operasyon ref. | Previous Operation Reference |
| 1 | 1 | OVERLAPPER | Double | 8 | 20 | Örtüşme oranı | Overlapping Rate |

## İlişkiler - Relations

| Level | Product ID | Source Field | Destination Table | Destination Field | Relation Type | Extra Condition |
| ----- | ---------- | ------------ | ---------------- | ---------------- | ------------- | --------------- |
| 1 | 1 | ROUTINGREF | L_ROUTING | LOGICALREF | one-to-one |  |
| 1 | 1 | ROUTLINEREF | L_RTNGLINE | LOGICALREF | one-to-one |  |
| 1 | 1 | LINEOPREF | L_OPERTION | LOGICALREF | one-to-one |  |
| 1 | 1 | PREVOPREF | L_OPERTION | LOGICALREF | one-to-one |  |

## Indexler

| Level | Product ID | Index Name | Attributes | Segment No | Segment Field | Sense |
| ----- | ---------- | ---------- | ---------- | ---------- | ------------- | ----- |
| 1 | 1 | Index1 | Unique + Not Null | 1 | LOGICALREF | Ascending |
| 1 | 1 | Index2 | Duplicate + Not Null | 1 | ROUTINGREF | Ascending |
| 1 | 1 | Index2 | Duplicate + Not Null | 2 | PREVOPREF | Ascending |
| 1 | 1 | Index3 | Duplicate + Not Null | 1 | ROUTLINEREF | Ascending |
| 1 | 1 | Index3 | Duplicate + Not Null | 2 | PREVOPREF | Ascending |
| 1 | 1 | Index4 | Unique + Not Null | 1 | PREVOPREF | Ascending |
| 1 | 1 | Index4 | Unique + Not Null | 2 | ROUTLINEREF | Ascending |
