---
title: ImagePixelFormat Enum
linktitle: ImagePixelFormat
articleTitle: ImagePixelFormat
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.ImagePixelFormat enum. Specifies the pixel format for the generated images of document pages in C#.
type: docs
weight: 5830
url: /net/aspose.words.saving/imagepixelformat/
---
## ImagePixelFormat enumeration

Specifies the pixel format for the generated images of document pages.

```csharp
public enum ImagePixelFormat
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Format16BppRgb555 | `0` | 16 bits per pixel, RGB. |
| Format16BppRgb565 | `1` | 16 bits per pixel, RGB. |
| Format16BppArgb1555 | `2` | 16 bits per pixel, ARGB. |
| Format24BppRgb | `3` | 24 bits per pixel, RGB. |
| Format32BppRgb | `4` | 32 bits per pixel, RGB. |
| Format32BppArgb | `5` | 32 bits per pixel, ARGB. |
| Format32BppPArgb | `6` | 32 bits per pixel, ARGB, premultiplied alpha. |
| Format48BppRgb | `7` | 48 bits per pixel, RGB. |
| Format64BppArgb | `8` | 64 bits per pixel, ARGB. |
| Format64BppPArgb | `9` | 64 bits per pixel, ARGB, premultiplied alpha. |
| Format1bppIndexed | `10` | 1 bit per pixel, Indexed. |

## Examples

Shows how to select a bit-per-pixel rate with which to render a document to an image.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// When we save the document as an image, we can pass a SaveOptions object to
// select a pixel format for the image that the saving operation will generate.
// Various bit per pixel rates will affect the quality and file size of the generated image.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PixelFormat = imagePixelFormat;

// We can clone ImageSaveOptions instances.
Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
