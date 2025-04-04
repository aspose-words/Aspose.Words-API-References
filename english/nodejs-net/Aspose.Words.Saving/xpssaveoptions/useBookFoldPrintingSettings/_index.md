---
title: XpsSaveOptions.useBookFoldPrintingSettings property
linktitle: useBookFoldPrintingSettings property
articleTitle: useBookFoldPrintingSettings property
second_title: Aspose.Words for Node.js
description: "XpsSaveOptions.useBookFoldPrintingSettings property. Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.multiplePages](../../../aspose.words/pagesetup/multiplePages/)."
type: docs
weight: 50
url: /nodejs-net/aspose.words.saving/xpssaveoptions/useBookFoldPrintingSettings/
---

## XpsSaveOptions.useBookFoldPrintingSettings property

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

Shows how to save a document to the XPS format in the form of a book fold.

```js
let doc = new aw.Document(base.myDir + "Paragraphs.docx");

// Create an "XpsSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .XPS.
let xpsOptions = new aw.Saving.XpsSaveOptions(aw.SaveFormat.Xps);

// Set the "UseBookFoldPrintingSettings" property to "true" to arrange the contents
// in the output XPS in a way that helps us use it to make a booklet.
// Set the "UseBookFoldPrintingSettings" property to "false" to render the XPS normally.
xpsOptions.useBookFoldPrintingSettings = renderTextAsBookFold;

// If we are rendering the document as a booklet, we must set the "MultiplePages"
// properties of the page setup objects of all sections to "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookFold)
  for (let s of doc.sections.toArray())
  {
    s.pageSetup.multiplePages = aw.Settings.MultiplePagesType.BookFoldPrinting;
  }

// Once we print this document, we can turn it into a booklet by stacking the pages
// to come out of the printer and folding down the middle.
doc.save(base.artifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [XpsSaveOptions](../)

