---
title: TextWatermarkOptions Class
linktitle: TextWatermarkOptions
articleTitle: TextWatermarkOptions
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.TextWatermarkOptions for customizable text watermarks. Enhance your documents with unique, professional branding options!
type: docs
weight: 7350
url: /net/aspose.words/textwatermarkoptions/
---
## TextWatermarkOptions class

Contains options that can be specified when adding a watermark with text.

To learn more, visit the [Working with Watermark](https://docs.aspose.com/words/net/working-with-watermark/) documentation article.

```csharp
public class TextWatermarkOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [TextWatermarkOptions](textwatermarkoptions/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [Color](../../aspose.words/textwatermarkoptions/color/) { get; set; } | Gets or sets font color. The default value is Silver. |
| [FontFamily](../../aspose.words/textwatermarkoptions/fontfamily/) { get; set; } | Gets or sets font family name. The default value is "Calibri". |
| [FontSize](../../aspose.words/textwatermarkoptions/fontsize/) { get; set; } | Gets or sets a font size. The default value is 0 - auto. |
| [IsSemitrasparent](../../aspose.words/textwatermarkoptions/issemitrasparent/) { get; set; } | Gets or sets a boolean value which is responsible for opacity of the watermark. The default value is `true`. |
| [Layout](../../aspose.words/textwatermarkoptions/layout/) { get; set; } | Gets or sets layout of the watermark. The default value is Diagonal. |

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
