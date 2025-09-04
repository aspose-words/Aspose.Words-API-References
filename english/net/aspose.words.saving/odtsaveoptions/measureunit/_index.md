---
title: OdtSaveOptions.MeasureUnit
linktitle: MeasureUnit
articleTitle: MeasureUnit
second_title: Aspose.Words for .NET
description: Customize your document's MeasureUnit with OdtSaveOptions. Choose your preferred measurement units for precision—default is Centimeters.
type: docs
weight: 40
url: /net/aspose.words.saving/odtsaveoptions/measureunit/
---
## OdtSaveOptions.MeasureUnit property

Allows to specify units of measure to apply to document content. The default value is Centimeters

```csharp
public OdtSaveMeasureUnit MeasureUnit { get; set; }
```

## Remarks

Open Office uses centimeters when specifying lengths, widths and other measurable formatting and content properties in documents whereas MS Office uses inches.

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

doc = new Document(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt");
Assert.That(doc.LayoutOptions.RevisionOptions.MeasurementUnit, Is.EqualTo(Aspose.Words.MeasurementUnits.Centimeters));
```

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

* enum [OdtSaveMeasureUnit](../../odtsavemeasureunit/)
* class [OdtSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
