---
title: Watermark.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET
description: Discover the Watermark Type property to enhance your design with customizable watermarks for branding and protection. Elevate your visuals today!
type: docs
weight: 10
url: /net/aspose.words/watermark/type/
---
## Watermark.Type property

Gets the watermark type.

```csharp
public WatermarkType Type { get; }
```

## Examples

Shows how to create a text watermark.

```csharp
Document doc = new Document();

// Add a plain text watermark.
doc.Watermark.SetText("Aspose Watermark");

// If we wish to edit the text formatting using it as a watermark,
// we can do so by passing a TextWatermarkOptions object when creating the watermark.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// We can remove a watermark from a document like this.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### See Also

* enum [WatermarkType](../../watermarktype/)
* class [Watermark](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
