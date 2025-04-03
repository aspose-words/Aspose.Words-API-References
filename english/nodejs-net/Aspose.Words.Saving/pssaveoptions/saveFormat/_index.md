---
title: PsSaveOptions.saveFormat property
linktitle: saveFormat property
articleTitle: saveFormat property
second_title: Aspose.Words for NodeJs
description: "PsSaveOptions.saveFormat property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 20
url: /nodejs-net/aspose.words.saving/pssaveoptions/saveFormat/
---

## PsSaveOptions.saveFormat property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.Ps](../../../aspose.words/saveformat/#Ps).



```js
get saveFormat(): Aspose.Words.SaveFormat
```

### Examples

Shows how to save a document to the Postscript format in the form of a book fold.

```js
let doc = new aw.Document(base.myDir + "Paragraphs.docx");

// Create a "PsSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to PostScript.
// Set the "UseBookFoldPrintingSettings" property to "true" to arrange the contents
// in the output Postscript document in a way that helps us make a booklet out of it.
// Set the "UseBookFoldPrintingSettings" property to "false" to save the document normally.
let saveOptions = new aw.Saving.PsSaveOptions()
saveOptions.saveFormat = aw.SaveFormat.Ps;
saveOptions.useBookFoldPrintingSettings = renderTextAsBookFold;

// If we are rendering the document as a booklet, we must set the "MultiplePages"
// properties of the page setup objects of all sections to "MultiplePagesType.BookFoldPrinting".
for (let s of doc.sections)
{
  let section = s.asSection();
  section.pageSetup.multiplePages = aw.Settings.MultiplePagesType.BookFoldPrinting;
}

// Once we print this document on both sides of the pages, we can fold all the pages down the middle at once,
// and the contents will line up in a way that creates a booklet.
doc.save(base.artifactsDir + "PsSaveOptions.useBookFoldPrintingSettings.ps", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [PsSaveOptions](../)

