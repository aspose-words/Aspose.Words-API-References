---
title: RevisionOptions.MeasurementUnit
linktitle: MeasurementUnit
articleTitle: MeasurementUnit
second_title: Aspose.Words for .NET
description: RevisionOptions MeasurementUnit property. Allows to specify the measurement units for revision comments. Default value is Centimeters in C#.
type: docs
weight: 60
url: /net/aspose.words.layout/revisionoptions/measurementunit/
---
## RevisionOptions.MeasurementUnit property

Allows to specify the measurement units for revision comments. Default value is Centimeters

```csharp
public MeasurementUnits MeasurementUnit { get; set; }
```

## Examples

Shows how to make a saved document conform to an older ODT schema.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### See Also

* enum [MeasurementUnits](../../../aspose.words/measurementunits/)
* class [RevisionOptions](../)
* namespace [Aspose.Words.Layout](../../../aspose.words.layout/)
* assembly [Aspose.Words](../../../)
