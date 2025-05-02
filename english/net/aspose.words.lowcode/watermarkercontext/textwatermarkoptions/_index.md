---
title: WatermarkerContext.TextWatermarkOptions
linktitle: TextWatermarkOptions
articleTitle: TextWatermarkOptions
second_title: Aspose.Words for .NET
description: Discover customizable options for image watermarks with the WatermarkerContext TextWatermarkOptions property to enhance your visuals and protect your content.
type: docs
weight: 50
url: /net/aspose.words.lowcode/watermarkercontext/textwatermarkoptions/
---
## WatermarkerContext.TextWatermarkOptions property

Options for the image watermark.

```csharp
public TextWatermarkOptions TextWatermarkOptions { get; }
```

## Examples

Shows how to insert watermark text to the document using context.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

WatermarkerContext watermarkerContext = new WatermarkerContext();
watermarkerContext.TextWatermark = watermarkText;

TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.Color = Color.Red;
watermarkerContext.TextWatermarkOptions = textWatermarkOptions;

Watermarker.Create(watermarkerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.WatermarkContextText.docx")
    .Execute();
```

Shows how to insert watermark text to the document from the stream using context.

```csharp
string watermarkText = "This is a watermark";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    WatermarkerContext watermarkerContext = new WatermarkerContext();
    watermarkerContext.TextWatermark = watermarkText;

    TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
    textWatermarkOptions.Color = Color.Red;
    watermarkerContext.TextWatermarkOptions = textWatermarkOptions;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkContextTextStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.Create(watermarkerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### See Also

* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [WatermarkerContext](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
