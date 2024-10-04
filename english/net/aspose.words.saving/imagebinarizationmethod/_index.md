---
title: ImageBinarizationMethod Enum
linktitle: ImageBinarizationMethod
articleTitle: ImageBinarizationMethod
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.ImageBinarizationMethod enum. Specifies the method used to binarize image in C#.
type: docs
weight: 5560
url: /net/aspose.words.saving/imagebinarizationmethod/
---
## ImageBinarizationMethod enumeration

Specifies the method used to binarize image.

```csharp
public enum ImageBinarizationMethod
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Threshold | `0` | Specifies threshold method. |
| FloydSteinbergDithering | `1` | Specifies dithering using Floyd-Steinberg error diffusion method. |

## Examples

Shows how to set the TIFF binarization error threshold when using the Floyd-Steinberg method to render a TIFF image.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// When we save the document as a TIFF, we can pass a SaveOptions object to
// adjust the dithering that Aspose.Words will apply when rendering this image.
// The default value of the "ThresholdForFloydSteinbergDithering" property is 128.
// Higher values tend to produce darker images.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff)
{
    TiffCompression = TiffCompression.Ccitt3,
    TiffBinarizationMethod = ImageBinarizationMethod.FloydSteinbergDithering,
    ThresholdForFloydSteinbergDithering = 240
};

doc.Save(ArtifactsDir + "ImageSaveOptions.FloydSteinbergDithering.tiff", options);
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
