---
title: OdtSaveMeasureUnit Enum
linktitle: OdtSaveMeasureUnit
articleTitle: OdtSaveMeasureUnit
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.OdtSaveMeasureUnit enum for precise control over document measurements. Enhance your document formatting with ease!
type: docs
weight: 6110
url: /net/aspose.words.saving/odtsavemeasureunit/
---
## OdtSaveMeasureUnit enumeration

Specified units of measure to apply to measurable document content such as shape, widths and other during saving.

```csharp
public enum OdtSaveMeasureUnit
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Centimeters | `0` | Specifies that the document content is saved using centimeters. |
| Inches | `1` | Specifies that the document content is saved using inches. |

## Examples

Shows how to use different measurement units to define style parameters of a saved ODT document.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// When we export the document to .odt, we can use an OdtSaveOptions object to modify how we save the document.
// We can set the "MeasureUnit" property to "OdtSaveMeasureUnit.Centimeters"
// to define content such as style parameters using the metric system, which Open Office uses. 
// We can set the "MeasureUnit" property to "OdtSaveMeasureUnit.Inches"
// to define content such as style parameters using the imperial system, which Microsoft Word uses.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
