---
title: XlsxSaveOptions.DateTimeParsingMode
linktitle: DateTimeParsingMode
articleTitle: DateTimeParsingMode
second_title: .NET için Aspose.Words
description: Belgenizin tarih ve saatleri nasıl ayrıştıracağını özelleştirmek ve doğru veri yorumlamasını sağlamak için XlsxSaveOptions' DateTimeParsingMode özelliğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/xlsxsaveoptions/datetimeparsingmode/
---
## XlsxSaveOptions.DateTimeParsingMode property

Belge metninin tarih ve saat değerlerini tanımlamak için nasıl ayrıştırılacağını belirten modu alır veya ayarlar. Varsayılan değerUseCurrentLocale .

```csharp
public XlsxDateTimeParsingMode DateTimeParsingMode { get; set; }
```

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

* enum [XlsxDateTimeParsingMode](../../xlsxdatetimeparsingmode/)
* class [XlsxSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
