---
title: WatermarkerContext.TextWatermark
linktitle: TextWatermark
articleTitle: TextWatermark
second_title: Aspose.Words for .NET
description: Discover the WatermarkerContext TextWatermark feature to easily add customizable text watermarks, enhancing your content's security and branding.
type: docs
weight: 40
url: /net/aspose.words.lowcode/watermarkercontext/textwatermark/
---
## WatermarkerContext.TextWatermark property

Text to be used as a watermark.

```csharp
public string TextWatermark { get; set; }
```

## Remarks

If both [`ImageWatermark`](../imagewatermark/) and `TextWatermark` are specified, text watermark overrides image watermark.

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

* class [WatermarkerContext](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
