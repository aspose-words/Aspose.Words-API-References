---
title: WatermarkType Enum
linktitle: WatermarkType
articleTitle: WatermarkType
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.WatermarkType enum for easy watermark customization in documents. Enhance your projects with versatile watermark options!
type: docs
weight: 7550
url: /net/aspose.words/watermarktype/
---
## WatermarkType enumeration

Specifies the watermark type.

```csharp
public enum WatermarkType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Text | `0` | Indicates that the text will be used as a watermark. |
| Image | `1` | Indicates that the image will be used as a watermark. |
| None | `2` | Indicates watermark is no set. |

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
