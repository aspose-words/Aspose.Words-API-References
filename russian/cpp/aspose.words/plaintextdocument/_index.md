---
title: "класс Aspose::Words::PlainTextDocument"
linktitle: "PlainTextDocument"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::PlainTextDocument. Позволяет извлекать текстовое представление содержимого документа''. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 50000
url: /ru/cpp/aspose.words/plaintextdocument/
---
## PlainTextDocument class


Позволяет извлекать текстовое представление содержимого документа. Чтобы узнать больше, посетите статью документации [Working with Text Document](https://docs.aspose.com/words/cpp/working-with-text-document/).

```cpp
class PlainTextDocument : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_BuiltInDocumentProperties](./get_builtindocumentproperties/)() const | Получает [BuiltInDocumentProperties](./get_builtindocumentproperties/) документа. |
| [get_CustomDocumentProperties](./get_customdocumentproperties/)() const | Получает [CustomDocumentProperties](./get_customdocumentproperties/) документа. |
| [get_Text](./get_text/)() const | Получает текстовое содержимое документа, объединённое в одну строку. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PlainTextDocument](./plaintextdocument/)(const System::String\&) | Создаёт текстовый документ из файла. Автоматически определяет формат файла. |
| [PlainTextDocument](./plaintextdocument/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Создаёт текстовый документ из файла. Позволяет указать дополнительные параметры, такие как пароль шифрования. |
| [PlainTextDocument](./plaintextdocument/)(const System::SharedPtr\<System::IO::Stream\>\&) | Создаёт текстовый документ из потока. Автоматически определяет формат файла. |
| [PlainTextDocument](./plaintextdocument/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Создаёт текстовый документ из потока. Позволяет указать дополнительные параметры, такие как пароль шифрования. |
| [PlainTextDocument](./plaintextdocument/)(std::istream\&) |  |
| [PlainTextDocument](./plaintextdocument/)(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
