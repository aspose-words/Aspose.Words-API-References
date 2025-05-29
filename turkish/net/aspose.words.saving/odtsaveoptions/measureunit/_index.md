---
title: OdtSaveOptions.MeasureUnit
linktitle: MeasureUnit
articleTitle: MeasureUnit
second_title: .NET için Aspose.Words
description: OdtSaveOptions ile belgenizin MeasureUnit'ini özelleştirin. Hassasiyet için tercih ettiğiniz ölçüm birimlerini seçin; varsayılan Santimetre'dir.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/odtsaveoptions/measureunit/
---
## OdtSaveOptions.MeasureUnit property

Belge içeriğine uygulanacak ölçü birimlerini belirtmenize olanak tanır. Varsayılan değerCentimeters

```csharp
public OdtSaveMeasureUnit MeasureUnit { get; set; }
```

## Notlar

Open Office, belgelerde uzunlukları, genişlikleri ve diğer ölçülebilir biçimlendirmeleri ve içerik özelliklerini belirtirken santimetre kullanır, oysa MS Office inç kullanır.

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

* enum [OdtSaveMeasureUnit](../../odtsavemeasureunit/)
* class [OdtSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
