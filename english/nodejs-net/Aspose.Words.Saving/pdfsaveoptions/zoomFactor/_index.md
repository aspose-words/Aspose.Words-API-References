---
title: PdfSaveOptions.zoomFactor property
linktitle: zoomFactor property
articleTitle: zoomFactor property
second_title: Aspose.Words for NodeJs
description: "PdfSaveOptions.zoomFactor property. Gets or sets a value determining zoom factor (in percentages) for a document."
type: docs
weight: 360
url: /nodejs-net/Aspose.Words.Saving/pdfsaveoptions/zoomFactor/
---

## PdfSaveOptions.zoomFactor property

Gets or sets a value determining zoom factor (in percentages) for a document.


```js
get zoomFactor(): number
```

### Remarks

This value is used only if [PdfSaveOptions.zoomBehavior](../zoomBehavior/) is set to [PdfZoomBehavior.ZoomFactor](../../pdfzoombehavior/#ZoomFactor).



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

