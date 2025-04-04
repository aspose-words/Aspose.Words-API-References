---
title: WatermarkerContext.ImageWatermarkOptions
linktitle: ImageWatermarkOptions
articleTitle: ImageWatermarkOptions
second_title: Aspose.Words for .NET
description: Discover customizable text watermark options with WatermarkerContext to enhance your images and protect your brand's identity effectively.
type: docs
weight: 30
url: /net/aspose.words.lowcode/watermarkercontext/imagewatermarkoptions/
---
## WatermarkerContext.ImageWatermarkOptions property

Options for the text watermark.

```csharp
public ImageWatermarkOptions ImageWatermarkOptions { get; set; }
```

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

* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [WatermarkerContext](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
