---
title: Watermarker.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words for .NET
description: Create a new watermarker processor with our innovative method for enhancing your images and protecting your content effortlessly.
type: docs
weight: 10
url: /net/aspose.words.lowcode/watermarker/create/
---
## Watermarker.Create method

Creates new instance of the watermarker processor.

```csharp
public static Watermarker Create(WatermarkerContext context)
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

Shows how to insert watermark image to the document using context.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

WatermarkerContext watermarkerContext = new WatermarkerContext();
watermarkerContext.ImageWatermark = File.ReadAllBytes(watermarkImage);

ImageWatermarkOptions imageWatermarkOptions  = new ImageWatermarkOptions();
imageWatermarkOptions.Scale = 50;
watermarkerContext.ImageWatermarkOptions = imageWatermarkOptions;

Watermarker.Create(watermarkerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.WatermarkContextImage.docx")
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

Shows how to insert watermark image to the document from a stream using context.

```csharp
string watermarkImage = ImageDir + "Logo.jpg";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    WatermarkerContext watermarkerContext = new WatermarkerContext();
    watermarkerContext.ImageWatermark = File.ReadAllBytes(watermarkImage);

    ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
    imageWatermarkOptions.Scale = 50;
    watermarkerContext.ImageWatermarkOptions = imageWatermarkOptions;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkContextImageStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.Create(watermarkerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### See Also

* class [WatermarkerContext](../../watermarkercontext/)
* class [Watermarker](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
