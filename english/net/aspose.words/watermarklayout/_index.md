---
title: WatermarkLayout Enum
linktitle: WatermarkLayout
articleTitle: WatermarkLayout
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.WatermarkLayout enum for optimal watermark positioning. Enhance your document design with precise layout control and customization.
type: docs
weight: 7510
url: /net/aspose.words/watermarklayout/
---
## WatermarkLayout enumeration

Defines layout of the watermark relative to the watermark center.

```csharp
public enum WatermarkLayout
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Horizontal | `0` | Horizontal watermark layout. Corresponds to 0 degrees of rotation. |
| Diagonal | `315` | Diagonal watermark layout. Corresponds to 315 degrees of rotation. |

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

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
