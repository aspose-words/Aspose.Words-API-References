---
title: PdfSaveOptions.createNoteHyperlinks property
linktitle: createNoteHyperlinks property
articleTitle: createNoteHyperlinks property
second_title: Aspose.Words for NodeJs
description: "PdfSaveOptions.createNoteHyperlinks property. Specifies whether to convert footnote/endnote references in main text story into active hyperlinks"
type: docs
weight: 60
url: /nodejs-net/aspose.words.saving/pdfsaveoptions/createNoteHyperlinks/
---

## PdfSaveOptions.createNoteHyperlinks property

Specifies whether to convert footnote/endnote references in main text story into active hyperlinks.
When clicked the hyperlink will lead to the corresponding footnote/endnote.
Default is ``false``.



```js
get createNoteHyperlinks(): boolean
```

### Examples

Shows how to make footnotes and endnotes function as hyperlinks.

```js
let doc = new aw.Document(base.myDir + "Footnotes and endnotes.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let options = new aw.Saving.PdfSaveOptions();

// Set the "CreateNoteHyperlinks" property to "true" to turn all footnote/endnote symbols
// in the text act as links that, upon clicking, take us to their respective footnotes/endnotes.
// Set the "CreateNoteHyperlinks" property to "false" not to have footnote/endnote symbols link to anything.
options.createNoteHyperlinks = true;

doc.save(base.artifactsDir + "PdfSaveOptions.NoteHyperlinks.pdf", options);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

