---
title: ImageWatermarkOptions.Scale
linktitle: Scale
articleTitle: Scale
second_title: Aspose.Words for .NET
description: Discover the ImageWatermarkOptions Scale property to easily adjust image scaling for optimal watermarking. Default value, 0 auto for seamless integration.
type: docs
weight: 30
url: /net/aspose.words/imagewatermarkoptions/scale/
---
## ImageWatermarkOptions.Scale property

Gets or sets the scale factor expressed as a fraction of the image. The default value is 0 - auto.

```csharp
public double Scale { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentOutOfRangeException | Throws when argument was out of the range of valid values. |

## Remarks

Valid values range from 0 to 65.5 inclusive.

Auto scale means that the watermark will be scaled to its max width and max height relative to the page margins.

## Examples

Shows how to create a watermark from an image in the local file system.

```csharp
Document doc = new Document();

            // Modify the image watermark's appearance with an ImageWatermarkOptions object,
            // then pass it while creating a watermark from an image file.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA || CPLUSPLUS
            // We have a different options to insert image.
            // Use on of the following methods to add image watermark.
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);

#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
                doc.Watermark.SetImage(image, imageWatermarkOptions);
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### See Also

* class [ImageWatermarkOptions](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
