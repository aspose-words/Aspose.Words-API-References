---
title: DocumentSplitCriteria
second_title: Aspose.Words for C++ API Reference
description: Specifies how the document is split into parts when saving to Html, Epub or Azw3 format.
type: docs
weight: 664
url: /cpp/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enum


Specifies how the document is split into parts when saving to [Html](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/) or [Azw3](../../aspose.words/saveformat/) format.

```cpp
enum class DocumentSplitCriteria
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 | The document is not split. |
| PageBreak | 1 | The document is split into parts at explicit page breaks. A page break can be specified by a [PageBreak](../../aspose.words/controlchar/pagebreak/) character, a section break specifying start of new section on a new page, or a paragraph that has its [PageBreakBefore](../../aspose.words/paragraphformat/get_pagebreakbefore/) property set to **true**. |
| ColumnBreak | 2 | The document is split into parts at column breaks. A column break can be specified by a [ColumnBreak](../../aspose.words/controlchar/columnbreak/) character or a section break specifying start of new section in a new column. |
| SectionBreak | 4 | The document is split into parts at a section break of any type. |
| HeadingParagraph | 8 | The document is split into parts at a paragraph formatted using a heading style **Heading 1**, **Heading 2** etc. Use together with [DocumentSplitHeadingLevel](../htmlsaveoptions/get_documentsplitheadinglevel/) to specify the heading levels (from 1 to the specified level) at which to split. |

## Remarks


[DocumentSplitCriteria](./) is a set of flags which can be combined. For instance you can split the document at page breaks and heading paragraphs in the same export operation.

Different criteria can partially overlap. For instance, **Heading 1** style is frequently given [PageBreakBefore](../../aspose.words/paragraphformat/get_pagebreakbefore/) property so it falls under two criteria: [PageBreak](./) and [HeadingParagraph](./). Some section breaks can cause page breaks and so on. In typical cases specifying only one flag is the most practical option.

## Examples



Shows how to use a specific encoding when saving a document to .epub. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

// Use a SaveOptions object to specify the encoding for a document that we will save.
auto saveOptions = MakeObject<HtmlSaveOptions>();
saveOptions->set_SaveFormat(SaveFormat::Epub);
saveOptions->set_Encoding(System::Text::Encoding::get_UTF8());

// By default, an output .epub document will have all its contents in one HTML part.
// A split criterion allows us to segment the document into several HTML parts.
// We will set the criteria to split the document into heading paragraphs.
// This is useful for readers who cannot read HTML files more significant than a specific size.
saveOptions->set_DocumentSplitCriteria(DocumentSplitCriteria::HeadingParagraph);

// Specify that we want to export document properties.
saveOptions->set_ExportDocumentProperties(true);

doc->Save(ArtifactsDir + u"HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words](../../)
