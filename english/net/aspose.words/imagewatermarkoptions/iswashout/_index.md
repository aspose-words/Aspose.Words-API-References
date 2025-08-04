---
title: ImageWatermarkOptions.IsWashout
linktitle: IsWashout
articleTitle: IsWashout
second_title: Aspose.Words for .NET
description: Discover the IsWashout property of ImageWatermarkOptions. Control your watermark's washout effect effortlessly with this simple boolean setting.
type: docs
weight: 20
url: /net/aspose.words/imagewatermarkoptions/iswashout/
---
## ImageWatermarkOptions.IsWashout property

Gets or sets a boolean value which is responsible for washout effect of the watermark. The default value is `true`.

```csharp
public bool IsWashout { get; set; }
```

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

* class [ImageWatermarkOptions](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
