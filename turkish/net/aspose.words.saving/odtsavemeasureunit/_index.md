---
title: Enum OdtSaveMeasureUnit
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.OdtSaveMeasureUnit Sıralama. Kaydetme sırasında şekil genişlik ve diğer ölçülebilir belge içeriğine uygulanacak belirli ölçü birimleri.
type: docs
weight: 5040
url: /tr/net/aspose.words.saving/odtsavemeasureunit/
---
## OdtSaveMeasureUnit enumeration

Kaydetme sırasında şekil, genişlik ve diğer ölçülebilir belge içeriğine uygulanacak belirli ölçü birimleri.

```csharp
public enum OdtSaveMeasureUnit
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Centimeters | `0` | Belge içeriğinin santimetre kullanılarak kaydedildiğini belirtir. |
| Inches | `1` | Belge içeriğinin inç kullanılarak kaydedildiğini belirtir. |

### Örnekler

Kaydedilmiş bir ODT belgesinin stil parametrelerini tanımlamak için farklı ölçü birimlerinin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Belgeyi .odt'a aktardığımızda, belgeyi kaydetme şeklimizi değiştirmek için bir OdtSaveOptions nesnesini kullanabiliriz.
// "MeasureUnit" özelliğini "OdtSaveMeasureUnit.Santimetre" olarak ayarlayabiliriz.
// Open Office'in kullandığı metrik sistemi kullanarak stil parametreleri gibi içerikleri tanımlamak için. 
// "MeasureUnit" özelliğini "OdtSaveMeasureUnit.Inches" olarak ayarlayabiliriz.
// Microsoft Word'ün kullandığı emperyal sistemi kullanarak stil parametreleri gibi içeriği tanımlamak için.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


