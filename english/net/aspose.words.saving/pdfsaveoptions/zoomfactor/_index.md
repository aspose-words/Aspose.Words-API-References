---
title: PdfSaveOptions.ZoomFactor
linktitle: ZoomFactor
articleTitle: ZoomFactor
second_title: Aspose.Words for .NET
description: Discover PdfSaveOptions' ZoomFactor property to easily adjust document zoom levels in percentages, enhancing your PDF viewing experience.
type: docs
weight: 360
url: /net/aspose.words.saving/pdfsaveoptions/zoomfactor/
---
## PdfSaveOptions.ZoomFactor property

Gets or sets a value determining zoom factor (in percentages) for a document.

```csharp
public int ZoomFactor { get; set; }
```

## Remarks

This value is used only if [`ZoomBehavior`](../zoombehavior/) is set to ZoomFactor.

## Examples

Shows how to set the default zooming that a reader applies when opening a rendered PDF document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
// Set the "ZoomBehavior" property to "PdfZoomBehavior.ZoomFactor" to get a PDF reader to
// apply a percentage-based zoom factor when we open the document with it.
// Set the "ZoomFactor" property to "25" to give the zoom factor a value of 25%.
PdfSaveOptions options = new PdfSaveOptions
{
    ZoomBehavior = PdfZoomBehavior.ZoomFactor,
    ZoomFactor = 25
};

// When we open this document using a reader such as Adobe Acrobat, we will see the document scaled at 1/4 of its actual size.
doc.Save(ArtifactsDir + "PdfSaveOptions.ZoomBehaviour.pdf", options);
```

### See Also

* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
