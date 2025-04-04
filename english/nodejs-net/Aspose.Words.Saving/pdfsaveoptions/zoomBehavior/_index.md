---
title: PdfSaveOptions.zoomBehavior property
linktitle: zoomBehavior property
articleTitle: zoomBehavior property
second_title: Aspose.Words for Node.js
description: "PdfSaveOptions.zoomBehavior property. Gets or sets a value determining what type of zoom should be applied when a document is opened with a PDF viewer."
type: docs
weight: 350
url: /nodejs-net/aspose.words.saving/pdfsaveoptions/zoomBehavior/
---

## PdfSaveOptions.zoomBehavior property

Gets or sets a value determining what type of zoom should be applied when a document is opened with a PDF viewer.


```js
get zoomBehavior(): Aspose.Words.Saving.PdfZoomBehavior
```

### Remarks

The default value is [PdfZoomBehavior.None](../../pdfzoombehavior/#None), i.e. no fit is applied.



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

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

