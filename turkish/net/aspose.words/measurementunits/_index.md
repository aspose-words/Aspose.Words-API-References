---
title: MeasurementUnits Enum
linktitle: MeasurementUnits
articleTitle: MeasurementUnits
second_title: .NET için Aspose.Words
description: Belge işlemede hassas birim seçimi için Aspose.Words.MeasurementUnits enum'unu keşfedin. Doğru ölçüm seçenekleriyle iş akışınızı geliştirin!
type: docs
weight: 4840
url: /tr/net/aspose.words/measurementunits/
---
## MeasurementUnits enumeration

Ölçüm birimini belirtir.

```csharp
public enum MeasurementUnits
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Inches | `0` | İnç. |
| Centimeters | `1` | Santimetre. |
| Millimeters | `2` | Milimetre. |
| Points | `3` | Puanlar. |
| Picas | `4` | Picas (genellikle geleneksel daktilo yazı tipi aralıklarında kullanılır). |

## Örnekler

Kaydedilmiş bir belgenin eski bir ODT şemasına uygun hale getirilmesinin nasıl yapılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
