---
title: Watermark Class
linktitle: Watermark
articleTitle: Watermark
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Watermark class to easily add and customize watermarks in your documents, enhancing professionalism and branding.
type: docs
weight: 7500
url: /net/aspose.words/watermark/
---
## Watermark class

Represents class to work with document watermark.

To learn more, visit the [Working with Watermark](https://docs.aspose.com/words/net/working-with-watermark/) documentation article.

```csharp
public sealed class Watermark
```

## Properties

| Name | Description |
| --- | --- |
| [Type](../../aspose.words/watermark/type/) { get; } | Gets the watermark type. |

## Methods

| Name | Description |
| --- | --- |
| [Remove](../../aspose.words/watermark/remove/)() | Removes the watermark. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage)(*Image*) | Adds Image watermark into the document. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_1)(*Image, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Adds Image watermark into the document. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_2)(*Stream, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Adds Image watermark into the document. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_3)(*string, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Adds Image watermark into the document. |
| [SetText](../../aspose.words/watermark/settext/#settext)(*string*) | Adds Text watermark into the document. |
| [SetText](../../aspose.words/watermark/settext/#settext_1)(*string, [TextWatermarkOptions](../textwatermarkoptions/)*) | Adds Text watermark into the document. |

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
