---
title: TextWatermarkOptions.FontFamily
linktitle: FontFamily
articleTitle: FontFamily
second_title: Aspose.Words for .NET API Reference
description: TextWatermarkOptions FontFamily property. Gets or sets font family name. The default value is Calibri in C#.
type: docs
weight: 30
url: /net/aspose.words/textwatermarkoptions/fontfamily/
---
## TextWatermarkOptions.FontFamily property

Gets or sets font family name. The default value is "Calibri".

```csharp
public string FontFamily { get; set; }
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

* class [TextWatermarkOptions](../)
* namespace [Aspose.Words](../../textwatermarkoptions/)
* assembly [Aspose.Words](../../../)
