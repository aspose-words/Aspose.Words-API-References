---
title: OdtSaveOptions.MeasureUnit
second_title: Aspose.Words for .NET API Referansı
description: OdtSaveOptions mülk. Belge içeriğine uygulanacak ölçü birimlerinin belirtilmesine izin verir. Varsayılan değerCentimeters
type: docs
weight: 30
url: /tr/net/aspose.words.saving/odtsaveoptions/measureunit/
---
## OdtSaveOptions.MeasureUnit property

Belge içeriğine uygulanacak ölçü birimlerinin belirtilmesine izin verir. Varsayılan değer:Centimeters

```csharp
public OdtSaveMeasureUnit MeasureUnit { get; set; }
```

### Notlar

Open Office, belgelerde uzunlukları, genişlikleri ve diğer ölçülebilir biçimlendirmeleri ve içerik özelliklerini belirtirken santimetreyi kullanırken, MS Office inç kullanır.

### Örnekler

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

* enum [OdtSaveMeasureUnit](../../odtsavemeasureunit/)
* class [OdtSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../odtsaveoptions/)
* toplantı [Aspose.Words](../../../)


