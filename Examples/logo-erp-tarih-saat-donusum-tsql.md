# LogoErp Veritabanı Tarih ve Saat Dönüşüm Fonksiyonları (T-SQL)

Bu kod, LogoErp veritabanındaki tarih ve saat formatlarını yönetmek için kullanılan SQL Server (T-SQL) fonksiyonlarını içerir. Bu fonksiyonlar, tarih ve saat verilerini sayısal (tamsayı) formata dönüştürmeyi ve tersine dönüştürmeyi sağlar.

```sql
-- LogoErp veritabanı için tarih ve saat dönüşüm işlemlerini sağlayan SQL Server fonksiyonları

-- Mevcut fonksiyonları silme
IF OBJECT_ID('dbo.TarihiIntYap', 'FN') IS NOT NULL
    DROP FUNCTION dbo.TarihiIntYap;
GO

IF OBJECT_ID('dbo.IntiTarihYap', 'FN') IS NOT NULL
    DROP FUNCTION dbo.IntiTarihYap;
GO

IF OBJECT_ID('dbo.SaatiIntYap', 'FN') IS NOT NULL
    DROP FUNCTION dbo.SaatiIntYap;
GO

IF OBJECT_ID('dbo.SaatiIntYapTime', 'FN') IS NOT NULL
    DROP FUNCTION dbo.SaatiIntYapTime;
GO

IF OBJECT_ID('dbo.IntiSaatYap', 'FN') IS NOT NULL
    DROP FUNCTION dbo.IntiSaatYap;
GO

-- DateTime değerini LogoErp formatında bir tamsayıya dönüştürür
CREATE FUNCTION dbo.TarihiIntYap(@tarih DATE)
RETURNS INT
AS
BEGIN
    DECLARE @yil INT = YEAR(@tarih);
    DECLARE @ay INT = MONTH(@tarih);
    DECLARE @gun INT = DAY(@tarih);
    
    RETURN 65536 * @yil + 256 * @ay + @gun;
END;
GO

-- LogoErp formatındaki tamsayıyı DateTime değerine dönüştürür
CREATE FUNCTION dbo.IntiTarihYap(@tarihInt INT)
RETURNS DATE
AS
BEGIN
    DECLARE @yil INT = @tarihInt / 65536;
    DECLARE @ay INT = (@tarihInt % 65536) / 256;
    DECLARE @gun INT = (@tarihInt % 65536) % 256;
    
    RETURN DATEFROMPARTS(@yil, @ay, @gun);
END;
GO

-- Saat değerini (HH:MM:SS formatında) LogoErp formatında bir tamsayıya dönüştürür
CREATE FUNCTION dbo.SaatiIntYap(@saat VARCHAR(8))
RETURNS INT
AS
BEGIN
    DECLARE @sonuc INT = 0;
    DECLARE @saat_degeri INT;
    DECLARE @dakika_degeri INT;
    DECLARE @saniye_degeri INT;
    
    IF @saat IS NULL OR @saat = ''
        RETURN 0;
    
    DECLARE @saatParcalari TABLE (id INT IDENTITY(1,1), deger VARCHAR(2));
    
    INSERT INTO @saatParcalari (deger)
    SELECT value FROM STRING_SPLIT(@saat, ':');
    
    SELECT @saat_degeri = CAST(deger AS INT) FROM @saatParcalari WHERE id = 1;
    SELECT @dakika_degeri = CAST(deger AS INT) FROM @saatParcalari WHERE id = 2;
    SELECT @saniye_degeri = CAST(deger AS INT) FROM @saatParcalari WHERE id = 3;
    
    SET @sonuc = @sonuc + ISNULL(@saat_degeri, 0) * 65536 * 256;
    SET @sonuc = @sonuc + ISNULL(@dakika_degeri, 0) * 65536;
    SET @sonuc = @sonuc + ISNULL(@saniye_degeri, 0) * 256;
    
    RETURN @sonuc;
END;
GO

-- TimeSpan değerini LogoErp formatında bir tamsayıya dönüştürür
CREATE FUNCTION dbo.SaatiIntYapTime(@saat TIME)
RETURNS INT
AS
BEGIN
    DECLARE @sonuc INT = 0;
    DECLARE @saat_part INT = DATEPART(HOUR, @saat);
    DECLARE @dakika_part INT = DATEPART(MINUTE, @saat);
    DECLARE @saniye_part INT = DATEPART(SECOND, @saat);
    
    SET @sonuc = @sonuc + @saat_part * 65536 * 256;
    SET @sonuc = @sonuc + @dakika_part * 65536;
    SET @sonuc = @sonuc + @saniye_part * 256;
    
    RETURN @sonuc;
END;
GO

-- LogoErp formatındaki tamsayıyı HH:MM:SS formatında saat dizesine dönüştürür
CREATE FUNCTION dbo.IntiSaatYap(@saatInt INT)
RETURNS VARCHAR(8)
AS
BEGIN
    DECLARE @saat_part INT = (@saatInt - (@saatInt % 65536)) / 65536 / 256;
    DECLARE @dakika_part INT = ((@saatInt - (@saatInt % 65536)) / 65536 - @saat_part * 256);
    DECLARE @saniye_part INT = ((@saatInt % 65536) - ((@saatInt % 65536) % 256)) / 256;
    
    RETURN RIGHT('00' + CAST(@saat_part AS VARCHAR(2)), 2) + ':' + 
           RIGHT('00' + CAST(@dakika_part AS VARCHAR(2)), 2) + ':' + 
           RIGHT('00' + CAST(@saniye_part AS VARCHAR(2)), 2);
END;
GO

-- Örnek kullanım
DECLARE @mevcutZaman DATETIME = GETDATE();
DECLARE @tarih DATE = CAST(@mevcutZaman AS DATE);
DECLARE @saat TIME = CAST(@mevcutZaman AS TIME);
DECLARE @tarihInt INT;
DECLARE @saatInt INT;
DECLARE @tarihDonusum DATE;
DECLARE @saatDonusum VARCHAR(8);

-- LogoErp formatında sayısal tarih karşılığını hesaplıyoruz
SET @tarihInt = dbo.TarihiIntYap(@tarih);
-- LogoErp formatında sayısal saat karşılığını hesaplıyoruz
SET @saatInt = dbo.SaatiIntYapTime(@saat);

PRINT 'Tarih: ' + CONVERT(VARCHAR, @mevcutZaman, 120);
PRINT 'Tarih LogoErp veritabanındaki sayısal karşılığı: ' + CAST(@tarihInt AS VARCHAR);
PRINT 'Saat LogoErp veritabanındaki sayısal karşılığı: ' + CAST(@saatInt AS VARCHAR);

-- Sayısal tarihi geri DATE değerine dönüştürme
SET @tarihDonusum = dbo.IntiTarihYap(@tarihInt);
-- Sayısal saati geri string formatında (HH:MM:SS) dönüştürme
SET @saatDonusum = dbo.IntiSaatYap(@saatInt);

PRINT 'Tarih dönüşüm: ' + CONVERT(VARCHAR, @tarihDonusum, 23);
PRINT 'Saat dönüşüm: ' + @saatDonusum;
```
