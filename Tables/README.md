# Logo ERP Veritabanı Tabloları  

Bu klasör, **LDDS.xls dosyasındaki bilgilerden yola çıkarak hazırlanmış veritabanı tabloları** ile ilgili dökümanları içerir.  

## 📂 İçerik  

- **Tablo Alanları** – Tablolardaki sütunların açıklamaları  
- **İndeksler** – Her tablonun indeks bilgileri  
- **İlişkiler** – Tablolar arası ilişkiler  

# Logo ERP Veritabanı Dökümantasyonu

Bu dökümantasyon, LogoWings ve LogoTiger ERP sistemlerinin MS SQL veritabanı yapısını detaylı olarak açıklamaktadır. Logo ERP sisteminin veritabanı yapısı, tablo isimleri, alan açıklamaları ve tablolar arası ilişkileri içermektedir.

Bu repo, geliştirici, veri analisti, danışman ve sistem yöneticileri için bir başvuru kaynağı olarak hazırlanmıştır.

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
| LG_ACTPEPL | Satış Faaliyetine Bağlı Kişiler |
| LG_CATEGLISTS | Kategoriler |
| LG_CNTSLSMASG | Satış Elemanı-İlgili Kişi Bağlantı |
| LG_CONTACTS | İlgili Kişiler |
| LG_CSTVND | Müşteri |
| LG_CVINDASG | Müşteri-Endüstri Bağlantı |
| LG_INDUSTRY | Endüstri/Sektör |
| LG_OFFER | Teklif |
| LG_SATI | Satış Faaliyetleri(m) Penceresi Genel ve Kişisel İşlemler |
| LG_SATIFILTER | Satış Faaliyetleri(m) Penceresi Genel ve Kişisel İşlemler Filtre Tanımları |
| LG_SLSACTIV | Satış Faaliyetleri |
| LG_SLSCLREL | Satış Temsilcisi-Müşteri Bağlantı (CRM Seti) |
| LG_SLSFILES | Satış Dosyaları |
| LG_SLSOPPOR | Satış Fırsatları |

### Satış Elemanı Tablosu

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| LG_SLSMAN | Satış Temsilcileri ve Plasiyerler |

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
| LG_000_SYSLOG | Kullanıcı İzleme |

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
| LG_XXX_XX_BNFICHE | Banka fişleri |
| LG_XXX_XX_BNFLINE | Banka hareketleri |
| LG_XXX_XX_BNTOTFIL | Banka aylık toplamları |
| LG_XXX_BANKACC | Banka hesapları |
| LG_XXX_BNCARD | Bankalar |

### Cari Hesap Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| LG_XXX_XX_CLFICHE | Cari hesap fişleri |
| LG_XXX_XX_CLFLINE | Cari hesap hareketleri |
| LG_XXX_XX_CLRNUMS | Cari hesap risk tabloları |
| LG_XXX_XX_CLTOTFIL | Cari hesap aylık toplamları |
| LG_XXX_CLCARD | Cari hesap kartları |
| LG_XXX_CLINTEL | Cari hesap istihbarat bilgileri |

### Çek/Senet Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| LG_XXX_XX_CSCARD | Çek/Senet kartları |
| LG_XXX_XX_CSROLL | Çek/Senet bordroları |
| LG_XXX_XX_CSTRANS | Çek/Senet hareketleri |

### Stok Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| LG_XXX_XX_STFICHE | Stok fişleri |
| LG_XXX_XX_STLINE | Malzeme hareketleri |
| LG_XXX_XX_STINVTOT | Günlük malzeme ambar toplamları |
| LG_XXX_XX_STINVENS | Malzeme alış/satış aylık toplamları |
| LG_XXX_ITEMS | Malzemeler |
| LG_XXX_ITEMSUBS | Malzeme alternatifleri |
| LG_XXX_INVDEF | Malzeme-Ambar bilgileri |
| LG_XXX_LOCATION | Stok yerleri |
| LG_XXX_STCOMPLN | Karma koli satırları |

### Muhasebe Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| LG_XXX_XX_EMFICHE | Muhasebe fişleri |
| LG_XXX_XX_EMFLINE | Muhasebe hareketleri |
| LG_XXX_XX_EMUHTOT | Muhasebe aylık toplamları |
| LG_XXX_EMUHACC | Muhasebe hesapları |
| LG_XXX_CRDACREF | Kart-Muhasbe kodları |

