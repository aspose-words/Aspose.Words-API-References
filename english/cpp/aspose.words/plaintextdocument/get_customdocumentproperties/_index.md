---
title: get_CustomDocumentProperties
second_title: Aspose.Words for C++ API Reference
description: Gets CustomDocumentProperties of the document.
type: docs
weight: 40
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
doc->get_CustomDocumentProperties()->Add(u"Location of writing", String(u"123 Main St, London, UK"));

doc->Save(ArtifactsDir + u"PlainTextDocument.CustomDocumentProperties.docx");

auto plaintext = MakeObject<PlainTextDocument>(ArtifactsDir + u"PlainTextDocument.CustomDocumentProperties.docx");

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
ASPOSE_ASSERT_EQ(u"123 Main St, London, UK", plaintext->get_CustomDocumentProperties()->idx_get(u"Location of writing")->get_Value());
```

## See Also

* Class [CustomDocumentProperties](../../../aspose.words.properties/customdocumentproperties/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
