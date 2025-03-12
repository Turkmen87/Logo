# LG_PEGGING

Transaction Connections

## Alanlar ve Açıklamaları

| Level | Product ID | Field Name | Field Type | Field Size | Field Offset | Türkçe Açıklama | Expression |
| ----- | ---------- | ---------- | ---------- | ---------- | ------------ | --------------- | ---------- |
| 1 | 1 | LOGICALREF | Longint | 4 | 0 | Hareket bağlantısı log. Ref. | Transaction Connection Logical Reference |
| 1 | 1 | PEGTYPE | Integer | 2 | 4 | Hareket bağlantısı türü ;0 Giriş bağlantısı;1 Çıkış bağlantısı | Transaction Connection Type ;0 Input Connection;1 Output Connection |
| 1 | 1 | PEGREF | Longint | 4 | 6 | Hareket bağlantısı ref. | Transaction Connection Reference |
| 1 | 1 | RELTYPE | Integer | 2 | 10 | İlişki türü ;FOR PEGTYPE = 0, 0 Üret,m emri;FOR PEGTYPE = 0, 1 Satınalma siparişi;FOR PEGTYPE = 1, 0 Üretim emri;FOR PEGTYPE = 1, 0 Satış fişi | Relation Type ;FOR PEGTYPE = 0, 0 Production Order;FOR PEGTYPE = 0, 1 Purchase Order;FOR PEGTYPE = 1, 0 Production Order;FOR PEGTYPE = 1, 0 Sales Order |
| 1 | 1 | PRODORDREF | Longint | 4 | 12 | Üretim Emri Referansı | Production Order Reference |
| 1 | 1 | SUBCONTREF | Longint | 4 | 16 | Fason sipariş ref. | Subcontracting Order Reference |
| 1 | 1 | PORDFICHEREF | Longint | 4 | 20 | Sipariş fişi Ref. | Order Voucher Reference |
| 1 | 1 | PORDLINEREF | Longint | 4 | 24 | Sipariş satırı ref. | Order Line Reference |
| 1 | 1 | ITEMREF | Longint | 4 | 28 | Malzeme Kartı Referansı | Item Card Reference |
| 1 | 1 | AMOUNT | Double | 8 | 32 | Miktar | Quantity |
| 1 | 1 | UOMREF | Longint | 4 | 40 | Birim referansı | Unit Reference |
| 1 | 1 | CANCHANGE | Byte | 1 | 44 | Değişebilir | Changeable |
| 1 | 1 | DISPLINEREF | Longint | 4 | 45 | İş emri ref. | Work Order Reference |
| 1 | 1 | PRODLINEREF | Longint | 4 | 49 | Üretim Emri Satır Ref. | Production Order Line Reference |
| 1 | 1 | OTHERPEGREF | Longint | 4 | 53 | Diğer fiyat tespit referansı | Other Pegging Reference |
| 1 | 1 | PERIODNR | Longint | 4 | 57 | Periyot numarası | Period Number |
| 1 | 1 | MRPPROPREF | Longint | 4 | 61 | MRP Önerisi Ref. | MRP Proposal Reference |
| 1 | 1 | PDEMFICHEREF | Longint | 4 | 65 | Talep Fişi Log. Ref. | DEMANDFICHE LOGICALREF |
| 1 | 1 | PDEMLINEREF | Longint | 4 | 69 | Talep Satırı Log. Ref. | DEMANDLINE LOGICALREF |

## İlişkiler - Relations

| Level | Product ID | Source Field | Destination Table | Destination Field | Relation Type | Extra Condition |
| ----- | ---------- | ------------ | ---------------- | ---------------- | ------------- | --------------- |
| 1 | 1 | PRODORDREF | L_PRODORD | LOGICALREF | one-to-one |  |
| 1 | 1 | PORDFICHEREF | L_ORFICHE | LOGICALREF | one-to-one |  |
| 1 | 1 | PORDLINEREF | L_ORFLINE | LOGICALREF | one-to-one |  |
| 1 | 1 | ITEMREF | L_ITEMS | LOGICALREF | one-to-one |  |
| 1 | 1 | UOMREF | L_UNITSETL | LOGICALREF | one-to-one |  |
| 1 | 1 | DISPLINEREF | L_DISPLINE | LOGICALREF | one-to-one |  |
| 1 | 1 | PRODLINEREF | L_POLINE | LOGICALREF | one-to-one |  |
| 1 | 1 | OTHERPEGREF | L_PEGGING | LOGICALREF | one-to-one |  |
| 1 | 1 | MRPPROPREF | L_MRPPROPOSAL | LOGICALREF | one-to-one |  |

## Indexler

| Level | Product ID | Index Name | Attributes | Segment No | Segment Field | Sense |
| ----- | ---------- | ---------- | ---------- | ---------- | ------------- | ----- |
| 1 | 1 | Index1 | Unique + Not Null | 1 | LOGICALREF | Ascending |
| 1 | 1 | Index2 | Duplicate + Not Null | 1 | PEGTYPE | Ascending |
| 1 | 1 | Index2 | Duplicate + Not Null | 2 | PEGREF | Ascending |
| 1 | 1 | Index3 | Duplicate + Not Null | 1 | PEGREF | Ascending |
| 1 | 1 | Index3 | Duplicate + Not Null | 2 | PEGTYPE | Ascending |
| 1 | 1 | Index3 | Duplicate + Not Null | 3 | RELTYPE | Ascending |
| 1 | 1 | Index4 | Duplicate + Not Null | 1 | PORDFICHEREF | Ascending |
| 1 | 1 | Index5 | Duplicate + Not Null | 1 | PORDLINEREF | Ascending |
