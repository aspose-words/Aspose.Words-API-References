---
title: Class FileFormatUtil
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.FileFormatUtil sınıf. Dosya formatlarıyla çalışmak için dosya formatını algılamak veya dosya uzantılarını dosya formatı numaralandırmalarına/dosya formatlarından dönüştürmek gibi yardımcı yöntemler sağlar.
type: docs
weight: 2820
url: /tr/net/aspose.words/fileformatutil/
---
## FileFormatUtil class

Dosya formatlarıyla çalışmak için, dosya formatını algılamak veya dosya uzantılarını dosya formatı numaralandırmalarına/dosya formatlarından dönüştürmek gibi yardımcı yöntemler sağlar.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Dosya Formatını Algıla ve Format Uyumluluğunu Kontrol Et](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/) dokümantasyon makalesi.

```csharp
public static class FileFormatUtil
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| static [ContentTypeToLoadFormat](../../aspose.words/fileformatutil/contenttypetoloadformat/)(string) | IANA içerik türünü, yükleme biçiminde numaralandırılmış bir değere dönüştürür. |
| static [ContentTypeToSaveFormat](../../aspose.words/fileformatutil/contenttypetosaveformat/)(string) | IANA içerik türünü, kaydetme biçiminde numaralandırılmış bir değere dönüştürür. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat)(Stream) | Bir akışta saklanan bir belgenin biçimi hakkındaki bilgileri algılar ve döndürür. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat_1)(string) | Disk dosyasında saklanan bir belgenin biçimi hakkındaki bilgileri algılar ve döndürür. |
| static [ExtensionToSaveFormat](../../aspose.words/fileformatutil/extensiontosaveformat/)(string) | Dosya adı uzantısını bir dosya adı uzantısına dönüştürür[`SaveFormat`](../saveformat/) değer. |
| static [ImageTypeToExtension](../../aspose.words/fileformatutil/imagetypetoextension/)(ImageType) | Aspose.Words görüntü türü numaralandırılmış değerini bir dosya uzantısına dönüştürür. Döndürülen uzantı, başında nokta bulunan küçük harfli bir dizedir. |
| static [LoadFormatToExtension](../../aspose.words/fileformatutil/loadformattoextension/)(LoadFormat) | Yükleme biçimi numaralandırılmış değerini bir dosya uzantısına dönüştürür. Döndürülen uzantı, başında nokta bulunan küçük harfli bir dizedir. |
| static [LoadFormatToSaveFormat](../../aspose.words/fileformatutil/loadformattosaveformat/)(LoadFormat) | Bir'i dönüştürür[`LoadFormat`](../loadformat/) bir değer[`SaveFormat`](../saveformat/) mümkünse değer. |
| static [SaveFormatToExtension](../../aspose.words/fileformatutil/saveformattoextension/)(SaveFormat) | Kayıt biçimi numaralandırılmış değerini bir dosya uzantısına dönüştürür. Döndürülen uzantı, başında nokta bulunan küçük harfli bir dizedir. |
| static [SaveFormatToLoadFormat](../../aspose.words/fileformatutil/saveformattoloadformat/)(SaveFormat) | Bir'i dönüştürür[`SaveFormat`](../saveformat/) bir değer[`LoadFormat`](../loadformat/) mümkünse değer. |

### Örnekler

Bir html dosyasındaki kodlamanın nasıl algılanacağını gösterir.

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// Encoding özelliği yalnızca bir html belgesi için FileFormatInfo nesnesi oluşturduğumuzda kullanılır.
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


