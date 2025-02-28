---
title: FixedPageSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words for .NET
description: Optimize JPEG quality in your HTML documents with FixedPageSaveOptions. Easily adjust the JpegQuality property for stunning image clarity.
type: docs
weight: 20
url: /net/aspose.words.saving/fixedpagesaveoptions/jpegquality/
---
## FixedPageSaveOptions.JpegQuality property

Gets or sets a value determining the quality of the JPEG images inside Html document.

```csharp
public int JpegQuality { get; set; }
```

## Remarks

Has effect only when a document contains JPEG images.

Use this property to get or set the quality of the images inside a document when saving in fixed page format. The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100 means best quality but minimum compression.

The default value is 95.

## Examples

Shows how to configure compression while saving a document as a JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);
// Set the "JpegQuality" property to "10" to use stronger compression when rendering the document.
// This will reduce the file size of the document, but the image will display more prominent compression artifacts.
imageOptions.JpegQuality = 10;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Set the "JpegQuality" property to "100" to use weaker compression when rending the document.
// This will improve the quality of the image at the cost of an increased file size.
imageOptions.JpegQuality = 100;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

### See Also

* class [FixedPageSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
