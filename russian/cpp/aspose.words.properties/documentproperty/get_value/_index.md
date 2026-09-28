---
title: "Aspose::Words::Properties::DocumentProperty::get_Value метод"
linktitle: "get_Value"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Properties::DocumentProperty::get_Value метод. Получает или задает значение свойства в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.properties/documentproperty/get_value/
---
## DocumentProperty::get_Value method


Получает или задает значение свойства.

```cpp
System::SharedPtr<System::Object> Aspose::Words::Properties::DocumentProperty::get_Value()
```

## Примечания


Не может быть **null**.

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

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
