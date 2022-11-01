---
title: get_SaveFormat
second_title: Aspose.Words for C++ API Reference
description: Specifies the format in which the document will be saved if this save options object is used.
type: docs
weight: 144
url: /cpp/aspose.words.saving/saveoptions/get_saveformat/
---
## SaveOptions.get_SaveFormat method


Specifies the format in which the document will be saved if this save options object is used.

```cpp
virtual Aspose::Words::SaveFormat Aspose::Words::Saving::SaveOptions::get_SaveFormat()=0
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