### Kasa Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| LG_XXX_XX_CSHTOTS | Kasa aylık toplamları |
| LG_XXX_XX_KSLINES | Kasa işlemleri |
| LG_XXX_KSCARD | Kasalar |

### Satış/Sipariş Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| LG_XXX_XX_INVOICE | Faturalar |
| LG_XXX_XX_ORFICHE | Sipariş fişleri |
| LG_XXX_XX_ORFLINE | Sipariş hareketleri |
| LG_XXX_SLSMAN | Satış elemanları |
| LG_XXX_SLSCLREL | Satış elemanı-Cari hesap ilişkisi |
| LG_XXX_TARGETS | Satış elemanı hareketleri |
| LG_XXX_ROUTE | Satış yönetim raporları |
| LG_XXX_ROUTETRS | Satış rota satırları |
| LG_XXX_PRCLIST | Alış/Satış fiyatları |
| LG_XXX_ASCOND | Alış/Satış koşulları |

### Üretim Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| LG_XXX_PRODORD | Üretim emirleri |
| LG_XXX_ROUTING | Üretim rotaları |
| LG_XXX_RTNGLINE | Üretim rota satırları |
| LG_XXX_BOMASTER | Ürün reçeteleri |
| LG_XXX_BOMLINE | Ürün reçete satırları |
| LG_XXX_BOMREVSN | Ürün reçete revizyonları |
| LG_XXX_WORKSTAT | İş istasyonları |
| LG_XXX_WSGRPF | İş istasyonu grupları |
| LG_XXX_OPERTION | Operasyonlar |
| LG_XXX_OCCUPATN | Kaynak kullanımları (üretim) |

### Kalite Kontrol Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| LG_XXX_QCSET | Kalite kontrol setleri |
| LG_XXX_QCSLINE | Kalite kontrol satırları |
| LG_XXX_QCLVAL | Kalite kontrol değerleri |
| LG_XXX_QASGN | Kalite kontrol hareketi-Kalite kontrol ataması |
| LG_XXX_XX_SLQCASGN | Kalite kontrol hareketleri |

### Hizmet Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| LG_XXX_SRVCARD | Hizmet kartları |
| LG_XXX_SRVUNITA | Hizmet kaydı-Birim ataması |
| LG_XXX_XX_SRVNUMS | Aylık hizmet toplamları |
| LG_XXX_XX_SRVTOT | Aylık hizmet alış/satış toplamları |

### Çalışan Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| LG_XXX_EMPLOYEE | Çalışanlar |
| LG_XXX_EMPGROUP | Çalışan grubu |
| LG_XXX_EMGRPASS | Çalışan-Grup ataması |
| LG_XXX_LABORREQ | Çalışan ihtiyaçları |

### Ödeme/Tahsilat Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| LG_XXX_PAYPLANS | Ödeme planları |
| LG_XXX_PAYLINES | Ödeme plan satırları |
| LG_XXX_XX_PAYTRANS | Ödeme/Tahsilat hareketleri |

### Özellik Tabloları

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| LG_XXX_CHARCODE | Özellik kodları |
| LG_XXX_CHARVAL | Özellik değerleri |
| LG_XXX_CHARASGN | Malzeme özellik ataması |
| LG_XXX_SELCHVAL | Malzeme-Özellik değerleri |
| LG_XXX_OPATTASG | Operasyon-Özellik ataması |
| LG_XXX_WSATTASG | İş ist.-Özellik ataması |
| LG_XXX_WSATTVAS | İş ist.-Özellik değeri ataması |
| LG_XXX_WSCHCODE | İş istasyonu özellikleri |
| LG_XXX_WSCHVAL | İş istasyonu özellik değerleri |

### Diğer Tablolar

| Tablo Adı | Tablo Açıklaması |
|-----------|------------------|
| LG_XXX_XX_TRANSAC | Firma dönem bilgileri |
| LG_XXX_XX_PRODUCER | Müstahsil faturası |
| LG_XXX_XX_PRDCOST | Maliyet dönem kapama kayıtları |
| LG_XXX_XX_SERILOTN | Malzeme seri lot no. bilgileri |
| LG_XXX_XX_SLTRANS | Seri/Lot hareketleri |
| LG_XXX_XX_PERDOC | Döküman bilgileri (örnek malzeme resmi) |
| LG_XXX_XX_FOLDER | Döküman katalog bilgileri (watermark varsa) |
| LG_XXX_FIRMDOC | Döküman katalog girişi(watermark) |
| LG_XXX_DECARDS | İndirim/Masraf kartları |
| LG_XXX_PRCARDS | Promosyon kartları |
| LG_XXX_SPECODES | Özel kodlar |
| LG_XXX_ACCCODES | Entegrasyon bağlantı kodları |
| LG_XXX_LNGEXCSETS | Bazı kayıtların diğer dillerdeki açıklamaları |
| LG_XXX_LOGREP | LOG (izleme) kaydı |
| LG_XXX_TRGPAR | Trigger parametreleri |
| LG_XXX_DISPLINE | İş emirleri |
| LG_XXX_FAREGIST | Sabit kıymet kayıtları |
| LG_XXX_FAYEAR | Sabit kıymet yıllık kaydı |
| LG_XXX_EMCENTER | Masraf malzemeleri |

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

