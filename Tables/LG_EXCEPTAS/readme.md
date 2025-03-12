# LG_EXCEPTAS

Exception Assignments

## Alanlar ve Açıklamaları

| Level | Product ID | Field Name | Field Type | Field Size | Field Offset | Türkçe Açıklama | Expression |
| ----- | ---------- | ---------- | ---------- | ---------- | ------------ | --------------- | ---------- |
| 0 | 0 | LOGICALREF | Longint | 4 | 0 | İstisnai Durum Atamaları Log. Ref. | Exception Assignment Logical Reference |
| 0 | 0 | CONNECTIONREF | Longint | 4 | 4 | Entegrasyon Bağlantı Kodu Log. Ref. | Integration Connection Code Logical Reference |
| 0 | 0 | SELNR | Integer | 2 | 8 | Filtre Türü | Filter Type |
| 0 | 0 | SELTYPE | Byte | 1 | 10 | Rezerve | Reserved |
| 0 | 0 | GRPVALUE | ZString | 25 | 11 | Rezerve | Reserved |
| 0 | 0 | BEGVALUE | ZString | 25 | 36 | Başlangıç Değeri | Begin Value |
| 0 | 0 | ENDVALUE | ZString | 25 | 61 | Bitiş Değeri | End Value |

## İlişkiler - Relations

| Level | Product ID | Source Field | Destination Table | Destination Field | Relation Type | Extra Condition |
| ----- | ---------- | ------------ | ---------------- | ---------------- | ------------- | --------------- |
| 0 | 0 | nan | L_EMPLOYEE | LOGICALREF | one-to-one | SOURCETYPE = 0 |
| 0 | 0 | nan | L_EMPGROUP | LOGICALREF | one-to-one | SOURCETYPE = 1 |
| 0 | 0 | nan | L_WORKSTAT | LOGICALREF | one-to-one | SOURCETYPE = 2 |
| 0 | 0 | nan | L_WSGRPF | LOGICALREF | one-to-one | SOURCETYPE = 3 |
| 0 | 0 | nan | L_EXCEPT | LOGICALREF | one-to-one |  |

## Indexler

| Level | Product ID | Index Name | Attributes | Segment No | Segment Field | Sense |
| ----- | ---------- | ---------- | ---------- | ---------- | ------------- | ----- |
| 0 | 0 | Index1 | Unique + Not Null | 1 | LOGICALREF | Ascending |
| 0 | 0 | Index2 | Duplicate + Not Null | 1 | PARENTTYPE | Ascending |
| 0 | 0 | Index2 | Duplicate + Not Null | 2 | PARENTREF | Ascending |
