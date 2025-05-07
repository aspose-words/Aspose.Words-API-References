---
title: HtmlSaveOptions.saveFormat property
linktitle: saveFormat property
articleTitle: saveFormat property
second_title: Aspose.Words for Node.js
description: "HtmlSaveOptions.saveFormat property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 460
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/saveFormat/
---

## HtmlSaveOptions.saveFormat property

Specifies the format in which the document will be saved if this save options object is used.
Can be [SaveFormat.Html](../../../aspose.words/saveformat/#Html), [SaveFormat.Mhtml](../../../aspose.words/saveformat/#Mhtml), [SaveFormat.Epub](../../../aspose.words/saveformat/#Epub),
[SaveFormat.Azw3](../../../aspose.words/saveformat/#Azw3) or [SaveFormat.Mobi](../../../aspose.words/saveformat/#Mobi).



```js
get saveFormat(): Aspose.Words.SaveFormat
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

