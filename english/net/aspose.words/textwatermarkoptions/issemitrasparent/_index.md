---
title: TextWatermarkOptions.IsSemitrasparent
linktitle: IsSemitrasparent
second_title: Aspose.Words for .NET API Reference
description: TextWatermarkOptions property. Gets or sets a boolean value which is responsible for opacity of the watermark. The default value is true in C#.
type: docs
weight: 50
url: /net/aspose.words/textwatermarkoptions/issemitrasparent/
---
## TextWatermarkOptions.IsSemitrasparent property

Gets or sets a boolean value which is responsible for opacity of the watermark. The default value is `true`.

```csharp
public bool IsSemitrasparent { get; set; }
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
