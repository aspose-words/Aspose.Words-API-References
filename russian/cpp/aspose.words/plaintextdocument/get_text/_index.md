---
title: "Метод Aspose::Words::PlainTextDocument::get_Text"
linktitle: "get_Text"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::PlainTextDocument::get_Text. Получает текстовое содержимое документа, объединённое в одну строку, в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words/plaintextdocument/get_text/
---
## PlainTextDocument::get_Text method


Получает текстовое содержимое документа, объединённое в одну строку.

```cpp
System::String Aspose::Words::PlainTextDocument::get_Text() const
```


## Примеры



Показывает, как загрузить содержимое документа Microsoft Word в виде обычного текста.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
```

## См. также

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
