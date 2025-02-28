---
title: PdfSaveOptions.PreblendImages
linktitle: PreblendImages
articleTitle: PreblendImages
second_title: Aspose.Words for .NET
description: Discover PdfSaveOptions' PreblendImages property: Easily control transparent image blending for enhanced document quality and visual appeal.
type: docs
weight: 270
url: /net/aspose.words.saving/pdfsaveoptions/preblendimages/
---
## PdfSaveOptions.PreblendImages property

Gets or sets a value determining whether or not to preblend transparent images with black background color.

```csharp
public bool PreblendImages { get; set; }
```

## Remarks

Preblending images may improve PDF document visual appearance in Adobe Reader and remove anti-aliasing artifacts.

In order to properly display preblended images, PDF viewer application must support /Matte entry in soft-mask image dictionary. Also preblending images may decrease PDF rendering performance.

The default value is `false`.

## Examples

Shows how to preblend images with transparent backgrounds while saving a document to PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Transparent background logo.png");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions options = new PdfSaveOptions();
// Set the "PreblendImages" property to "true" to preblend transparent images
// with a background, which may reduce artifacts.
// Set the "PreblendImages" property to "false" to render transparent images normally.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImages.pdf", options);
```

### See Also

* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
