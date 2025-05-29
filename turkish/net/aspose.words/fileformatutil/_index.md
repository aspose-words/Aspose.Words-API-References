---
title: FileFormatUtil Class
linktitle: FileFormatUtil
articleTitle: FileFormatUtil
second_title: .NET için Aspose.Words
description: Aspose.Words.FileFormatUtil ile dosya formatlarını zahmetsizce yönetin. Gelişmiş üretkenlik için formatları algılayın ve uzantıları sorunsuz bir şekilde dönüştürün.
type: docs
weight: 3230
url: /tr/net/aspose.words/fileformatutil/
---
## FileFormatUtil class

Dosya biçimleriyle çalışmak için yardımcı yöntemler sağlar, örneğin dosya biçimini algılamak veya dosya uzantılarını dosya biçimi sayımlarına dönüştürmek/dosya biçimi sayımlarından dönüştürmek.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Dosya Biçimini Algıla ve Biçim Uyumluluğunu Kontrol Et](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/) belgeleme makalesi.

```csharp
public static class FileFormatUtil
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| static [ContentTypeToLoadFormat](../../aspose.words/fileformatutil/contenttypetoloadformat/)(*string*) | IANA içerik türünü yükleme biçiminde numaralandırılmış bir değere dönüştürür. |
| static [ContentTypeToSaveFormat](../../aspose.words/fileformatutil/contenttypetosaveformat/)(*string*) | IANA içerik türünü, numaralandırılmış bir kaydetme biçimi değerine dönüştürür. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat)(*Stream*) | Bir akışta depolanan bir belgenin biçimi hakkında bilgi algılar ve döndürür. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat_1)(*string*) | Bir disk dosyasında saklanan bir belgenin biçimi hakkında bilgi algılar ve döndürür. |
| static [ExtensionToSaveFormat](../../aspose.words/fileformatutil/extensiontosaveformat/)(*string*) | Bir dosya adı uzantısını bir[`SaveFormat`](../saveformat/) değer. |
| static [ImageTypeToExtension](../../aspose.words/fileformatutil/imagetypetoextension/)(*[ImageType](../../aspose.words.drawing/imagetype/)*) | Aspose.Words görüntü türünde numaralandırılmış bir değeri dosya uzantısına dönüştürür. Döndürülen uzantı, başında nokta bulunan küçük harfli bir dizedir. |
| static [LoadFormatToExtension](../../aspose.words/fileformatutil/loadformattoextension/)(*[LoadFormat](../loadformat/)*) | Yükleme biçiminde numaralandırılmış bir değeri dosya uzantısına dönüştürür. Döndürülen uzantı, başında nokta bulunan küçük harfli bir dizedir. |
| static [LoadFormatToSaveFormat](../../aspose.words/fileformatutil/loadformattosaveformat/)(*[LoadFormat](../loadformat/)*) | Birini dönüştürür[`LoadFormat`](../loadformat/) bir değere[`SaveFormat`](../saveformat/) mümkünse değer. |
| static [SaveFormatToExtension](../../aspose.words/fileformatutil/saveformattoextension/)(*[SaveFormat](../saveformat/)*) | Kayıtlı formatta numaralandırılmış bir değeri dosya uzantısına dönüştürür. Döndürülen uzantı, başında nokta bulunan küçük harfli bir dizedir. |
| static [SaveFormatToLoadFormat](../../aspose.words/fileformatutil/saveformattoloadformat/)(*[SaveFormat](../saveformat/)*) | Birini dönüştürür[`SaveFormat`](../saveformat/) bir değere[`LoadFormat`](../loadformat/) mümkünse değer. |

## Örnekler

Bir html dosyasındaki kodlamanın nasıl tespit edileceğini gösterir.

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
