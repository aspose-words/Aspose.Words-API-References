---
title: Document.Watermark
linktitle: Watermark
articleTitle: Watermark
second_title: Aspose.Words for .NET
description: Secure your documents with our customizable watermarking feature. Enhance protection and ensure authenticity effortlessly!
type: docs
weight: 500
url: /net/aspose.words/document/watermark/
---
## Document.Watermark property

Provides access to the document watermark.

```csharp
public Watermark Watermark { get; }
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

* class [Watermark](../../watermark/)
* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
