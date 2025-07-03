---
title: Aspose::Words::PlainTextDocument::get_CustomDocumentProperties method
linktitle: get_CustomDocumentProperties
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::PlainTextDocument::get_CustomDocumentProperties method. Gets CustomDocumentProperties of the document in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words/plaintextdocument/get_customdocumentproperties/
---
## PlainTextDocument::get_CustomDocumentProperties method


Gets [CustomDocumentProperties](./) of the document.

```cpp
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> Aspose::Words::PlainTextDocument::get_CustomDocumentProperties() const
```


## Examples



Shows how to load the contents of a Microsoft Word document in plaintext and then access the original document's custom properties. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
doc->get_CustomDocumentProperties()->Add(u"Location of writing", System::String(u"123 Main St, London, UK"));

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.CustomDocumentProperties.docx");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.CustomDocumentProperties.docx");

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
ASPOSE_ASSERT_EQ(u"123 Main St, London, UK", plaintext->get_CustomDocumentProperties()->idx_get(u"Location of writing")->get_Value());
```

## See Also

* Class [CustomDocumentProperties](../../../aspose.words.properties/customdocumentproperties/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
