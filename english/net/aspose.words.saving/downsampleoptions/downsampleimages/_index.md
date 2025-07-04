---
title: DownsampleOptions.DownsampleImages
linktitle: DownsampleImages
articleTitle: DownsampleImages
second_title: Aspose.Words for .NET
description: Discover how the DownsampleImages property optimizes image quality by controlling downsampling for enhanced performance and faster loading times.
type: docs
weight: 20
url: /net/aspose.words.saving/downsampleoptions/downsampleimages/
---
## DownsampleOptions.DownsampleImages property

Specifies whether images should be downsampled.

```csharp
public bool DownsampleImages { get; set; }
```

## Remarks

The default value is `true`.

## Examples

Shows how to change the resolution of images in the PDF document.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// By default, Aspose.Words downsample all images in a document that we save to PDF to 220 ppi.
Assert.That(options.DownsampleOptions.DownsampleImages, Is.True);
Assert.That(options.DownsampleOptions.Resolution, Is.EqualTo(220));
Assert.That(options.DownsampleOptions.ResolutionThreshold, Is.EqualTo(0));

doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

// Set the "Resolution" property to "36" to downsample all images to 36 ppi.
options.DownsampleOptions.Resolution = 36;

// Set the "ResolutionThreshold" property to only apply the downsampling to
// images with a resolution that is above 128 ppi.
options.DownsampleOptions.ResolutionThreshold = 128;

// Only the first two images from the document will be downsampled at this stage.
doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
```

### See Also

* class [DownsampleOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
