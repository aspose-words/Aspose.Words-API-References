---
title: PdfSaveOptions.DownsampleOptions
linktitle: DownsampleOptions
articleTitle: DownsampleOptions
second_title: Aspose.Words for .NET
description: Discover PdfSaveOptions' DownsampleOptions property to customize your PDF quality and optimize file size for better performance and clarity.
type: docs
weight: 110
url: /net/aspose.words.saving/pdfsaveoptions/downsampleoptions/
---
## PdfSaveOptions.DownsampleOptions property

Allows to specify downsample options.

```csharp
public DownsampleOptions DownsampleOptions { get; set; }
```

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

* class [DownsampleOptions](../../downsampleoptions/)
* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
