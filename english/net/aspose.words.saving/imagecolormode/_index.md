---
title: ImageColorMode Enum
linktitle: ImageColorMode
articleTitle: ImageColorMode
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.Saving.ImageColorMode enum to optimize document page images. Control color modes for enhanced visual quality in your projects.
type: docs
weight: 5950
url: /net/aspose.words.saving/imagecolormode/
---
## ImageColorMode enumeration

Specifies the color mode for the generated images of document pages.

```csharp
public enum ImageColorMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | The pages of the document will be rendered as color images. |
| Grayscale | `1` | The pages of the document will be rendered as grayscale images. |
| BlackAndWhite | `2` | The pages of the document will be rendered as black and white images. |

## Examples

Shows how to set a color mode when rendering documents.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// When we save the document as an image, we can pass a SaveOptions object to
// select a color mode for the image that the saving operation will generate.
// If we set the "ImageColorMode" property to "ImageColorMode.BlackAndWhite",
// the saving operation will apply grayscale color reduction while rendering the document.
// If we set the "ImageColorMode" property to "ImageColorMode.Grayscale", 
// the saving operation will render the document into a monochrome image.
// If we set the "ImageColorMode" property to "None", the saving operation will apply the default method
// and preserve all the document's colors in the output image.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.ImageColorMode = imageColorMode;

doc.Save(ArtifactsDir + "ImageSaveOptions.ColorMode.png", imageSaveOptions);
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
