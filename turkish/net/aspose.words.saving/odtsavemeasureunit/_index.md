---
title: OdtSaveMeasureUnit Enum
linktitle: OdtSaveMeasureUnit
articleTitle: OdtSaveMeasureUnit
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.OdtSaveMeasureUnit Sıralama. Kaydetme sırasında şekil genişlik ve diğer gibi ölçülebilir belge içeriğine uygulanacak ölçü birimleri belirtildi C#'da.
type: docs
weight: 5320
url: /tr/net/aspose.words.saving/odtsavemeasureunit/
---
## OdtSaveMeasureUnit enumeration

Kaydetme sırasında şekil, genişlik ve diğer gibi ölçülebilir belge içeriğine uygulanacak ölçü birimleri belirtildi.

```csharp
public enum OdtSaveMeasureUnit
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Centimeters | `0` | Belge içeriğinin santimetre kullanılarak kaydedildiğini belirtir. |
| Inches | `1` | Belge içeriğinin inç kullanılarak kaydedildiğini belirtir. |

## Örnekler

Kaydedilmiş bir ODT belgesinin stil parametrelerini tanımlamak için farklı ölçü birimlerinin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Belgeyi .odt'a aktardığımızda, belgeyi kaydetme şeklimizi değiştirmek için OdtSaveOptions nesnesini kullanabiliriz.
// "MeasureUnit" özelliğini "OdtSaveMeasureUnit.Centimeters" olarak ayarlayabiliriz
 // stil parametreleri gibi içerikleri Open Office'in kullandığı metrik sistemi kullanarak tanımlamak için.
// "MeasureUnit" özelliğini "OdtSaveMeasureUnit.Inches" olarak ayarlayabiliriz
// Microsoft Word'ün kullandığı emperyal sistemi kullanarak stil parametreleri gibi içerikleri tanımlamak için.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
