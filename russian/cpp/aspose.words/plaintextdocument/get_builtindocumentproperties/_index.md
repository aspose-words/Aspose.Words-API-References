---
title: "Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties метод"
linktitle: "get_BuiltInDocumentProperties"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties метод. Получает BuiltInDocumentProperties документа в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/plaintextdocument/get_builtindocumentproperties/
---
## PlainTextDocument::get_BuiltInDocumentProperties method


Получает [BuiltInDocumentProperties](./) документа.

```cpp
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties() const
```


## Примеры



Показывает, как загрузить содержимое документа Microsoft Word в виде простого текста и затем получить доступ к встроенным свойствам исходного документа.
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

## См. также

* Class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
