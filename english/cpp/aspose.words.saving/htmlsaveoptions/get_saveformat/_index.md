---
title: Aspose::Words::Saving::HtmlSaveOptions::get_SaveFormat method
linktitle: get_SaveFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::get_SaveFormat method. Specifies the format in which the document will be saved if this save options object is used. Can be Html, Mhtml, Epub, Azw3 or Mobi in C++.'
type: docs
weight: 45000
url: /cpp/aspose.words.saving/htmlsaveoptions/get_saveformat/
---
## HtmlSaveOptions::get_SaveFormat method


Specifies the format in which the document will be saved if this save options object is used. Can be [Html](../../../aspose.words/saveformat/), [Mhtml](../../../aspose.words/saveformat/), [Epub](../../../aspose.words/saveformat/), [Azw3](../../../aspose.words/saveformat/) or [Mobi](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::HtmlSaveOptions::get_SaveFormat() override
```


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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
