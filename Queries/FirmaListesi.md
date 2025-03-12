# Logo ERP Firma Listesi Sorgusu

Bu proje, Logo ERP sisteminde kayıtlı firma listesini SQL sorgusu ile çekmek için hazırlanmıştır.

## Kullanım

Bu proje, Logo ERP veritabanında bulunan `L_CAPIFIRM` tablosundan firma listesini çekmek için aşağıdaki SQL sorgusunu kullanır:

```sql
SELECT LTRIM(CAST(NR AS VARCHAR) + ' - ' + NAME) AS Firma 
FROM L_CAPIFIRM 
ORDER BY NR;
```

## Açıklamalar

* **NR**: Firma numarasını içerir.
* **NAME**: Firma adını içerir.
* **LTRIM()**: Başta oluşabilecek gereksiz boşlukları temizler.
* **ORDER BY NR**: Firma numarasına göre sıralama yapar.

## Katkıda Bulunma

Herhangi bir geliştirme öneriniz veya hata bildiriminiz varsa, lütfen GitHub üzerinden bir issue oluşturun veya pull request gönderin.

Katkılar **branch koruma kuralları** ile yönetilmektedir. Yapılan değişiklikler, doğrudan ana branch'e eklenemez. Bir değişiklik önerisi (pull request) gönderdiğinizde, inceleme ve onay sürecinden sonra birleşecektir.

Daha fazla bilgi için [Logo ERP Resmi Dokümantasyonu](https://www.logo.com.tr) adresine göz atabilirsiniz.
