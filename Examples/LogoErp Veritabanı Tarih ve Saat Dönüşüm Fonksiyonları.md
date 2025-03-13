# LogoErp Veritabanı Tarih ve Saat Dönüşüm Fonksiyonları

Aşağıda, `LogoErp` veritabanındaki tarih ve saat formatlarını yönetmek için kullanılan C# kodu bulunmaktadır. Bu kod, tarih ve saat verilerini sayısal (tamsayı) formata dönüştürmeyi ve tersine dönüştürmeyi sağlar. Kodun her bir fonksiyonu açıklamalarla birlikte verilmiştir.

## Tam Kod

```csharp
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("LogoErp veritabanı tarih ve saat dönüşüm fonksiyonları");

        DateTime mevcutZaman = DateTime.Now;
        Console.WriteLine($"Tarih: {mevcutZaman}");
        Console.WriteLine($"Saat: {mevcutZaman.ToLongTimeString()}");

        // Sadece tarih kısmını alıyoruz (saat 00:00:00 olarak sıfırlanır)
        DateTime tarih = mevcutZaman.Date;
        // Saat kısmını alıyoruz
        TimeSpan saat = mevcutZaman.TimeOfDay;

        // LogoErp formatında sayısal tarih karşılığını hesaplıyoruz
        int tarihInt = LogoErpTarihSaatDonusturucu.TarihiIntYap(tarih);
        // LogoErp formatında sayısal saat karşılığını hesaplıyoruz
        int saatInt = LogoErpTarihSaatDonusturucu.SaatiIntYap(saat);

        Console.WriteLine($"Tarih LogoErp veritabanındaki sayısal karşılığı: {tarihInt}");
        Console.WriteLine($"Saat LogoErp veritabanındaki sayısal karşılığı: {saatInt}");

        Console.WriteLine("LogoErp veritabanı sayısal tarih ve saat karşılıklarının geri dönüşümü");

        // Sayısal tarihi geri DateTime nesnesine dönüştürme
        DateTime tarihDonusum = LogoErpTarihSaatDonusturucu.IntiTarihYap(tarihInt);
        // Sayısal saati geri string formatında (hh:mm:ss) dönüştürme
        string saatDonusum = LogoErpTarihSaatDonusturucu.IntiSaatYap(saatInt);

        Console.WriteLine($"Tarih: {tarihDonusum}");
        Console.WriteLine($"Saat: {saatDonusum}");
    }
}

static class LogoErpTarihSaatDonusturucu
{
    /// <summary>
    /// Bir DateTime nesnesini LogoErp veritabanı için tamsayıya dönüştürür.
    /// </summary>
    /// <param name="tarih">Dönüştürülecek DateTime nesnesi.</param>
    /// <returns>LogoErp formatında tarihi temsil eden bir tamsayı.</returns>
    public static int TarihiIntYap(DateTime tarih)
    {
        int yil = tarih.Year; // Yılı alıyoruz
        int ay = tarih.Month; // Ayı alıyoruz
        int gun = tarih.Day; // Günü alıyoruz

        return 65536 * yil + 256 * ay + gun;
    }

    /// <summary>
    /// LogoErp formatındaki sayısal bir tarihi DateTime nesnesine dönüştürür.
    /// </summary>
    /// <param name="tarihInt">Sayısal tarihi temsil eden tamsayı.</param>
    /// <returns>Sayısal tarihi temsil eden bir DateTime nesnesi.</returns>
    public static DateTime IntiTarihYap(int tarihInt)
    {
        int yil = tarihInt / 65536;
        int ay = (tarihInt % 65536) / 256;
        int gun = (tarihInt % 65536) % 256;

        return new DateTime(yil, ay, gun);
    }

    /// <summary>
    /// Bir zaman string'ini (hh:mm:ss formatında) LogoErp veritabanı için tamsayıya dönüştürür.
    /// </summary>
    /// <param name="saat">Dönüştürülecek zaman string'i (format: hh:mm:ss).</param>
    /// <returns>LogoErp formatında zamanı temsil eden bir tamsayı.</returns>
    public static int SaatiIntYap(string saat)
    {
        int sonuc = 0;
        if (!string.IsNullOrEmpty(saat))
        {
            string[] saatParcalari = saat.Split(':');
            for (int i = 0; i < saatParcalari.Length; i++)
            {
                int deger = Convert.ToInt32(saatParcalari[i]);
                switch (i)
                {
                    case 0:
                        sonuc += deger * 65536 * 256;
                        break;
                    case 1:
                        sonuc += deger * 65536;
                        break;
                    case 2:
                        sonuc += deger * 256;
                        break;
                }
            }
        }
        return sonuc;
    }

    /// <summary>
    /// Bir TimeSpan nesnesini LogoErp veritabanı için tamsayıya dönüştürür.
    /// </summary>
    /// <param name="saat">Dönüştürülecek TimeSpan nesnesi.</param>
    /// <returns>LogoErp formatında zamanı temsil eden bir tamsayı.</returns>
    public static int SaatiIntYap(TimeSpan saat)
    {
        int sonuc = 0;
        sonuc += saat.Hours * 65536 * 256;
        sonuc += saat.Minutes * 65536;
        sonuc += saat.Seconds * 256;
        return sonuc;
    }

    /// <summary>
    /// LogoErp formatında sayısal bir zamanı (tamsayıyı) geri saat string'ine dönüştürür.
    /// </summary>
    /// <param name="saatInt">Sayısal zamanı temsil eden tamsayı.</param>
    /// <returns>Zamanı temsil eden bir string (format: hh:mm:ss).</returns>
    public static string IntiSaatYap(int saatInt)
    {
        int saat = (saatInt - (saatInt % 65536)) / 65536 / 256;
        int dakika = ((saatInt - (saatInt % 65536)) / 65536 - saat * 256);
        int saniye = ((saatInt % 65536) - ((saatInt % 65536) % 256)) / 256;

        return string.Format("{0:D2}:{1:D2}:{2:D2}", saat, dakika, saniye);
    }
}

