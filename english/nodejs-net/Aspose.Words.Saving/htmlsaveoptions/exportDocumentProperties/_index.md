---
title: HtmlSaveOptions.exportDocumentProperties property
linktitle: exportDocumentProperties property
articleTitle: exportDocumentProperties property
second_title: Aspose.Words for NodeJs
description: "HtmlSaveOptions.exportDocumentProperties property. Specifies whether to export built-in and custom document properties to HTML, MHTML or EPUB"
type: docs
weight: 120
url: /nodejs-net/Aspose.Words.Saving/htmlsaveoptions/exportDocumentProperties/
---

## HtmlSaveOptions.exportDocumentProperties property

Specifies whether to export built-in and custom document properties to HTML, MHTML or EPUB.
Default value is ``False``.



```js
get exportDocumentProperties(): boolean
```

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

