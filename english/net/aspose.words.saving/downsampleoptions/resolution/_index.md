---
title: DownsampleOptions.Resolution
linktitle: Resolution
articleTitle: Resolution
second_title: Aspose.Words for .NET
description: Optimize image quality with the DownsampleOptions Resolution property, defining the ideal pixels per inch for superior downsampling results.
type: docs
weight: 30
url: /net/aspose.words.saving/downsampleoptions/resolution/
---
## DownsampleOptions.Resolution property

Specifies the resolution in pixels per inch which the images should be downsampled to.

```csharp
public int Resolution { get; set; }
```

## Remarks

The default value is 220 ppi.

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
