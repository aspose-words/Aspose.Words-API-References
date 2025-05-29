---
title: OdtSaveMeasureUnit Enum
linktitle: OdtSaveMeasureUnit
articleTitle: OdtSaveMeasureUnit
second_title: .NET için Aspose.Words
description: Belge ölçümleri üzerinde hassas kontrol için Aspose.Words.OdtSaveMeasureUnit enum'unu keşfedin. Belge biçimlendirmenizi kolaylıkla geliştirin!
type: docs
weight: 6100
url: /tr/net/aspose.words.saving/odtsavemeasureunit/
---
## OdtSaveMeasureUnit enumeration

Şekil, genişlik ve diğer ölçülebilir belge içeriğine kaydetme sırasında uygulanacak belirtilen ölçü birimleri.

```csharp
public enum OdtSaveMeasureUnit
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Centimeters | `0` | Belge içeriğinin santimetre kullanılarak kaydedildiğini belirtir. |
| Inches | `1` | Belge içeriğinin inç kullanılarak kaydedildiğini belirtir. |

## Örnekler

Kaydedilmiş bir ODT belgesinin stil parametrelerini tanımlamak için farklı ölçüm birimlerinin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Belgeyi .odt'ye aktardığımızda, belgeyi nasıl kaydedeceğimizi değiştirmek için OdtSaveOptions nesnesini kullanabiliriz.
// "MeasureUnit" özelliğini "OdtSaveMeasureUnit.Centimeters" olarak ayarlayabiliriz
 // Open Office'in kullandığı metrik sistemi kullanarak stil parametreleri gibi içerikleri tanımlamak için.
// "MeasureUnit" özelliğini "OdtSaveMeasureUnit.Inches" olarak ayarlayabiliriz
// Microsoft Word'ün kullandığı imparatorluk sistemini kullanarak stil parametreleri gibi içerikleri tanımlamak için.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
