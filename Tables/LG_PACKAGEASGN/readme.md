# LG_PACKAGEASGN

nan

## Alanlar ve Açıklamaları

| Level | Product ID | Field Name | Field Type | Field Size | Field Offset | Türkçe Açıklama | Expression |
| ----- | ---------- | ---------- | ---------- | ---------- | ------------ | --------------- | ---------- |
| 2 | 1 | LOGICALREF | Longint | 4 | 0 | Logical Reference | Logical Reference |
| 2 | 1 | PACKFICHEREF | Longint | 4 | 4 | Paket fişi log. Ref. | PACKAGEFICHE LOGICALREF |
| 2 | 1 | PACKLNREF | Longint | 4 | 8 | Paket fişi satırı log. Ref. | PACKAGEFCLN LOGICALREF |
| 2 | 1 | PARENTPACKLNREF | Longint | 4 | 12 | Paket fişi satırı log. Ref. | PACKAGEFCLN LOGICALREF |
| 2 | 1 | ITEMREF | Longint | 4 | 16 | Malzemeler Log. Ref. | ITEMS LOGICALREF |
| 2 | 1 | UOMREF | Longint | 4 | 20 | Birim seti log. Ref. | UNITSETL LOGICALREF |
| 2 | 1 | ASGNFICHETYPE | Integer | 2 | 24 | İlişkili fiş türü; 1. Sipariş; 2. İrsaliye | Type of Related Voucher;1. Order;2. Dispatch |
| 2 | 1 | ASGNFICHEREF | Longint | 4 | 26 | Fiş Atama Ref. 1. Sipariş; 2. İrsaliye | ASSIGNFICHEREF;1. Order;2. Dispatch |
| 2 | 1 | ASGNTRANSREF | Longint | 4 | 30 | Hareket Atama Ref. 1. Sipariş; 2. İrsaliye | ASSGNTRANSREF;1. Order;2. Dispatch |
| 2 | 1 | AMOUNT | Double | 8 | 34 | Tutar | Amount |
| 2 | 1 | ASGNSLTRANREF | Longint | 4 | 42 | SLTRANS LOGICALREF | SLTRANS LOGICALREF |
| 2 | 1 | MAINITEMLNREF | Longint | 4 | 46 | Paket fişi satırı log. Ref. | PACKAGEFCLN LOGICALREF |

## İlişkiler - Relations

| Level | Product ID | Source Field | Destination Table | Destination Field | Relation Type | Extra Condition |
| ----- | ---------- | ------------ | ---------------- | ---------------- | ------------- | --------------- |
| 2 | 1 | PACKFICHEREF | L_PACKAGEFICHE | LOGICALREF | one-to-one |  |
| 2 | 1 | PACKLNREF | L_PACKAGEFCLN | LOGICALREF | one-to-one |  |
| 2 | 1 | PARENTPACKLNREF | L_PACKAGEFCLN | LOGICALREF | one-to-one |  |
| 2 | 1 | ITEMREF | L_ITEMS | LOGICALREF | one-to-one |  |
| 2 | 1 | UOMREF | L_UNITSETL | LOGICALREF | one-to-one |  |
| 2 | 1 | ASGNFICHEREF | L_ORFICHE | LOGICALREF | one-to-one |  |
| 2 | 1 | ASGNFICHEREF | L_STFICHE | LOGICALREF | one-to-one |  |
| 2 | 1 | ASGNTRANSREF | L_ORFLINE | LOGICALREF | one-to-one |  |
| 2 | 1 | ASGNTRANSREF | L_STLINE | LOGICALREF | one-to-one |  |
| 2 | 1 | ASGNSLTRANREF | L_SLTRANS | LOGICALREF | one-to-one |  |

## Indexler

| Level | Product ID | Index Name | Attributes | Segment No | Segment Field | Sense |
| ----- | ---------- | ---------- | ---------- | ---------- | ------------- | ----- |
| 2 | 1 | Index1 | Unique + Not Null | 1 | LOGICALREF | Ascending |
| 2 | 1 | Index2 | Duplicate + Not Null | 1 | PACKFICHEREF | Ascending |
| 2 | 1 | Index3 | Unique + Not Null | 1 | PACKLNREF | Ascending |
