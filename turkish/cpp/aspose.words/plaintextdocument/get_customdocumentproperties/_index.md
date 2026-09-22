---
title: "Aspose::Words::PlainTextDocument::get_CustomDocumentProperties yöntemi"
linktitle: "get_CustomDocumentProperties"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PlainTextDocument::get_CustomDocumentProperties yöntemi. C++'ta belgenin CustomDocumentProperties değerini alır."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/plaintextdocument/get_customdocumentproperties/
---
## PlainTextDocument::get_CustomDocumentProperties method


Belgenin [CustomDocumentProperties](./) değerini alır.

```cpp
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> Aspose::Words::PlainTextDocument::get_CustomDocumentProperties() const
```


## Örnekler



Bir Microsoft Word belgesinin içeriğini düz metin olarak yüklemeyi ve ardından orijinal belgenin özel özelliklerine erişmeyi gösterir.
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

## Ayrıca Bakınız

* Class [CustomDocumentProperties](../../../aspose.words.properties/customdocumentproperties/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
