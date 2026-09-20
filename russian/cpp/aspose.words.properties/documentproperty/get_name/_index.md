---
title: "Aspose::Words::Properties::DocumentProperty::get_Name метод"
linktitle: "get_Name"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Properties::DocumentProperty::get_Name метод. Возвращает имя свойства в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.properties/documentproperty/get_name/
---
## DocumentProperty::get_Name method


Возвращает имя свойства.

```cpp
System::String Aspose::Words::Properties::DocumentProperty::get_Name() const
```

## Примечания


Не может быть **null** и не может быть пустой строкой.

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
