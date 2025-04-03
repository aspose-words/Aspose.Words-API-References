---
title: PdfSaveOptions.useBookFoldPrintingSettings property
linktitle: useBookFoldPrintingSettings property
articleTitle: useBookFoldPrintingSettings property
second_title: Aspose.Words for NodeJs
description: "PdfSaveOptions.useBookFoldPrintingSettings property. Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.multiplePages](../../../aspose.words/pagesetup/multiplePages/)."
type: docs
weight: 320
url: /nodejs-net/aspose.words.saving/pdfsaveoptions/useBookFoldPrintingSettings/
---

## PdfSaveOptions.useBookFoldPrintingSettings property

Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout,
if it is specified via [PageSetup.multiplePages](../../../aspose.words/pagesetup/multiplePages/).



```js
get useBookFoldPrintingSettings(): boolean
```

### Remarks

If this option is specified, [FixedPageSaveOptions.pageSet](../../fixedpagesaveoptions/pageSet/) is ignored when saving.
This behavior matches MS Word.
If book fold printing settings are not specified in page setup, this option will have no effect.





### Examples

Shows how to save a document to the PDF format in the form of a book fold.

```js
let doc = new aw.Document(base.myDir + "Paragraphs.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let options = new aw.Saving.PdfSaveOptions();

// Set the "UseBookFoldPrintingSettings" property to "true" to arrange the contents
// in the output PDF in a way that helps us use it to make a booklet.
// Set the "UseBookFoldPrintingSettings" property to "false" to render the PDF normally.
options.useBookFoldPrintingSettings = renderTextAsBookfold;

// If we are rendering the document as a booklet, we must set the "MultiplePages"
// properties of the page setup objects of all sections to "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookfold)
  for (let s of doc.sections.toArray())
  {
    s.pageSetup.multiplePages = aw.Settings.MultiplePagesType.BookFoldPrinting;
  }

// Once we print this document on both sides of the pages, we can fold all the pages down the middle at once,
// and the contents will line up in a way that creates a booklet.
doc.save(base.artifactsDir + "PdfSaveOptions.SaveAsPdfBookFold.pdf", options);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

