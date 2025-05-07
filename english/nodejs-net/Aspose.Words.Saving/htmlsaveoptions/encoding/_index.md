---
title: HtmlSaveOptions.encoding property
linktitle: encoding property
articleTitle: encoding property
second_title: Aspose.Words for Node.js
description: "HtmlSaveOptions.encoding property. Specifies the encoding to use when exporting to HTML, MHTML or EPUB"
type: docs
weight: 100
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/encoding/
---

## HtmlSaveOptions.encoding property

Specifies the encoding to use when exporting to HTML, MHTML or EPUB.
Default value is .


```js
get encoding(): string
```

### Remarks




### Examples

Shows how to use a specific encoding when saving a document to .epub.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

// Use a SaveOptions object to specify the encoding for a document that we will save.
let saveOptions = new aw.Saving.HtmlSaveOptions();
saveOptions.saveFormat = aw.SaveFormat.Epub;
saveOptions.encoding = "utf-8";

// By default, an output .epub document will have all its contents in one HTML part.
// A split criterion allows us to segment the document into several HTML parts.
// We will set the criteria to split the document into heading paragraphs.
// This is useful for readers who cannot read HTML files more significant than a specific size.
saveOptions.documentSplitCriteria = aw.Saving.DocumentSplitCriteria.HeadingParagraph;

// Specify that we want to export document properties.
saveOptions.exportDocumentProperties = true;

doc.save(base.artifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlSaveOptions](../)

