---
title: Watermark.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words for .NET
description: Effortlessly remove watermarks with our effective method. Restore your images to their original beauty and enhance your creative projects today!
type: docs
weight: 20
url: /net/aspose.words/watermark/remove/
---
## Watermark.Remove method

Removes the watermark.

```csharp
public void Remove()
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

* class [Watermark](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
