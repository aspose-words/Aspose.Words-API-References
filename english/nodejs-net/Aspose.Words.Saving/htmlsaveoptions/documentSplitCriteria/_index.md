---
title: HtmlSaveOptions.documentSplitCriteria property
linktitle: documentSplitCriteria property
articleTitle: documentSplitCriteria property
second_title: Aspose.Words for Node.js
description: "HtmlSaveOptions.documentSplitCriteria property. Specifies how the document should be split when saving to [SaveFormat.Html](../../../aspose.words/saveformat/#Html), [SaveFormat.Epub](../../../aspose.words/saveformat/#Epub) or [SaveFormat.Azw3](../../../aspose.words/saveformat/#Azw3) format"
type: docs
weight: 80
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/documentSplitCriteria/
---

## HtmlSaveOptions.documentSplitCriteria property

Specifies how the document should be split when saving to [SaveFormat.Html](../../../aspose.words/saveformat/#Html),
[SaveFormat.Epub](../../../aspose.words/saveformat/#Epub) or [SaveFormat.Azw3](../../../aspose.words/saveformat/#Azw3) format.
Default is [DocumentSplitCriteria.None](../../documentsplitcriteria/#None) for HTML and
[DocumentSplitCriteria.HeadingParagraph](../../documentsplitcriteria/#HeadingParagraph) for EPUB and AZW3.



```js
get documentSplitCriteria(): Aspose.Words.Saving.DocumentSplitCriteria
```

### Remarks

Normally you would want a document saved to HTML as a single file.
But in some cases it is preferable to split the output into several smaller HTML pages.
When saving to HTML format these pages will be output to individual files or streams.
When saving to EPUB format they will be incorporated into corresponding packages.

A document cannot be split when saving in the MHTML format.




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
* property [HtmlSaveOptions.documentSplitHeadingLevel](../documentSplitHeadingLevel/)
* property [HtmlSaveOptions.documentPartSavingCallback](../documentPartSavingCallback/)

