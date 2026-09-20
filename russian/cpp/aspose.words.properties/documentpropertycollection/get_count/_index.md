---
title: "метод Aspose::Words::Properties::DocumentPropertyCollection::get_Count"
linktitle: "get_Count"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Properties::DocumentPropertyCollection::get_Count метод. Получает количество элементов в коллекции в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.properties/documentpropertycollection/get_count/
---
## DocumentPropertyCollection::get_Count method


Получает количество элементов в коллекции.

```cpp
int32_t Aspose::Words::Properties::DocumentPropertyCollection::get_Count()
```


## Примеры



Показывает, как работать с пользовательскими свойствами документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");

// Каждый документ содержит коллекцию пользовательских свойств, которые, как и встроенные свойства, представляют собой пары ключ‑значение.
// Документ имеет фиксированный список встроенных свойств. Пользователь создает все пользовательские свойства.
ASSERT_EQ(u"Value of custom document property", System::ObjectExt::ToString(doc->get_CustomDocumentProperties()->idx_get(u"CustomProperty")));

doc->get_CustomDocumentProperties()->Add(u"CustomProperty2", System::String(u"Value of custom document property #2"));

std::cout << "Custom Properties:" << std::endl;
for (auto&& customDocumentProperty : System::IterateOver(doc->get_CustomDocumentProperties()))
{
    std::cout << customDocumentProperty->get_Name() << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", customDocumentProperty->get_Type()) << std::endl;
    std::cout << System::String::Format(u"\tValue:\t\"{0}\"", customDocumentProperty->get_Value()) << std::endl;
}
```

## См. также

* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
