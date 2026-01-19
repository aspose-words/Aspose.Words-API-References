---
title: PdfZoomBehavior enumeration
linktitle: PdfZoomBehavior enumeration
articleTitle: PdfZoomBehavior enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.PdfZoomBehavior enumeration. Specifies the type of zoom applied to a PDF document when it is opened in a PDF viewer."
type: docs
weight: 750
url: /nodejs-net/aspose.words.saving/pdfzoombehavior/
---

## PdfZoomBehavior enumeration

Specifies the type of zoom applied to a PDF document when it is opened in a PDF viewer.


### Members

| Name | Description |
| --- | --- |
| None | How the document is displayed is left to the PDF viewer. Usually the viewer displays the document to fit page width. |
| ZoomFactor | Displays the page using the specified zoom factor. |
| FitPage | Displays the page so it visible entirely. |
| FitWidth | Fits the width of the page. |
| FitHeight | Fits the height of the page. |
| FitBox | Fits the bounding box (rectangle containing all visible elements on the page). |

### Examples

Shows how to set the default zooming that a reader applies when opening a rendered PDF document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.writeln("Hello world!");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
// Set the "ZoomBehavior" property to "PdfZoomBehavior.ZoomFactor" to get a PDF reader to
// apply a percentage-based zoom factor when we open the document with it.
// Set the "ZoomFactor" property to "25" to give the zoom factor a value of 25%.
let options = new aw.Saving.PdfSaveOptions();
options.zoomBehavior = aw.Saving.PdfZoomBehavior.ZoomFactor;
options.zoomFactor = 25;

// When we open this document using a reader such as Adobe Acrobat, we will see the document scaled at 1/4 of its actual size.
doc.save(base.artifactsDir + "PdfSaveOptions.ZoomBehaviour.pdf", options);
```

### See Also

* module [Aspose.Words.Saving](../)

