---
title: PdfZoomBehavior Enum
linktitle: PdfZoomBehavior
articleTitle: PdfZoomBehavior
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.PdfZoomBehavior enum. Specifies the type of zoom applied to a PDF document when it is opened in a PDF viewer in C#.
type: docs
weight: 5720
url: /net/aspose.words.saving/pdfzoombehavior/
---
## PdfZoomBehavior enumeration

Specifies the type of zoom applied to a PDF document when it is opened in a PDF viewer.

```csharp
public enum PdfZoomBehavior
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | How the document is displayed is left to the PDF viewer. Usually the viewer displays the document to fit page width. |
| ZoomFactor | `1` | Displays the page using the specified zoom factor. |
| FitPage | `2` | Displays the page so it visible entirely. |
| FitWidth | `3` | Fits the width of the page. |
| FitHeight | `4` | Fits the height of the page. |
| FitBox | `5` | Fits the bounding box (rectangle containing all visible elements on the page). |

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

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