- Çek senet kartları LG_xxx_xx_CSCARD Tablosunda tutulur ve bu tablodan gördüğü harekete göre durum bilgisi (STATNO) ile alınabilir.
- Çekler Hareket gördükçe LG_XXX_XX_CSTRANS Tablosunda çek refaransı olarak (CSREF) de tutulur. Ve her hareket birden çok satıra dağılır.
- Bankada işlem gören çekler için kesilen bordrolardan sonra banka fişi ve hareketi oluşmaktadır. LG_XXX_01_BNFLINE Ve LG_XXX_XX_BNFICHE Tablolarına bu bilgiler yazılmaktadır.
- Çek hareketleri Bordrolar aracılığı ile LG_XXX_XX_CSTRANS (ROLLREF Referansı ve LINENO_ ilede bordronun kaçıncı satırı ile) Tablosuna yazılır. Devir çekleri Hariç (Devir çekleri bordrolar aracılığı ile olmadığından) bordroların bilgilerinin yazıldığı LG_XXX_XX_CSROLL Tablosunda Sadece bordro başlık bilgileri bulunur.
- Bordro olarak işlediğiniz bütün bilgiler LG_XXX_XX_CLFLINE Tablosuna ve Çek Kart Bilgilerinizde Vade kontrolleri için Satır Satır LG_XXX_XX_PAYTRANS Tablosuna yazar. Oradan da Borc/Alacak Toplam bilgileri oluşur.

## Bazı Önemli Tabloların Önemli Alanları

### Fatura Tabloları

`INVOICE` tablosunda veri tabanına kaydedilen faturaların başlık bilgileri tutulmaktadır. Faturanın satır bilgilerine ulaşmak için `STLINE` tablosu okunmalıdır.

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

Ambar fişi, giriş çıkış fişleri ve irsaliyeler kayıtlarının başlık bilgileri `STFICHE` tablosunda tutulmaktadır. Stok hareketlerine ulaşmak için `STFLINE` tablosunun okunması gerekmektedir.

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

`LG_XXX_ITEMS`

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

`LG_XXX_CLCARD`

**Kart tipi (ACTIVE):**

| Kod | Açıklama |
|-----|----------|
| 1 | Alıcı |
| 2 | Satıcı |
| 3 | Alıcı+Satıcı |

### Cari Hesap Hareketleri

`LG_XXX_XX_CLFLINE`

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

#### ÇEK SENET KARTI (LG_XXX_XX_CSCARD)

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

#### ÇEK SENET HAREKETİ (LG_XXX_XX_CSTRANS)

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

