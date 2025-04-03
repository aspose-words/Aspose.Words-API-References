---
title: DocumentSplitCriteria enumeration
linktitle: DocumentSplitCriteria enumeration
articleTitle: DocumentSplitCriteria enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.DocumentSplitCriteria enumeration. Specifies how the document is split into parts when saving to [SaveFormat.Html](../../aspose.words/saveformat/#Html), [SaveFormat.Epub](../../aspose.words/saveformat/#Epub) or [SaveFormat.Azw3](../../aspose.words/saveformat/#Azw3) format."
type: docs
weight: 130
url: /nodejs-net/aspose.words.saving/documentsplitcriteria/
---

## DocumentSplitCriteria enumeration

Specifies how the document is split into parts when saving to [SaveFormat.Html](../../aspose.words/saveformat/#Html),
[SaveFormat.Epub](../../aspose.words/saveformat/#Epub) or [SaveFormat.Azw3](../../aspose.words/saveformat/#Azw3) format.


[DocumentSplitCriteria](./) is a set of flags which can be combined. For instance you can split the document
at page breaks and heading paragraphs in the same export operation.

Different criteria can partially overlap. For instance, **Heading 1** style is frequently given 
[ParagraphFormat.pageBreakBefore](../../aspose.words/paragraphformat/pageBreakBefore/) property so it falls under two criteria: [DocumentSplitCriteria.PageBreak](./#PageBreak) and 
[DocumentSplitCriteria.HeadingParagraph](./#HeadingParagraph). Some section breaks can cause page breaks and so on. 
In typical cases specifying only one flag is the most practical option.




### Members

| Name | Description |
| --- | --- |
| None | The document is not split. |
| PageBreak | The document is split into parts at explicit page breaks. A page break can be specified by a Aspose.Words.ControlChar.PageBreak character,  a section break specifying start of new section on a new page, or a paragraph that has its [ParagraphFormat.pageBreakBefore](../../aspose.words/paragraphformat/pageBreakBefore/) property set to ``true``. |
| ColumnBreak | The document is split into parts at column breaks. A column break can be specified by a Aspose.Words.ControlChar.ColumnBreak character or a section break specifying start of new section in a new column. |
| SectionBreak | The document is split into parts at a section break of any type. |
| HeadingParagraph | The document is split into parts at a paragraph formatted using a heading style **Heading 1**, **Heading 2** etc.  Use together with [HtmlSaveOptions.documentSplitHeadingLevel](../htmlsaveoptions/documentSplitHeadingLevel/) to specify the heading levels  (from 1 to the specified level) at which to split. |

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

* module [Aspose.Words.Saving](../)
* property [HtmlSaveOptions.documentSplitCriteria](../htmlsaveoptions/documentSplitCriteria/)

