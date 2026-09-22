---
title: "Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties yöntemi"
linktitle: "get_BuiltInDocumentProperties"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties yöntemi. C++'ta belgenin BuiltInDocumentProperties değerini alır."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/plaintextdocument/get_builtindocumentproperties/
---
## PlainTextDocument::get_BuiltInDocumentProperties method


Belgenin [BuiltInDocumentProperties](./) değerini alır.

```cpp
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties() const
```


## Örnekler



Bir Microsoft Word belgesinin içeriğini düz metin olarak yüklemeyi ve ardından orijinal belgenin yerleşik özelliklerine erişmeyi gösterir.
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

## Ayrıca Bakınız

* Class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
