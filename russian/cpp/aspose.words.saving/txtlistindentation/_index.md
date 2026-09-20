---
title: "Класс Aspose::Words::Saving::TxtListIndentation"
linktitle: "TxtListIndentation"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Saving::TxtListIndentation. Указывает, как уровни списка отступаются при экспорте документа в формат Text. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 32000
url: /ru/cpp/aspose.words.saving/txtlistindentation/
---
## TxtListIndentation class


Указывает, как уровни списка отступаются при экспорте документа в формат [Text](../../aspose.words/saveformat/). Чтобы узнать больше, посетите статью документации [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class TxtListIndentation : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Character](./get_character/)() const | Получает или задает символ, используемый для отступа уровней списка. Значение по умолчанию — "\\0", что означает отсутствие отступа. |
| [get_Count](./get_count/)() const | Получает или задает количество [Character](./get_character/), используемое в качестве отступа для одного уровня списка. Значение по умолчанию — 0, что означает отсутствие отступа. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Character](./set_character/)(char16_t) | Сеттер для [Aspose::Words::Saving::TxtListIndentation::get_Character](./get_character/). |
| [set_Count](./set_count/)(int32_t) | Сеттер для [Aspose::Words::Saving::TxtListIndentation::get_Count](./get_count/). |
| [TxtListIndentation](./txtlistindentation/)() |  |
| static [Type](./type/)() |  |

## Примеры



Показывает, как настроить отступы списка при сохранении документа в простой текст.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте список с тремя уровнями отступа.
builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Item 1");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 2");
builder->get_ListFormat()->ListIndent();
builder->Write(u"Item 3");

// Создайте объект "TxtSaveOptions", который мы можем передать методу "Save" документа
// чтобы изменить способ сохранения документа в простой текст.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Установите свойство "Character", чтобы задать используемый символ
// для заполнения, имитирующего отступы списка в простом тексте.
txtSaveOptions->get_ListIndentation()->set_Character(u' ');

// Установите свойство "Count", чтобы указать количество раз
// для размещения символа заполнения на каждом уровне отступа списка.
txtSaveOptions->get_ListIndentation()->set_Count(3);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.TxtListIndentation.txt");
System::String newLine = System::Environment::get_NewLine();

ASSERT_EQ(System::String::Format(u"1. Item 1{0}", newLine) + System::String::Format(u"   a. Item 2{0}", newLine) + System::String::Format(u"      i. Item 3{0}", newLine), docText);
```

## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
