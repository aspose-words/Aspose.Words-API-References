---
title: RevisionOptions.MeasurementUnit
linktitle: MeasurementUnit
articleTitle: MeasurementUnit
second_title: .NET için Aspose.Words
description: Revizyon yorumlarınızı RevisionOptions MeasurementUnit özelliğiyle özelleştirin. Varsayılan olarak Santimetre ile ölçüm birimlerini kolayca ayarlayın.
type: docs
weight: 80
url: /tr/net/aspose.words.layout/revisionoptions/measurementunit/
---
## RevisionOptions.MeasurementUnit property

Gözden geçirme yorumları için ölçüm birimlerini belirtmeye olanak tanır. Varsayılan değerCentimeters

```csharp
public MeasurementUnits MeasurementUnit { get; set; }
```

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

* enum [MeasurementUnits](../../../aspose.words/measurementunits/)
* class [RevisionOptions](../)
* ad alanı [Aspose.Words.Layout](../../../aspose.words.layout/)
* toplantı [Aspose.Words](../../../)
