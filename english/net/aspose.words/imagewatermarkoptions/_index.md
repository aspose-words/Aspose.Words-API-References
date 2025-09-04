---
title: ImageWatermarkOptions Class
linktitle: ImageWatermarkOptions
articleTitle: ImageWatermarkOptions
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.ImageWatermarkOptions. Customize your image watermarks effortlessly with versatile options for enhanced document presentation.
type: docs
weight: 3680
url: /net/aspose.words/imagewatermarkoptions/
---
## ImageWatermarkOptions class

Contains options that can be specified when adding a watermark with image.

To learn more, visit the [Working with Watermark](https://docs.aspose.com/words/net/working-with-watermark/) documentation article.

```csharp
public class ImageWatermarkOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [ImageWatermarkOptions](imagewatermarkoptions/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [IsWashout](../../aspose.words/imagewatermarkoptions/iswashout/) { get; set; } | Gets or sets a boolean value which is responsible for washout effect of the watermark. The default value is `true`. |
| [Scale](../../aspose.words/imagewatermarkoptions/scale/) { get; set; } | Gets or sets the scale factor expressed as a fraction of the image. The default value is 0 - auto. |

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

#elif NET6_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
                doc.Watermark.SetImage(image, imageWatermarkOptions);
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
