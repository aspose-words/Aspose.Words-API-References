---
title: XlsxDateTimeParsingMode Enum
linktitle: XlsxDateTimeParsingMode
articleTitle: XlsxDateTimeParsingMode
second_title: .NET için Aspose.Words
description: Verimli belge metni ayrıştırma için Aspose.Words' XlsxDateTimeParsingMode enum'unu keşfedin. Dosyalarınızdaki tarih ve saat değerlerini kolayca tanımlayın!
type: docs
weight: 6510
url: /tr/net/aspose.words.saving/xlsxdatetimeparsingmode/
---
## XlsxDateTimeParsingMode enumeration

Belge metninin tarih ve saat değerlerini tanımlamak için nasıl ayrıştırılacağını belirtir.

```csharp
public enum XlsxDateTimeParsingMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| UseCurrentLocale | `0` | Geçerli iş parçacığı için ayarlanan tarih-saat biçimi, dize değerlerini ayrıştırmak için ilk önce kullanılır. Ayrıştırma başarısız olursa, diğer yaygın tarih-saat biçimleri denenir. |
| Auto | `1` | Bir belgede kullanılan tarih/saat biçimi otomatik olarak belirlenir. Bu ek zaman alabilir. |

## Örnekler

Tarih saat biçiminin otomatik olarak algılanmasının nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Xlsx DateTime.docx");

XlsxSaveOptions saveOptions = new XlsxSaveOptions();
// Datetime formatını otomatik algılama kullanarak belirtin.
saveOptions.DateTimeParsingMode = XlsxDateTimeParsingMode.Auto;

doc.Save(ArtifactsDir + "XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