#### BORDRO (CSROLL)

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
| LG_000_SYSLOG | Kullanıcı İzleme |
| LG_ACTPEPL | Satış Faaliyetine Bağlı Kişiler |
| LG_CATEGLISTS | Kategoriler |
| LG_CNTSLSMASG | Satış Elemanı-İlgili Kişi Bağlantı |
| LG_CONTACTS | İlgili Kişiler |
| LG_CSTVND | Müşteri |
| LG_CVINDASG | Müşteri-Endüstri Bağlantı |
| LG_EXCHANGE_XXX | Firma Bazlı Günlük döviz kurları |
| LG_INDUSTRY | Endüstri/Sektör |
| LG_OFFER | Teklif |
| LG_SATI | Satış Faaliyetleri(m) Penceresi Genel ve Kişisel İşlemler |
| LG_SATIFILTER | Satış Faaliyetleri(m) Penceresi Genel ve Kişisel İşlemler Filtre Tanımları |
| LG_SLSACTIV | Satış Faaliyetleri |
| LG_SLSCLREL | Satış Temsilcisi-Müşteri Bağlantı (CRM Seti) |
| LG_SLSFILES | Satış Dosyaları |
| LG_SLSMAN | Satış Temsilcileri ve Plasiyerler |
| LG_SLSOPPOR | Satış Fırsatları |
| LG_XXX_ACCCODES | Entegrasyon bağlantı kodları |
| LG_XXX_ASCOND | Alış/Satış koşulları |
| LG_XXX_BANKACC | Banka hesapları |
| LG_XXX_BNCARD | Bankalar |
| LG_XXX_BOMLINE | Ürün reçete satırları |
| LG_XXX_BOMASTER | Ürün reçeteleri |
| LG_XXX_BOMREVSN | Ürün reçete revizyonları |
| LG_XXX_CHARASGN | Malzeme özellik ataması |
| LG_XXX_CHARCODE | Özellik kodları |
| LG_XXX_CHARVAL | Özellik değerleri |
| LG_XXX_CLCARD | Cari hesap kartları |
| LG_XXX_CLINTEL | Cari hesap istihbarat bilgileri |
| LG_XXX_COPRDBOM | Reçete-ek ürün ataması |
| LG_XXX_CRDACREF | Kart-Muhasbe kodları |
| LG_XXX_DECARDS | İndirim/Masraf kartları |
| LG_XXX_DISPLINE | İş emirleri |
| LG_XXX_DISTLINE | Dağıtım şablonu satırları |
| LG_XXX_DISTTEMP | Dağıtım şablonları |
| LG_XXX_EMCENTER | Masraf malzemeleri |
| LG_XXX_EMGRPASS | Çalışan-Grup ataması |
| LG_XXX_EMPGROUP | Çalışan grubu |
| LG_XXX_EMPLOYEE | Çalışanlar |
| LG_XXX_EMUHACC | Muhasebe hesapları |
| LG_XXX_ENGCLINE | Mühendislik değişikliği işlemi |
| LG_XXX_FAREGIST | Sabit kıymet kayıtları |
| LG_XXX_FAYEAR | Sabit kıymet yıllık kaydı |
| LG_XXX_FIRMDOC | Doküman katalog girişi(watermark) |
| LG_XXX_INVDEF | Malzeme-Ambar bilgileri |
| LG_XXX_ITEMS | Malzemeler |
| LG_XXX_ITEMSUBS | Malzeme alternatifleri |
| LG_XXX_ITMBOMAS | Malzeme-Ürecetesi ataması |
| LG_XXX_ITMCLSAS | Malzeme-Malzeme sınıfı ataması |
| LG_XXX_ITMFACTP | Malzeme-Fabrika bilgileri |
| LG_XXX_ITMUNITA | Malzeme-Birim ataması |
| LG_XXX_ITMWSDEF | Malzeme-İş ist. bilgileri |
| LG_XXX_ITMWSTOT | Malzeme-İş ist. Toplamları (günlük) |
| LG_XXX_KSCARD | Kasalar |
| LG_XXX_LABORREQ | Çalışan ihtiyaçları |
| LG_XXX_LNGEXCSETS | Bazı kayıtların diğer dillerdeki açıklamaları |
| LG_XXX_LNOPASGN | Operasyon-Malzeme ilişkisi |
| LG_XXX_LOCATION | Stok yerleri |
| LG_XXX_LOGREP | LOG (izleme) kaydı |
| LG_XXX_OCCUPATN | Kaynak kullanımları (üretim) |
| LG_XXX_OPATTASG | Operasyon-Özellik ataması |
| LG_XXX_OPERTION | Operasyonlar |
| LG_XXX_OPRTREQ | Operasyon ihtiyaçları |
| LG_XXX_PAYLINES | Ödeme plan satırları |
| LG_XXX_PAYPLANS | Ödeme planları |
| LG_XXX_PEGGING | İşlem bağlantıları (üretim emri, sipariş) |
| LG_XXX_PRCARDS | Promosyon kartları |
| LG_XXX_PRCLIST | Alış/Satış fiyatları |
| LG_XXX_PRODORD | Üretim emirleri |
| LG_XXX_PRVOPASG | Önceki operasyon ilişkileri |
| LG_XXX_QASGN | Kalite kontrol hareketi- Kalite kontrol ataması |
| LG_XXX_QCLVAL | Kalite kontrol değerleri |
| LG_XXX_QCSET | Kalite kontrol setleri |
| LG_XXX_QCSLINE | Kalite kontrol satırları |
| LG_XXX_ROUTE | Satış yönetim raporları |
| LG_XXX_ROUTETRS | Satış rota satırları |
| LG_XXX_ROUTING | Üretim rotaları |
| LG_XXX_RTNGLINE | Üretim rota satırları |
| LG_XXX_SELCHVAL | Malzeme-Özellik değerleri |
| LG_XXX_SHIPINFO | Sevkiyat Adresleri |
| LG_XXX_SLSCLREL | Satış elemanı-Cari hesap ilişkisi |
| LG_XXX_SLSMAN | Satış elemanları |
| LG_XXX_SPECODES | Özel kodlar |
| LG_XXX_SRVCARD | Hizmet kartları |
| LG_XXX_SRVUNITA | Hizmet kaydı-Birim ataması |
| LG_XXX_STCOMPLN | Karma koli satırları |
| LG_XXX_SUPPASGN | Malzeme-Tedarikçi ataması |
| LG_XXX_TARGETS | Satış elemanı hareketleri |
| LG_XXX_TOOLREQ | Araç ihtiyaçları |
| LG_XXX_TRGPAR | Trigger parametreleri |
| LG_XXX_UNITSETC | Birim setleri arası çevrim katsayıları |
| LG_XXX_UNITSETF | Birim setleri |
| LG_XXX_UNITSETL | Birimler |
| LG_XXX_WORKSTAT | İş istasyonları |
| LG_XXX_WSATTASG | İş ist.-Özellik ataması |
| LG_XXX_WSATTVAS | İş ist.-Özellik değeri ataması |
| LG_XXX_WSCHCODE | İş istasyonu özellikleri |
| LG_XXX_WSCHVAL | İş istasyonu özellik değerleri |
| LG_XXX_WSGRPASS | İş istasyonu-grup ataması |
| LG_XXX_WSGRPF | İş istasyonu grupları |
| LG_XXX_XX_BNFICHE | Banka fişleri |
| LG_XXX_XX_BNFLINE | Banka hareketleri |
| LG_XXX_XX_BNTOTFIL | Banka aylık toplamları |
| LG_XXX_XX_CLFICHE | Cari hesap fişleri |
| LG_XXX_XX_CLFLINE | Cari hesap hareketleri |
| LG_XXX_XX_CLRNUMS | Cari hesap risk tabloları |
| LG_XXX_XX_CLTOTFIL | Cari hesap aylık toplamları |
| LG_XXX_XX_CSCARD | Çek/Senet kartları |
| LG_XXX_XX_CSHTOTS | Kasa aylık toplamları |
| LG_XXX_XX_CSROLL | Çek/Senet bordroları |
| LG_XXX_XX_CSTRANS | Çek/Senet hareketleri |
| LG_XXX_XX_EMFICHE | Muhasebe fişleri |
| LG_XXX_XX_EMFLINE | Muhasebe hareketleri |
| LG_XXX_XX_EMUHTOT | Muhasebe aylık toplamları |
| LG_XXX_XX_FOLDER | Doküman katalog bilgileri (watermark varsa) |
| LG_XXX_XX_INVOICE | Faturalar |
| LG_XXX_XX_KSLINES | Kasa işlemleri |
| LG_XXX_XX_ORFICHE | Sipariş fişleri |
| LG_XXX_XX_ORFLINE | Sipariş hareketleri |
| LG_XXX_XX_PAYTRANS | Ödeme/Tahsilat hareketleri |
| LG_XXX_XX_PERDOC | Doküman bilgileri (örnek malzeme resmi) |
| LG_XXX_XX_PRDCOST | Maliyet dönem kapama kayıtları |
| LG_XXX_XX_PRODUCER | Müstahsil faturası |
| LG_XXX_XX_SERILOTN | Malzeme seri lot no. Bilgileri |
| LG_XXX_XX_SLQCASGN | Kalite kontrol hareketleri |
| LG_XXX_XX_SLTRANS | Seri/Lot hareketleri |
| LG_XXX_XX_SRVNUMS | Aylık hizmet toplamları |
| LG_XXX_XX_SRVTOT | Aylık hizmet alış/satış toplamları |
| LG_XXX_XX_STFICHE | Stok fişleri |
| LG_XXX_XX_STINVENS | Malzeme alış/satış aylık toplamları |
| LG_XXX_XX_STINVTOT | Günlük malzeme ambar toplamları |
| LG_XXX_XX_STLINE | Malzeme hareketleri |
| LG_XXX_XX_TRANSAC | Firma dönem bilgileri |
