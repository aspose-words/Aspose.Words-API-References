---
title: PdfSaveOptions.displayDocTitle property
linktitle: displayDocTitle property
articleTitle: displayDocTitle property
second_title: Aspose.Words for NodeJs
description: "PdfSaveOptions.displayDocTitle property. A flag specifying whether the window’s title bar should display the document title taken from the Title entry of the document information dictionary."
type: docs
weight: 90
url: /nodejs-net/Aspose.Words.Saving/pdfsaveoptions/displayDocTitle/
---

## PdfSaveOptions.displayDocTitle property

A flag specifying whether the window’s title bar should display the document title taken from
the Title entry of the document information dictionary.


```js
get displayDocTitle(): boolean
```

### Remarks

If ``false``, the title bar should instead display the name of the PDF file containing the document.

This flag is required by PDF/UA compliance. ``true`` value will be used automatically when saving
to PDF/UA.

The default value is ``false``.




### Examples

Shows how to display the title of the document as the title bar.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.writeln("Hello world!");

doc.builtInDocumentProperties.title = "Windows bar pdf title";

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
// Set the "DisplayDocTitle" to "true" to get some PDF readers, such as Adobe Acrobat Pro,
// to display the value of the document's "Title" built-in property in the tab that belongs to this document.
// Set the "DisplayDocTitle" to "false" to get such readers to display the document's filename.
let pdfSaveOptions = new aw.Saving.PdfSaveOptions();
pdfSaveOptions.displayDocTitle = displayDocTitle;;

doc.save(base.artifactsDir + "PdfSaveOptions.DocTitle.pdf", pdfSaveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

