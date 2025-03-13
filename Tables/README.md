# Logo ERP Veritabanı Tabloları  

Bu klasör, **LDDS.xls dosyasındaki bilgilerden yola çıkarak hazırlanmış veritabanı tabloları** ile ilgili dökümanları içerir.  

## 📂 İçerik  

- **Tablo Alanları** – Tablolardaki sütunların açıklamaları  
- **İndeksler** – Her tablonun indeks bilgileri  
- **İlişkiler** – Tablolar arası ilişkiler  

# Logo ERP Veritabanı Dökümantasyonu

Bu dökümantasyon, LogoWings ve LogoTiger ERP sistemlerinin MS SQL veritabanı yapısını detaylı olarak açıklamaktadır. Logo ERP sisteminin veritabanı yapısı, tablo isimleri, alan açıklamaları ve tablolar arası ilişkileri içermektedir.

Bu repo, geliştirici, veri analisti, danışman ve sistem yöneticileri için bir başvuru kaynağı olarak hazırlanmıştır.

## İçindekiler

- [Genel Tablo Yönetimi](#genel-tablo-yönetimi)
  - [Adres Bilgileri](#adres-bilgileri)
  - [Banka Bilgileri](#banka-bilgileri)
  - [Vergi Dairesi Bilgileri](#vergi-dairesi-bilgileri)
  - [Doküman Yönetim Tabloları](#doküman-yönetim-tabloları)
  - [Satış Yönetim Tabloları](#satış-yönetim-tabloları)
  - [Satış Elemanı Tablosu](#satış-elemanı-tablosu)
  - [Yardımcı Bilgi Tabloları](#yardımcı-bilgi-tabloları)
  - [Kullanıcı İzleme Tablosu](#kullanıcı-izleme-tablosu)
  - [Organizasyon Tabloları](#organizasyon-tabloları)
  - [GTIP Tabloları](#gtip-tabloları)
  - [Banka Tabloları](#banka-tabloları)
  - [Cari Hesap Tabloları](#cari-hesap-tabloları)
  - [Çek/Senet Tabloları](#çeksenet-tabloları)
  - [Stok Tabloları](#stok-tabloları)
  - [Muhasebe Tabloları](#muhasebe-tabloları)
  - [Kasa Tabloları](#kasa-tabloları)
  - [Satış/Sipariş Tabloları](#satışsipariş-tabloları)
  - [Üretim Tabloları](#üretim-tabloları)
  - [Kalite Kontrol Tabloları](#kalite-kontrol-tabloları)
  - [Hizmet Tabloları](#hizmet-tabloları)
  - [Çalışan Tabloları](#çalışan-tabloları)
  - [Ödeme/Tahsilat Tabloları](#ödemetahsilat-tabloları)
  - [Özellik Tabloları](#özellik-tabloları)
  - [Diğer Tablolar](#diğer-tablolar)
  - [Firma Bağımsız Tablolar](#firma-bağımsız-tablolar)
- [Kayıt Numaralama Şablonları](#kayıt-numaralama-şablonları)
- [Logo Çek Tabloları](#logo-çek-tabloları)
- [Bazı Önemli Tabloların Önemli Alanları](#bazı-önemli-tabloların-önemli-alanları)
  - [Fatura Tabloları](#fatura-tabloları)
  - [Stok Fişleri](#stok-fişleri)
  - [Stok Kartları](#stok-kartları)
  - [Cari Hesap Kartları](#cari-hesap-kartları)
  - [Cari Hesap Hareketleri](#cari-hesap-hareketleri)
  - [Çek/Senet İşlemleri](#çeksenet-işlemleri)
- [Logo Tablo Yapısı Sınıflandırması](#logo-tablo-yapısı-sınıflandırması)
- [Logo Tablo İsimleri Listesi](#logo-tablo-isimleri-listesi)

## Genel Tablo Yönetimi

### Adres Bilgileri

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| L_COUNTRY | Ülke bilgileri |
| L_CITY | İl bilgileri |
| L_POSTCODE | Posta kodları |
| L_TOWN | İlçe bilgileri |
| L_DISTRICT | Semt bilgileri |

### Banka Bilgileri

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| L_BANKCODE | Banka bilgileri |
| L_BNBRANCH | Şube bilgileri |

### Vergi Dairesi Bilgileri

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| L_TAXOFFICE | Vergi daireleri |

### Doküman Yönetim Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| L_LDOCFOLD | Doküman katalog bilgisi |
| L_LDOCITEM | Doküman tanımları |

### Satış Yönetim Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| [LG_ACTPEPL](../../Tables/LG_ACTPEPL) | Satış Faaliyetine Bağlı Kişiler |
| [LG_CATEGLISTS](../../Tables/LG_CATEGLISTS) | Kategoriler |
| [LG_CNTSLSMASG](../../Tables/LG_CNTSLSMASG) | Satış Elemanı-İlgili Kişi Bağlantı |
| [LG_CONTACTS](../../Tables/LG_CONTACTS) | İlgili Kişiler |
| [LG_CSTVND](../../Tables/LG_CSTVND) | Müşteri |
| [LG_CVINDASG](../../Tables/LG_CVINDASG) | Müşteri-Endüstri Bağlantı |
| [LG_INDUSTRY](../../Tables/LG_INDUSTRY) | Endüstri/Sektör |
| [LG_OFFER](../../Tables/LG_OFFER) | Teklif |
| [LG_SATI](../../Tables/LG_SATI) | Satış Faaliyetleri(m) Penceresi Genel ve Kişisel İşlemler |
| [LG_SATIFILTER](../../Tables/LG_SATIFILTER) | Satış Faaliyetleri(m) Penceresi Genel ve Kişisel İşlemler Filtre Tanımları |
| [LG_SLSACTIV](../../Tables/LG_SLSACTIV) | Satış Faaliyetleri |
| [LG_SLSCLREL](../../Tables/LG_SLSCLREL) | Satış Temsilcisi-Müşteri Bağlantı (CRM Seti) |
| [LG_SLSFILES](../../Tables/LG_SLSFILES) | Satış Dosyaları |
| [LG_SLSOPPOR](../../Tables/LG_SLSOPPOR) | Satış Fırsatları |

### Satış Elemanı Tablosu

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| [LG_SLSMAN](../../Tables/LG_SLSMAN) | Satış Temsilcileri ve Plasiyerler |

### Yardımcı Bilgi Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| L_FRGTYPES | Taşıma tipleri |
| L_SHPAGENT | Taşıyıcı firmalar |
| L_SHPTYPES | Taşıma şekli |
| L_TRADGRP | Ticari işlem grubu |

### Kullanıcı İzleme Tablosu

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| [LG_XXX_SYSLOG](../../Tables/LG_SYSLOG) | Kullanıcı İzleme |

### Organizasyon Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| L_ORGDEFS | Organizasyon Şeması |
| L_ORGDOC | Pozisyon açıklamalarının(uzun text) |
| L_POSDEFS | Org.Şeması Pozisyonları |

### GTIP Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| L_GTIP_CODE | Gtip kodları |
| L_GTIP_DEF | Gtip tanımları |

### Banka Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| [LG_XXX_XX_BNFICHE](../../Tables/LG_BNFICHE) | Banka fişleri |
| [LG_XXX_XX_BNFLINE](../../Tables/LG_BNFLINE) | Banka hareketleri |
| [LG_XXX_XX_BNTOTFIL](../../Tables/LG_BNTOTFIL) | Banka aylık toplamları |
| [LG_XXX_BANKACC](../../Tables/LG_BANKACC) | Banka hesapları |
| [LG_XXX_BNCARD](../../Tables/LG_BNCARD) | Bankalar |

### Cari Hesap Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| [LG_XXX_XX_CLFICHE](../../Tables/LG_CLFICHE) | Cari hesap fişleri |
| [LG_XXX_XX_CLFLINE](../../Tables/LG_CLFLINE) | Cari hesap hareketleri |
| [LG_XXX_XX_CLRNUMS](../../Tables/LG_CLRNUMS) | Cari hesap risk tabloları |
| [LG_XXX_XX_CLTOTFIL](../../Tables/LG_CLTOTFIL) | Cari hesap aylık toplamları |
| [LG_XXX_CLCARD](../../Tables/LG_CLCARD) | Cari hesap kartları |
| [LG_XXX_CLINTEL](../../Tables/LG_CLINTEL) | Cari hesap istihbarat bilgileri |

### Çek/Senet Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| [LG_XXX_XX_CSCARD](../../Tables/LG_CSCARD) | Çek/Senet kartları |
| [LG_XXX_XX_CSROLL](../../Tables/LG_CSROLL) | Çek/Senet bordroları |
| [LG_XXX_XX_CSTRANS](../../Tables/LG_CSTRANS) | Çek/Senet hareketleri |

### Stok Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| [LG_XXX_XX_STFICHE](../../Tables/LG_STFICHE) | Stok fişleri |
| [LG_XXX_XX_STLINE](../../Tables/LG_STLINE) | Malzeme hareketleri |
| [LG_XXX_XX_STINVTOT](../../Tables/LG_STINVTOT) | Günlük malzeme ambar toplamları |
| [LG_XXX_XX_STINVENS](../../Tables/LG_STINVENS) | Malzeme alış/satış aylık toplamları |
| [LG_XXX_ITEMS](../../Tables/LG_ITEMS) | Malzemeler |
| [LG_XXX_ITEMSUBS](../../Tables/LG_ITEMSUBS) | Malzeme alternatifleri |
| [LG_XXX_INVDEF](../../Tables/LG_INVDEF) | Malzeme-Ambar bilgileri |
| [LG_XXX_LOCATION](../../Tables/LG_LOCATION) | Stok yerleri |
| [LG_XXX_STCOMPLN](../../Tables/LG_STCOMPLN) | Karma koli satırları |

### Muhasebe Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| [LG_XXX_XX_EMFICHE](../../Tables/LG_EMFICHE) | Muhasebe fişleri |
| [LG_XXX_XX_EMFLINE](../../Tables/LG_EMFLINE) | Muhasebe hareketleri |
| [LG_XXX_XX_EMUHTOT](../../Tables/LG_EMUHTOT) | Muhasebe aylık toplamları |
| [LG_XXX_EMUHACC](../../Tables/LG_EMUHACC) | Muhasebe hesapları |
| [LG_XXX_CRDACREF](../../Tables/LG_CRDACREF) | Kart-Muhasbe kodları |

### Kasa Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| [LG_XXX_XX_CSHTOTS](../../Tables/LG_CSHTOTS) | Kasa aylık toplamları |
| [LG_XXX_XX_KSLINES](../../Tables/LG_KSLINES) | Kasa işlemleri |
| [LG_XXX_KSCARD](../../Tables/LG_KSCARD) | Kasalar |

### Satış/Sipariş Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| [LG_XXX_XX_INVOICE](../../Tables/LG_INVOICE) | Faturalar |
| [LG_XXX_XX_ORFICHE](../../Tables/LG_ORFICHE) | Sipariş fişleri |
| [LG_XXX_XX_ORFLINE](../../Tables/LG_ORFLINE) | Sipariş hareketleri |
| [LG_XXX_SLSMAN](../../Tables/LG_SLSMAN) | Satış elemanları |
| [LG_XXX_SLSCLREL](../../Tables/LG_SLSCLREL) | Satış elemanı-Cari hesap ilişkisi |
| [LG_XXX_TARGETS](../../Tables/LG_TARGETS) | Satış elemanı hareketleri |
| [LG_XXX_ROUTE](../../Tables/LG_ROUTE) | Satış yönetim raporları |
| [LG_XXX_ROUTETRS](../../Tables/LG_ROUTETRS) | Satış rota satırları |
| [LG_XXX_PRCLIST](../../Tables/LG_PRCLIST) | Alış/Satış fiyatları |
| [LG_XXX_ASCOND](../../Tables/LG_ASCOND) | Alış/Satış koşulları |

### Üretim Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| [LG_XXX_PRODORD](../../Tables/LG_PRODORD) | Üretim emirleri |
| [LG_XXX_ROUTING](../../Tables/LG_ROUTING) | Üretim rotaları |
| [LG_XXX_RTNGLINE](../../Tables/LG_RTNGLINE) | Üretim rota satırları |
| [LG_XXX_BOMASTER](../../Tables/LG_BOMASTER) | Ürün reçeteleri |
| [LG_XXX_BOMLINE](../../Tables/LG_BOMLINE) | Ürün reçete satırları |
| [LG_XXX_BOMREVSN](../../Tables/LG_BOMREVSN) | Ürün reçete revizyonları |
| [LG_XXX_WORKSTAT](../../Tables/LG_WORKSTAT) | İş istasyonları |
| [LG_XXX_WSGRPF](../../Tables/LG_WSGRPF) | İş istasyonu grupları |
| [LG_XXX_OPERTION](../../Tables/LG_OPERTION) | Operasyonlar |
| [LG_XXX_OCCUPATN](../../Tables/LG_OCCUPATN) | Kaynak kullanımları (üretim) |

### Kalite Kontrol Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| [LG_XXX_QCSET](../../Tables/LG_QCSET) | Kalite kontrol setleri |
| [LG_XXX_QCSLINE](../../Tables/LG_QCSLINE) | Kalite kontrol satırları |
| [LG_XXX_QCLVAL](../../Tables/LG_QCLVAL) | Kalite kontrol değerleri |
| [LG_XXX_QASGN](../../Tables/LG_QASGN) | Kalite kontrol hareketi-Kalite kontrol ataması |
| [LG_XXX_XX_SLQCASGN](../../Tables/LG_SLQCASGN) | Kalite kontrol hareketleri |

### Hizmet Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| [LG_XXX_SRVCARD](../../Tables/LG_SRVCARD) | Hizmet kartları |
| [LG_XXX_SRVUNITA](../../Tables/LG_SRVUNITA) | Hizmet kaydı-Birim ataması |
| [LG_XXX_XX_SRVNUMS](../../Tables/LG_SRVNUMS) | Aylık hizmet toplamları |
| [LG_XXX_XX_SRVTOT](../../Tables/LG_SRVTOT) | Aylık hizmet alış/satış toplamları |

### Çalışan Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| [LG_XXX_EMPLOYEE](../../Tables/LG_EMPLOYEE) | Çalışanlar |
| [LG_XXX_EMPGROUP](../../Tables/LG_EMPGROUP) | Çalışan grubu |
| [LG_XXX_EMGRPASS](../../Tables/LG_EMGRPASS) | Çalışan-Grup ataması |
| [LG_XXX_LABORREQ](../../Tables/LG_LABORREQ) | Çalışan ihtiyaçları |

### Ödeme/Tahsilat Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| [LG_XXX_PAYPLANS](../../Tables/LG_PAYPLANS) | Ödeme planları |
| [LG_XXX_PAYLINES](../../Tables/LG_PAYLINES) | Ödeme plan satırları |
| [LG_XXX_XX_PAYTRANS](../../Tables/LG_PAYTRANS) | Ödeme/Tahsilat hareketleri |

### Özellik Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| [LG_XXX_CHARCODE](../../Tables/LG_CHARCODE) | Özellik kodları |
| [LG_XXX_CHARVAL](../../Tables/LG_CHARVAL) | Özellik değerleri |
| [LG_XXX_CHARASGN](../../Tables/LG_CHARASGN) | Malzeme özellik ataması |
| [LG_XXX_SELCHVAL](../../Tables/LG_SELCHVAL) | Malzeme-Özellik değerleri |
| [LG_XXX_OPATTASG](../../Tables/LG_OPATTASG) | Operasyon-Özellik ataması |
| [LG_XXX_WSATTASG](../../Tables/LG_WSATTASG) | İş ist.-Özellik ataması |
| [LG_XXX_WSATTVAS](../../Tables/LG_WSATTVAS) | İş ist.-Özellik değeri ataması |
| [LG_XXX_WSCHCODE](../../Tables/LG_WSCHCODE) | İş istasyonu özellikleri |
| [LG_XXX_WSCHVAL](../../Tables/LG_WSCHVAL) | İş istasyonu özellik değerleri |

### Diğer Tablolar

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| [LG_XXX_XX_TRANSAC](../../Tables/LG_TRANSAC) | Firma dönem bilgileri |
| [LG_XXX_XX_PRODUCER](../../Tables/LG_PRODUCER) | Müstahsil faturası |
| [LG_XXX_XX_PRDCOST](../../Tables/LG_PRDCOST) | Maliyet dönem kapama kayıtları |
| [LG_XXX_XX_SERILOTN](../../Tables/LG_SERILOTN) | Malzeme seri lot no. bilgileri |
| [LG_XXX_XX_SLTRANS](../../Tables/LG_SLTRANS) | Seri/Lot hareketleri |
| [LG_XXX_XX_PERDOC](../../Tables/LG_PERDOC) | Döküman bilgileri (örnek malzeme resmi) |
| [LG_XXX_XX_FOLDER](../../Tables/LG_FOLDER) | Döküman katalog bilgileri (watermark varsa) |
| [LG_XXX_FIRMDOC](../../Tables/LG_FIRMDOC) | Döküman katalog girişi(watermark) |
| [LG_XXX_DECARDS](../../Tables/LG_DECARDS) | İndirim/Masraf kartları |
| [LG_XXX_PRCARDS](../../Tables/LG_PRCARDS) | Promosyon kartları |
| [LG_XXX_SPECODES](../../Tables/LG_SPECODES) | Özel kodlar |
| [LG_XXX_ACCCODES](../../Tables/LG_ACCCODES) | Entegrasyon bağlantı kodları |
| [LG_XXX_LNGEXCSETS](../../Tables/LG_LNGEXCSETS) | Bazı kayıtların diğer dillerdeki açıklamaları |
| [LG_XXX_LOGREP](../../Tables/LG_LOGREP) | LOG (izleme) kaydı |
| [LG_XXX_TRGPAR](../../Tables/LG_TRGPAR) | Trigger parametreleri |
| [LG_XXX_DISPLINE](../../Tables/LG_DISPLINE) | İş emirleri |
| [LG_XXX_FAREGIST](../../Tables/LG_FAREGIST) | Sabit kıymet kayıtları |
| [LG_XXX_FAYEAR](../../Tables/LG_FAYEAR) | Sabit kıymet yıllık kaydı |
| [LG_XXX_EMCENTER](../../Tables/LG_EMCENTER) | Masraf malzemeleri |

### Firma Bağımsız Tablolar

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| L_COUNTRY | Ülkeler |
| L_CITY | Şehirler |
| L_TOWN | İlçe bilgileri |
| L_DISTRICT | Semt bilgileri |
| L_POSTCODE | Posta kodları |
| L_BANKCODE | Banka bilgileri |
| L_BNBRANCH | Şube bilgileri |
| L_TAXOFFICE | Vergi daireleri |
| L_SHPAGENT | Sevkiyat firmaları |
| L_SHPTYPES | Sevkiyat türleri |
| L_FRGTYPES | Taşıma tipleri |
| L_TRADGRP | Ticari işlem grupları |
| L_GOUSERS | Kullanıcılar |
| L_CAPIDEF | Kuruluş bilgileri (ambar, işyer, fabrika vb.) |
| L_NET | Network kontrolü (kimlerin hangi firma ve dönemle çalıştığı) |
| L_CDBTMP | Form boyutları |
| L_DAILYEXCHANGES | Günlük döviz kurları |
| L_ORGDEFS | Organizasyon Şeması |
| L_POSDEFS | Org.Şeması Pozisyonları |
| L_ORGDOC | Pozisyon açıklamalarının(uzun text) |
| L_GTIP_CODE | Gtip kodları |
| L_GTIP_DEF | Gtip tanımları |
| L_LDOCNUM | Döküman numaralama şablonları |
| L_LDOCFOLD | Doküman katalog bilgisi |
| L_LDOCITEM | Doküman tanımları |
| L_RPFILTSXXX | Kaydedilen rapor filtreleri |
| L_RPLAYS_XXX | Kaydedilen rapor tasarımları |
| L_PRICEINDEXTYP | Endeks türleri |
| L_PRICEINDEX | Fiyat endeksleri |

## Kayıt Numaralama Şablonları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| L_LDOCNUM | Kayıt Numaralama Şablonları |

## Logo Çek Tabloları

- Çek senet kartları [LG_xxx_xx_CSCARD](../../Tables/LG_CSCARD) Tablosunda tutulur ve bu tablodan gördüğü harekete göre durum bilgisi (STATNO) ile alınabilir.
- Çekler Hareket gördükçe [LG_XXX_XX_CSTRANS](../../Tables/LG_CSTRANS) Tablosunda çek refaransı olarak (CSREF) de tutulur. Ve her hareket birden çok satıra dağılır.
- Bankada işlem gören çekler için kesilen bordrolardan sonra banka fişi ve hareketi oluşmaktadır. [LG_XXX_01_BNFLINE](../../Tables/LG_BNFLINE) Ve [LG_XXX_XX_BNFICHE](../../Tables/LG_BNFICHE) Tablolarına bu bilgiler yazılmaktadır.
- Çek hareketleri Bordrolar aracılığı ile [LG_XXX_XX_CSTRANS](../../Tables/LG_CSTRANS) (ROLLREF Referansı ve LINENO_ ilede bordronun kaçıncı satırı ile) Tablosuna yazılır. Devir çekleri Hariç (Devir çekleri bordrolar aracılığı ile olmadığından) bordroların bilgilerinin yazıldığı [LG_XXX_XX_CSROLL](../../Tables/LG_CSROLL) Tablosunda Sadece bordro başlık bilgileri bulunur.
- Bordro olarak işlediğiniz bütün bilgiler [LG_XXX_XX_CLFLINE](../../Tables/LG_CLFLINE) Tablosuna ve Çek Kart Bilgilerinizde Vade kontrolleri için Satır Satır [LG_XXX_XX_PAYTRANS](../../Tables/LG_PAYTRANS) Tablosuna yazar. Oradan da Borc/Alacak Toplam bilgileri oluşur.

## Bazı Önemli Tabloların Önemli Alanları

### Fatura Tabloları

[`INVOICE`](../../Tables/LG_INVOICE) tablosunda veri tabanına kaydedilen faturaların başlık bilgileri tutulmaktadır. Faturanın satır bilgilerine ulaşmak için [`STLINE`](../../Tables/LG_STLINE) tablosu okunmalıdır.

**Fatura türü (TRCODE):**

| Kod | Açıklama |
|-----|----------|
| 1 | Mal alım faturası |
| 2 | Perakende satış iade faturası |
| 3 | Toptan satış iade faturası |
| 4 | Alınan hizmet faturası |
| 5 | Alınan proforma fatura |
| 6 | Alım iade faturası |
| 7 | Perakende satış faturası |
| 8 | Toptan satış faturası |
| 9 | Verilen hizmet faturası |
| 10 | Verilen proforma fatura |
| 13 | Alınan Fiyat farkı faturası |
| 14 | Verilen fiyat farkı faturası |
| 26 | Müstahsil makbuzu |

### Stok Fişleri

Ambar fişi, giriş çıkış fişleri ve irsaliyeler kayıtlarının başlık bilgileri [`STFICHE`](../../Tables/LG_STFICHE) tablosunda tutulmaktadır. Stok hareketlerine ulaşmak için [`STFLINE`](../../Tables/LG_STLINE) tablosunun okunması gerekmektedir.

**Fiş türü (TRCODE):**

| Kod | Açıklama |
|-----|----------|
| 1 | Mal alım irsaliyesi |
| 2 | Per. sat. iade irs. |
| 3 | Topt.sat. iade irs. |
| 4 | Kons. çıkış iade irs. |
| 5 | Konsinye giriş irs. |
| 6 | Alım iade irs. |
| 7 | Perakende satış irs. |
| 8 | Toptan satış irs. |
| 9 | Konsinye çıkış irs. |
| 10 | Konsinye giriş iade irs. |
| 11 | Fire fişi |
| 12 | Sarf fişi |
| 13 | Üretimden giriş fişi |
| 14 | Devir fişi |
| 25 | Ambar fişi |
| 26 | Mustahsil irs. |
| 50 | Sayım Fazlası Fişi |
| 51 | Sayım Eksiği Fişi |

### Stok Kartları

[`LG_XXX_ITEMS`](../../Tables/LG_ITEMS)

**Kart türü (CARDTYPE):**

| Kod | Açıklama |
|-----|----------|
| 1 | Ticari mal |
| 2 | Karma koli |
| 3 | Depozitolu mal |
| 4 | Sabit kıymet |
| 10 | Hammadde |
| 11 | Yarımamul |
| 12 | Mamul |
| 13 | Tüketim malı |
| 20 | M.sınıfı (genel) |
| 21 | M.sınıfı (tablolu) |
| 22 | Firma dosyaları oluşturulurken default olarak eklenen malzeme sınıfı |

### Cari Hesap Kartları

[`LG_XXX_CLCARD`](../../Tables/LG_CLCARD)

**Kart tipi (ACTIVE):**

| Kod | Açıklama |
|-----|----------|
| 1 | Alıcı |
| 2 | Satıcı |
| 3 | Alıcı+Satıcı |

### Cari Hesap Hareketleri

[`LG_XXX_XX_CLFLINE`](../../Tables/LG_CLFLINE)

**Hareket türü (TRCODE):**

| Kod | Açıklama |
|-----|----------|
| 01 | Nakit tahsilat |
| 02 | Nakit ödeme |
| 03 | Borç dekontu |
| 04 | Alacak dekontu |
| 05 | Virman Işlemi |
| 06 | Kur farkı işlemi |
| 12 | Özel işlem |
| 20 | Gelen havaleler |
| 21 | Gönderilen havaleler |
| 31 | Mal alım fat. |
| 32 | Perakende satış iade fat. |
| 33 | Toptan satış iade fat. |
| 34 | Alınan hizmet fat. |
| 35 | Alınan proforma fat. |
| 36 | Alım iade fat. |
| 37 | Perakende satış fat. |
| 38 | Toptan satış fat. |
| 39 | Verilen hizmet faturası |
| 40 | Verilen proforma fat. |
| 41 | Verilen vade farkı fat. |
| 42 | Alınan Vade farkı fat. |
| 43 | Alınan fiyat farkı fat. |
| 44 | Verilen fiyat farkı fat. |
| 56 | Müstahsil makbuzu |
| 61 | Çek girişi |
| 62 | Senet girişi |
| 63 | Çek çıkış cari hesaba |
| 64 | Senet çıkış cari hesaba |

### Çek/Senet İşlemleri

#### ÇEK SENET KARTI ([LG_XXX_XX_CSCARD](../../Tables/LG_CSCARD))

**Şimdiki statüsü (CURRSTAT):**

Çek için (doc=1):

| Kod | Açıklama |
|-----|----------|
| 1 | Müşteriye iade |
| 2 | Portföyden tahsil |
| 3 | Bankada tahsil |
| 4 | Portföyde karşılıksız |
| 5 | Bankada karşılıksız |
| 6 | Müşteriden portföye iade |
| 7 | Bankadan portföye iade |
| 8 | Müşteriden karşılıksız iade |
| 9 | Cirodan tahsil |
| A | Tahsil edilemiyor |

Senet için (doc=2):

| Kod | Açıklama |
|-----|----------|
| 1 | Müşteriye iade |
| 2 | Portföyden tahsil |
| 3 | Bankada tahsil |
| 4 | Portföyde protestolu |
| 5 | Bankada protestolu |
| 6 | Müşteriden portföye iade |
| 7 | Bankadan portföye iade |
| 8 | Müşteriden protestolu iade |
| 9 | Cirodan tahsil |
| A | Tahsil edilemiyor |

#### ÇEK SENET HAREKETİ ([LG_XXX_XX_CSTRANS](../../Tables/LG_CSTRANS))

**Statü (STATUS):**

| Kod | Açıklama |
|-----|----------|
| 1 | Portföyde |
| 2 | Ciro edildi |
| 3 | Teminata verildi |
| 4 | Tahsile verildi |
| 5 | Protestolu tahsile verildi |
| 6 | İade edildi |
| 7 | Protesto edildi |
| 8 | Tahsil edildi |
| 9 | Kendi çekimiz |
| 10 | Borç senedimiz |
| 11 | Karşılığı yok |
| 12 | Tahsil edilemiyor |

#### BORDRO ([CSROLL](../../Tables/LG_CSROLL))

Çek ve senetlerle ilgili tüm hareketler çek/senet bordroları aracılığı ile kaydedilmekte ve bu kayıtlar CSROLL tablosunda tutulmaktadır.

**Bordro İşlem türü (TRCODE):**

| Kod | Açıklama |
|-----|----------|
| 1 | Çek girişi |
| 2 | Senet girişi |
| 3 | Çek çıkış (cari hesaba) |
| 4 | Senet çıkış (cari hesaba) |
| 5 | Çek çıkış (banka tahsil) |
| 6 | Senet çıkış (Banka tahsil) |
| 7 | Çek çıkış (banka teminat) |
| 8 | Senet çıkış (banka teminat) |
| 9 | İşlem Bordrosu (müşteri çeki) |
| 10 | İşlem bordrosu (müşteri senedi) |
| 11 | İşlem bordrosu (kendi çekimiz) |
| 12 | İşlem bordrosu (borç senedimiz) |

**Bordro İşlem Referansları (doc=3 ise):**

| Kod | Açıklama |
|-----|----------|
| 1 | Müşteriden iade |
| 2 | Müşteride tahsil |

**Bordro İşlem Referansları (doc=4 ise):**

| Kod | Açıklama |
|-----|----------|
| 1 | Müşteriden iade |
| 2 | Müşteride tahsil |
| 3 | Müşteride protesto |
| 4 | Tahsil edilemiyor |

## Logo Tablo Yapısı Sınıflandırması

Logo veritabanı yapısı firma kodlarına ve dönemlere göre düzenlenmiştir. Tablo isimlerindeki XXX firma kodunu, XX ise dönem numarasını temsil etmektedir.

## Logo Tablo İsimleri Listesi

Aşağıda Logo ERP sisteminde kullanılan tüm tablo isimleri alfabetik olarak listelenmiştir:

| Tablo Adı | Açıklama |
|-----------|----------|
| L_BANKCODE | Banka bilgileri |
| L_BNBRANCH | Şube bilgileri |
| L_CAPIDEF | Kuruluş bilgileri (ambar, işyer, fabrika vb.) |
| L_CDBTMP | Form boyutları |
| L_CITY | Şehirler |
| L_COUNTRY | Ülkeler |
| L_DAILYEXCHANGES | Günlük döviz kurları |
| L_DISTRICT | Semt bilgileri |
| L_FRGTYPES | Taşıma tipleri |
| L_GOUSERS | Kullanıcılar |
| L_GTIP_CODE | Gtip kodları |
| L_GTIP_DEF | Gtip tanımları |
| L_LDOCFOLD | Doküman katalog bilgisi |
| L_LDOCITEM | Doküman tanımları |
| L_LDOCNUM | Doküman numaralama şablonları |
| L_NET | Network kontrolü (kimlerin hangi firma ve dönemle çalıştığı) |
| L_ORGDEFS | Organizasyon Şeması |
| L_ORGDOC | Pozisyon açıklamaları |
| L_POSDEFS | Org.Şeması Pozisyonları |
| L_POSTCODE | Posta kodları |
| L_PRICEINDEX | Fiyat endeksleri |
| L_PRICEINDEXTYP | Endeks türleri |
| L_RPFILTSXXX | Kaydedilen rapor filtreleri |
| L_RPLAYS_XXX | Kaydedilen rapor tasarımları |
| L_SHPAGENT | Sevkiyat firmaları |
| L_SHPTYPES | Sevkiyat türleri |
| L_TAXOFFICE | Vergi daireleri |
| L_TOWN | İlçe bilgileri |
| L_TRADGRP | Ticari işlem grupları |
| [LG_000_SYSLOG](../../Tables/LG_SYSLOG) | Kullanıcı İzleme |
| [LG_ACTPEPL](../../Tables/LG_ACTPEPL) | Satış Faaliyetine Bağlı Kişiler |
| [LG_CATEGLISTS](../../Tables/LG_CATEGLISTS) | Kategoriler |
| [LG_CNTSLSMASG](../../Tables/LG_CNTSLSMASG) | Satış Elemanı-İlgili Kişi Bağlantı |
| [LG_CONTACTS](../../Tables/LG_CONTACTS) | İlgili Kişiler |
| [LG_CSTVND](../../Tables/LG_CSTVND) | Müşteri |
| [LG_CVINDASG](../../Tables/LG_CVINDASG) | Müşteri-Endüstri Bağlantı |
| [LG_EXCHANGE_XXX](../../Tables/LG_EXCHANGE) | Firma Bazlı Günlük döviz kurları |
| [LG_INDUSTRY](../../Tables/LG_INDUSTRY) | Endüstri/Sektör |
| [LG_OFFER](../../Tables/LG_OFFER) | Teklif |
| [LG_SATI](../../Tables/LG_SATI) | Satış Faaliyetleri(m) Penceresi Genel ve Kişisel İşlemler |
| [LG_SATIFILTER](../../Tables/LG_SATIFILTER) | Satış Faaliyetleri(m) Penceresi Genel ve Kişisel İşlemler Filtre Tanımları |
| [LG_SLSACTIV](../../Tables/LG_SLSACTIV) | Satış Faaliyetleri |
| [LG_SLSCLREL](../../Tables/LG_SLSCLREL) | Satış Temsilcisi-Müşteri Bağlantı (CRM Seti) |
| [LG_SLSFILES](../../Tables/LG_SLSFILES) | Satış Dosyaları |
| [LG_SLSMAN](../../Tables/LG_SLSMAN) | Satış Temsilcileri ve Plasiyerler |
| [LG_SLSOPPOR](../../Tables/LG_SLSOPPOR) | Satış Fırsatları |
| [LG_XXX_ACCCODES](../../Tables/LG_ACCCODES) | Entegrasyon bağlantı kodları |
| [LG_XXX_ASCOND](../../Tables/LG_ASCOND) | Alış/Satış koşulları |
| [LG_XXX_BANKACC](../../Tables/LG_BANKACC) | Banka hesapları |
| [LG_XXX_BNCARD](../../Tables/LG_BNCARD) | Bankalar |
| [LG_XXX_BOMLINE](../../Tables/LG_BOMLINE) | Ürün reçete satırları |
| [LG_XXX_BOMASTER](../../Tables/LG_BOMASTER) | Ürün reçeteleri |
| [LG_XXX_BOMREVSN](../../Tables/LG_BOMREVSN) | Ürün reçete revizyonları |
| [LG_XXX_CHARASGN](../../Tables/LG_CHARASGN) | Malzeme özellik ataması |
| [LG_XXX_CHARCODE](../../Tables/LG_CHARCODE) | Özellik kodları |
| [LG_XXX_CHARVAL](../../Tables/LG_CHARVAL) | Özellik değerleri |
| [LG_XXX_CLCARD](../../Tables/LG_CLCARD) | Cari hesap kartları |
| [LG_XXX_CLINTEL](../../Tables/LG_CLINTEL) | Cari hesap istihbarat bilgileri |
| [LG_XXX_COPRDBOM](../../Tables/LG_COPRDBOM) | Reçete-ek ürün ataması |
| [LG_XXX_CRDACREF](../../Tables/LG_CRDACREF) | Kart-Muhasbe kodları |
| [LG_XXX_DECARDS](../../Tables/LG_DECARDS) | İndirim/Masraf kartları |
| [LG_XXX_DISPLINE](../../Tables/LG_DISPLINE) | İş emirleri |
| [LG_XXX_DISTLINE](../../Tables/LG_DISTLINE) | Dağıtım şablonu satırları |
| [LG_XXX_DISTTEMP](../../Tables/LG_DISTTEMP) | Dağıtım şablonları |
| [LG_XXX_EMCENTER](../../Tables/LG_EMCENTER) | Masraf malzemeleri |
| [LG_XXX_EMGRPASS](../../Tables/LG_EMGRPASS) | Çalışan-Grup ataması |
| [LG_XXX_EMPGROUP](../../Tables/LG_EMPGROUP) | Çalışan grubu |
| [LG_XXX_EMPLOYEE](../../Tables/LG_EMPLOYEE) | Çalışanlar |
| [LG_XXX_EMUHACC](../../Tables/LG_EMUHACC) | Muhasebe hesapları |
| [LG_XXX_ENGCLINE](../../Tables/LG_ENGCLINE) | Mühendislik değişikliği işlemi |
| [LG_XXX_FAREGIST](../../Tables/LG_FAREGIST) | Sabit kıymet kayıtları |
| [LG_XXX_FAYEAR](../../Tables/LG_FAYEAR) | Sabit kıymet yıllık kaydı |
| [LG_XXX_FIRMDOC](../../Tables/LG_FIRMDOC) | Doküman katalog girişi(watermark) |
| [LG_XXX_INVDEF](../../Tables/LG_INVDEF) | Malzeme-Ambar bilgileri |
| [LG_XXX_ITEMS](../../Tables/LG_ITEMS) | Malzemeler |
| [LG_XXX_ITEMSUBS](../../Tables/LG_ITEMSUBS) | Malzeme alternatifleri |
| [LG_XXX_ITMBOMAS](../../Tables/LG_ITMBOMAS) | Malzeme-Ürecetesi ataması |
| [LG_XXX_ITMCLSAS](../../Tables/LG_ITMCLSAS) | Malzeme-Malzeme sınıfı ataması |
| [LG_XXX_ITMFACTP](../../Tables/LG_ITMFACTP) | Malzeme-Fabrika bilgileri |
| [LG_XXX_ITMUNITA](../../Tables/LG_ITMUNITA) | Malzeme-Birim ataması |
| [LG_XXX_ITMWSDEF](../../Tables/LG_ITMWSDEF) | Malzeme-İş ist. bilgileri |
| [LG_XXX_ITMWSTOT](../../Tables/LG_ITMWSTOT) | Malzeme-İş ist. Toplamları (günlük) |
| [LG_XXX_KSCARD](../../Tables/LG_KSCARD) | Kasalar |
| [LG_XXX_LABORREQ](../../Tables/LG_LABORREQ) | Çalışan ihtiyaçları |
| [LG_XXX_LNGEXCSETS](../../Tables/LG_LNGEXCSETS) | Bazı kayıtların diğer dillerdeki açıklamaları |
| [LG_XXX_LNOPASGN](../../Tables/LG_LNOPASGN) | Operasyon-Malzeme ilişkisi |
| [LG_XXX_LOCATION](../../Tables/LG_LOCATION) | Stok yerleri |
| [LG_XXX_LOGREP](../../Tables/LG_LOGREP) | LOG (izleme) kaydı |
| [LG_XXX_OCCUPATN](../../Tables/LG_OCCUPATN) | Kaynak kullanımları (üretim) |
| [LG_XXX_OPATTASG](../../Tables/LG_OPATTASG) | Operasyon-Özellik ataması |
| [LG_XXX_OPERTION](../../Tables/LG_OPERTION) | Operasyonlar |
| [LG_XXX_OPRTREQ](../../Tables/LG_OPRTREQ) | Operasyon ihtiyaçları |
| [LG_XXX_PAYLINES](../../Tables/LG_PAYLINES) | Ödeme plan satırları |
| [LG_XXX_PAYPLANS](../../Tables/LG_PAYPLANS) | Ödeme planları |
| [LG_XXX_PEGGING](../../Tables/LG_PEGGING) | İşlem bağlantıları (üretim emri, sipariş) |
| [LG_XXX_PRCARDS](../../Tables/LG_PRCARDS) | Promosyon kartları |
| [LG_XXX_PRCLIST](../../Tables/LG_PRCLIST) | Alış/Satış fiyatları |
| [LG_XXX_PRODORD](../../Tables/LG_PRODORD) | Üretim emirleri |
| [LG_XXX_PRVOPASG](../../Tables/LG_PRVOPASG) | Önceki operasyon ilişkileri |
| [LG_XXX_QASGN](../../Tables/LG_QASGN) | Kalite kontrol hareketi- Kalite kontrol ataması |
| [LG_XXX_QCLVAL](../../Tables/LG_QCLVAL) | Kalite kontrol değerleri |
| [LG_XXX_QCSET](../../Tables/LG_QCSET) | Kalite kontrol setleri |
| [LG_XXX_QCSLINE](../../Tables/LG_QCSLINE) | Kalite kontrol satırları |
| [LG_XXX_ROUTE](../../Tables/LG_ROUTE) | Satış yönetim raporları |
| [LG_XXX_ROUTETRS](../../Tables/LG_ROUTETRS) | Satış rota satırları |
| [LG_XXX_ROUTING](../../Tables/LG_ROUTING) | Üretim rotaları |
| [LG_XXX_RTNGLINE](../../Tables/LG_RTNGLINE) | Üretim rota satırları |
| [LG_XXX_SELCHVAL](../../Tables/LG_SELCHVAL) | Malzeme-Özellik değerleri |
| [LG_XXX_SHIPINFO](../../Tables/LG_SHIPINFO) | Sevkiyat Adresleri |
| [LG_XXX_SLSCLREL](../../Tables/LG_SLSCLREL) | Satış elemanı-Cari hesap ilişkisi |
| [LG_XXX_SLSMAN](../../Tables/LG_SLSMAN) | Satış elemanları |
| [LG_XXX_SPECODES](../../Tables/LG_SPECODES) | Özel kodlar |
| [LG_XXX_SRVCARD](../../Tables/LG_SRVCARD) | Hizmet kartları |
| [LG_XXX_SRVUNITA](../../Tables/LG_SRVUNITA) | Hizmet kaydı-Birim ataması |
| [LG_XXX_STCOMPLN](../../Tables/LG_STCOMPLN) | Karma koli satırları |
| [LG_XXX_SUPPASGN](../../Tables/LG_SUPPASGN) | Malzeme-Tedarikçi ataması |
| [LG_XXX_TARGETS](../../Tables/LG_TARGETS) | Satış elemanı hareketleri |
| [LG_XXX_TOOLREQ](../../Tables/LG_TOOLREQ) | Araç ihtiyaçları |
| [LG_XXX_TRGPAR](../../Tables/LG_TRGPAR) | Trigger parametreleri |
| [LG_XXX_UNITSETC](../../Tables/LG_UNITSETC) | Birim setleri arası çevrim katsayıları |
| [LG_XXX_UNITSETF](../../Tables/LG_UNITSETF) | Birim setleri |
| [LG_XXX_UNITSETL](../../Tables/LG_UNITSETL) | Birimler |
| [LG_XXX_WORKSTAT](../../Tables/LG_WORKSTAT) | İş istasyonları |
| [LG_XXX_WSATTASG](../../Tables/LG_WSATTASG) | İş ist.-Özellik ataması |
| [LG_XXX_WSATTVAS](../../Tables/LG_WSATTVAS) | İş ist.-Özellik değeri ataması |
| [LG_XXX_WSCHCODE](../../Tables/LG_WSCHCODE) | İş istasyonu özellikleri |
| [LG_XXX_WSCHVAL](../../Tables/LG_WSCHVAL) | İş istasyonu özellik değerleri |
| [LG_XXX_WSGRPASS](../../Tables/LG_WSGRPASS) | İş istasyonu-grup ataması |
| [LG_XXX_WSGRPF](../../Tables/LG_WSGRPF) | İş istasyonu grupları |
| [LG_XXX_XX_BNFICHE](../../Tables/LG_BNFICHE) | Banka fişleri |
| [LG_XXX_XX_BNFLINE](../../Tables/LG_BNFLINE) | Banka hareketleri |
| [LG_XXX_XX_BNTOTFIL](../../Tables/LG_BNTOTFIL) | Banka aylık toplamları |
| [LG_XXX_XX_CLFICHE](../../Tables/LG_CLFICHE) | Cari hesap fişleri |
| [LG_XXX_XX_CLFLINE](../../Tables/LG_CLFLINE) | Cari hesap hareketleri |
| [LG_XXX_XX_CLRNUMS](../../Tables/LG_CLRNUMS) | Cari hesap risk tabloları |
| [LG_XXX_XX_CLTOTFIL](../../Tables/LG_CLTOTFIL) | Cari hesap aylık toplamları |
| [LG_XXX_XX_CSCARD](../../Tables/LG_CSCARD) | Çek/Senet kartları |
| [LG_XXX_XX_CSHTOTS](../../Tables/LG_CSHTOTS) | Kasa aylık toplamları |
| [LG_XXX_XX_CSROLL](../../Tables/LG_CSROLL) | Çek/Senet bordroları |
| [LG_XXX_XX_CSTRANS](../../Tables/LG_CSTRANS) | Çek/Senet hareketleri |
| [LG_XXX_XX_EMFICHE](../../Tables/LG_EMFICHE) | Muhasebe fişleri |
| [LG_XXX_XX_EMFLINE](../../Tables/LG_EMFLINE) | Muhasebe hareketleri |
| [LG_XXX_XX_EMUHTOT](../../Tables/LG_EMUHTOT) | Muhasebe aylık toplamları |
| [LG_XXX_XX_FOLDER](../../Tables/LG_FOLDER) | Doküman katalog bilgileri (watermark varsa) |
| [LG_XXX_XX_INVOICE](../../Tables/LG_INVOICE) | Faturalar |
| [LG_XXX_XX_KSLINES](../../Tables/LG_KSLINES) | Kasa işlemleri |
| [LG_XXX_XX_ORFICHE](../../Tables/LG_ORFICHE) | Sipariş fişleri |
| [LG_XXX_XX_ORFLINE](../../Tables/LG_ORFLINE) | Sipariş hareketleri |
| [LG_XXX_XX_PAYTRANS](../../Tables/LG_PAYTRANS) | Ödeme/Tahsilat hareketleri |
| [LG_XXX_XX_PERDOC](../../Tables/LG_PERDOC) | Doküman bilgileri (örnek malzeme resmi) |
| [LG_XXX_XX_PRDCOST](../../Tables/LG_PRDCOST) | Maliyet dönem kapama kayıtları |
| [LG_XXX_XX_PRODUCER](../../Tables/LG_PRODUCER) | Müstahsil faturası |
| [LG_XXX_XX_SERILOTN](../../Tables/LG_SERILOTN) | Malzeme seri lot no. Bilgileri |
| [LG_XXX_XX_SLQCASGN](../../Tables/LG_SLQCASGN) | Kalite kontrol hareketleri |
| [LG_XXX_XX_SLTRANS](../../Tables/LG_SLTRANS) | Seri/Lot hareketleri |
| [LG_XXX_XX_SRVNUMS](../../Tables/LG_SRVNUMS) | Aylık hizmet toplamları |
| [LG_XXX_XX_SRVTOT](../../Tables/LG_SRVTOT) | Aylık hizmet alış/satış top
