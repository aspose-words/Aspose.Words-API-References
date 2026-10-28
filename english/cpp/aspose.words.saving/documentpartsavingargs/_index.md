---
title: Aspose::Words::Saving::DocumentPartSavingArgs class
linktitle: DocumentPartSavingArgs
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::DocumentPartSavingArgs class. Provides data for the DocumentPartSaving() callback. To learn more, visit the Save a Document documentation article in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.saving/documentpartsavingargs/
---
## DocumentPartSavingArgs class


Provides data for the [DocumentPartSaving()](../idocumentpartsavingcallback/documentpartsaving/) callback. 
To learn more, visit the [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/) documentation article.

```cpp
class DocumentPartSavingArgs : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo \&) const override |  |
| static [Type](./type/)() |  |
| [get_Document](./get_document/)() const | Gets the document object that is being saved. |
| [get_DocumentPartFileName](./get_documentpartfilename/)() const | Gets or sets the file name (without path) where the document part will be saved to. |
| [get_DocumentPartStream](./get_documentpartstream/)() const | Allows to specify the stream where the document part will be saved to. |
| [get_KeepDocumentPartStreamOpen](./get_keepdocumentpartstreamopen/)() const | Specifies whether Aspose.Words should keep the stream open or close it after saving a document part. |
| [set_DocumentPartFileName](./set_documentpartfilename/)(const System::String \&) | Sets the file name (without path) where the document part will be saved to. |
| [set_DocumentPartStream](./set_documentpartstream/)(const System::SharedPtr\<System::IO::Stream\> \&) | Allows to specify the stream where the document part will be saved to. |
| [set_DocumentPartStream](./set_documentpartstream/)(std::basic_ostream\<CharType, Traits\> \&) | Allows to specify the stream where the document part will be saved to. |
| [set_KeepDocumentPartStreamOpen](./set_keepdocumentpartstreamopen/)(bool) | Specifies whether Aspose.Words should keep the stream open or close it after saving a document part. |
## Remarks


When Aspose.Words saves a document to HTML or related formats and [DocumentSplitCriteria](../htmlsaveoptions/get_documentsplitcriteria/) is specified, the document is split into parts and by default, each document part is saved into a separate file.

Class [DocumentPartSavingArgs](./) allows you to control how each document part will be saved. It allows to redefine how file names are generated or to completely circumvent saving of document parts into files by providing your own stream objects.

To save document parts into streams instead of files, use the [DocumentPartStream](./get_documentpartstream/) property.
## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
