---
title: "Класс Aspose::Words::Markup::CustomPart"
linktitle: "CustomPart"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Markup::CustomPart class. Представляет пользовательскую (произвольную) часть, которая не определена стандартом ISO/IEC 29500. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.markup/custompart/
---
## CustomPart class


Представляет пользовательскую (произвольную) часть, не определённую стандартом ISO/IEC 29500. Чтобы узнать больше, посетите статью документации [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomPart : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [Clone](./clone/)() | Создаёт «достаточно глубокую» копию объекта. Не дублирует байты значения [Data](./get_data/). |
| [CustomPart](./custompart/)() |  |
| [get_ContentType](./get_contenttype/)() const | Указывает тип содержимого этой пользовательской части. |
| [get_Data](./get_data/)() const | Содержит данные этой пользовательской части. |
| [get_IsExternal](./get_isexternal/)() const | False, если эта пользовательская часть хранится внутри пакета OOXML. True, если эта пользовательская часть является внешней целью. |
| [get_Name](./get_name/)() const | Получает или задает абсолютное имя этой части внутри пакета OOXML или целевой URL. |
| [get_RelationshipType](./get_relationshiptype/)() const | Получает или задает тип отношения от родительской части к этой пользовательской части. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ContentType](./set_contenttype/)(const System::String\&) | Сеттер для [Aspose::Words::Markup::CustomPart::get_ContentType](./get_contenttype/). |
| [set_Data](./set_data/)(const System::ArrayPtr\<uint8_t\>\&) | Сеттер для [Aspose::Words::Markup::CustomPart::get_Data](./get_data/). |
| [set_IsExternal](./set_isexternal/)(bool) | Сеттер для [Aspose::Words::Markup::CustomPart::get_IsExternal](./get_isexternal/). |
| [set_Name](./set_name/)(const System::String\&) | Сеттер для [Aspose::Words::Markup::CustomPart::get_Name](./get_name/). |
| [set_RelationshipType](./set_relationshiptype/)(const System::String\&) | Сеттер для [Aspose::Words::Markup::CustomPart::get_RelationshipType](./get_relationshiptype/). |
| static [Type](./type/)() |  |
## Примечания


Этот класс представляет часть OOXML, являющуюся целью "неизвестного отношения". Все отношения, не определённые в ISO/IEC 29500, считаются "неизвестными отношениями". Неизвестные отношения допускаются в документе Office Open XML при условии, что они соответствуют рекомендациям по разметке отношений.

Microsoft Word сохраняет пользовательские части во время циклов открытия/сохранения. Дополнительную информацию можно найти здесь [http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx](http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx)

Aspose.Words также проходит пользовательские части через процесс чтения/записи и, кроме того, позволяет программно получать доступ к таким частям через объекты [CustomPart](./) и [CustomPartCollection](../custompartcollection/).

Не путайте пользовательские части с данными Custom XML. Используйте [CustomXmlPart](../customxmlpart/), если вам нужно получить доступ к данным Custom XML.

## Примеры



Показывает, как получить доступ к коллекции произвольных пользовательских частей документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom parts OOXML package.docx");

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

// Клонируйте вторую часть, затем добавьте клон в коллекцию.
System::SharedPtr<Aspose::Words::Markup::CustomPart> clonedPart = doc->get_PackageCustomParts()->idx_get(1)->Clone();
doc->get_PackageCustomParts()->Add(clonedPart);

ASSERT_EQ(3, doc->get_PackageCustomParts()->get_Count());

// Переберите коллекцию и выведите каждую часть.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomPart>>> enumerator = doc->get_PackageCustomParts()->GetEnumerator();
    int32_t index = 0;
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Part index {0}:", index) << std::endl;
        std::cout << System::String::Format(u"\tName:\t\t\t\t{0}", enumerator->get_Current()->get_Name()) << std::endl;
        std::cout << System::String::Format(u"\tContent type:\t\t{0}", enumerator->get_Current()->get_ContentType()) << std::endl;
        std::cout << System::String::Format(u"\tRelationship type:\t{0}", enumerator->get_Current()->get_RelationshipType()) << std::endl;
        std::cout << (enumerator->get_Current()->get_IsExternal() ? u"\tSourced from outside the document" : System::String::Format(u"\tStored within the document, length: {0} bytes", enumerator->get_Current()->get_Data()->get_Length())) << std::endl;
        index++;
    }
}

// Мы можем удалять элементы из этой коллекции по отдельности или сразу все.
doc->get_PackageCustomParts()->RemoveAt(2);

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

doc->get_PackageCustomParts()->Clear();

ASSERT_EQ(0, doc->get_PackageCustomParts()->get_Count());
```

## См. также

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
