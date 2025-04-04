---
title: WatermarkerContext.ImageWatermark
linktitle: ImageWatermark
articleTitle: ImageWatermark
second_title: Aspose.Words for .NET
description: Discover how to enhance your images with the WatermarkerContext ImageWatermark property, allowing you to add custom watermark images effortlessly.
type: docs
weight: 20
url: /net/aspose.words.lowcode/watermarkercontext/imagewatermark/
---
## WatermarkerContext.ImageWatermark property

Image bytes to be used as a watermark.

```csharp
public byte[] ImageWatermark { get; set; }
```

## Remarks

If both `ImageWatermark` and [`TextWatermark`](../textwatermark/) are specified, text watermark overrides image watermark.

## Examples

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

* class [WatermarkerContext](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
