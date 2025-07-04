---
title: Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria method
linktitle: get_DocumentSplitCriteria
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria method. Specifies how the document should be split when saving to Html, Epub or Azw3 format. Default is None for HTML and HeadingParagraph for EPUB and AZW3 in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.saving/htmlsaveoptions/get_documentsplitcriteria/
---
## HtmlSaveOptions::get_DocumentSplitCriteria method


Specifies how the document should be split when saving to [Html](../../../aspose.words/saveformat/), [Epub](../../../aspose.words/saveformat/) or [Azw3](../../../aspose.words/saveformat/) format. Default is [None](../../documentsplitcriteria/) for HTML and [HeadingParagraph](../../documentsplitcriteria/) for EPUB and AZW3.

```cpp
Aspose::Words::Saving::DocumentSplitCriteria Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria() const
```

## Remarks


Normally you would want a document saved to HTML as a single file. But in some cases it is preferable to split the output into several smaller HTML pages. When saving to HTML format these pages will be output to individual files or streams. When saving to EPUB format they will be incorporated into corresponding packages.

A document cannot be split when saving in the MHTML format.

## Examples



Shows how to use a specific encoding when saving a document to .epub. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Use a SaveOptions object to specify the encoding for a document that we will save.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Epub);
saveOptions->set_Encoding(System::Text::Encoding::get_UTF8());

// By default, an output .epub document will have all its contents in one HTML part.
// A split criterion allows us to segment the document into several HTML parts.
// We will set the criteria to split the document into heading paragraphs.
// This is useful for readers who cannot read HTML files more significant than a specific size.
saveOptions->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);

// Specify that we want to export document properties.
saveOptions->set_ExportDocumentProperties(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

## See Also

* Enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
