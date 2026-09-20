---
title: "Aspose::Words::Properties::DocumentProperty класс"
linktitle: "DocumentProperty"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Properties::DocumentProperty класс. Представляет пользовательское или встроенное свойство документа. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.properties/documentproperty/
---
## DocumentProperty class


Представляет пользовательское или встроенное свойство документа. Чтобы узнать больше, посетите статью документации [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/).

```cpp
class DocumentProperty : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_IsLinkToContent](./get_islinktocontent/)() | Показывает, связано ли это свойство с содержимым или нет. |
| [get_LinkSource](./get_linksource/)() const | Получает источник связанного пользовательского свойства документа. |
| [get_Name](./get_name/)() const | Возвращает имя свойства. |
| [get_Type](./get_type/)() const | Получает тип данных свойства. |
| [get_Value](./get_value/)() | Получает или задает значение свойства. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Value](./set_value/)(const System::SharedPtr\<System::Object\>\&) | Сеттер для [Aspose::Words::Properties::DocumentProperty::get_Value](./get_value/). |
| [ToBool](./tobool/)() | Возвращает значение свойства как bool. |
| [ToByteArray](./tobytearray/)() | Возвращает значение свойства как массив байтов. |
| [ToDateTime](./todatetime/)() | Возвращает значение свойства как **DateTime** в UTC. |
| [ToDouble](./todouble/)() | Возвращает значение свойства как double. |
| [ToInt](./toint/)() | Возвращает значение свойства как integer. |
| [ToString](./tostring/)() const override | Возвращает значение свойства как строку, отформатированную в соответствии с текущей локалью. |
| static [Type](./type/)() |  |

## Примеры



Показывает, как работать со встроенными свойствами документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");

// Объект "Document" содержит часть своей метаданных в своих членах.
std::cout << System::String::Format(u"Document filename:\n\t \"{0}\"", doc->get_OriginalFileName()) << std::endl;

// Документ также сохраняет метаданные во встроенных свойствах.
// Каждое встроенное свойство является членом объекта "BuiltInDocumentProperties" документа.
std::cout << "Built-in Properties:" << std::endl;
for (auto&& docProperty : System::IterateOver(doc->get_BuiltInDocumentProperties()))
{
    std::cout << docProperty->get_Name() << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", docProperty->get_Type()) << std::endl;

    // Некоторые свойства могут хранить несколько значений.
    if (System::ObjectExt::Is<System::Collections::Generic::ICollection<System::SharedPtr<System::Object>>>(docProperty->get_Value()))
    {
        for (auto&& value : System::IterateOver(System::AsCast<System::Collections::Generic::ICollection<System::SharedPtr<System::Object>>>(docProperty->get_Value())))
        {
            std::cout << System::String::Format(u"\tValue:\t\"{0}\"", value) << std::endl;
        }
    }
    else
    {
        std::cout << System::String::Format(u"\tValue:\t\"{0}\"", docProperty->get_Value()) << std::endl;
    }
}
```

## См. также

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
