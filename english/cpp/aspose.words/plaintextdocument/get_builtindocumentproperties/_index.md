---
title: Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties method
linktitle: get_BuiltInDocumentProperties
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties method. Gets BuiltInDocumentProperties of the document in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words/plaintextdocument/get_builtindocumentproperties/
---
## PlainTextDocument::get_BuiltInDocumentProperties method


Gets [BuiltInDocumentProperties](./) of the document.

```cpp
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties() const
```


## Examples



Shows how to load the contents of a Microsoft Word document in plaintext and then access the original document's built-in properties. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.BuiltInProperties.docx");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.BuiltInProperties.docx");

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
ASSERT_EQ(u"John Doe", plaintext->get_BuiltInDocumentProperties()->get_Author());
```

## See Also

* Class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
