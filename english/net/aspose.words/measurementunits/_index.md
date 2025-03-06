---
title: MeasurementUnits Enum
linktitle: MeasurementUnits
articleTitle: MeasurementUnits
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.MeasurementUnits enum for precise unit selection in document processing. Enhance your workflow with accurate measurement options!
type: docs
weight: 4700
url: /net/aspose.words/measurementunits/
---
## MeasurementUnits enumeration

Specifies the unit of measurement.

```csharp
public enum MeasurementUnits
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Inches | `0` | Inches. |
| Centimeters | `1` | Centimeters. |
| Millimeters | `2` | Millimeters. |
| Points | `3` | Points. |
| Picas | `4` | Picas (commonly used in traditional typewriter font spacing). |

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

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
