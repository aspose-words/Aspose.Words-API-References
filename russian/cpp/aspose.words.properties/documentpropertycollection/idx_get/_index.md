---
title: "Aspose::Words::Properties::DocumentPropertyCollection::idx_get метод"
linktitle: "idx_get"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Properties::DocumentPropertyCollection::idx_get метод. Возвращает объект DocumentProperty по индексу в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.properties/documentpropertycollection/idx_get/
---
## DocumentPropertyCollection::idx_get(int32_t) method


Возвращает объект [DocumentProperty](../../documentproperty/) по индексу.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::DocumentPropertyCollection::idx_get(int32_t index)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int32_t | Индекс [DocumentProperty](../../documentproperty/) начиная с нуля для получения. |

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

* Class [DocumentProperty](../../documentproperty/)
* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentPropertyCollection::idx_get(System::String) method


Возвращает объект [DocumentProperty](../../documentproperty/) по имени свойства.

```cpp
virtual System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::DocumentPropertyCollection::idx_get(System::String name)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| name | System::String | Имя свойства без учета регистра для получения. |
## Примечания


Возвращает **null**, если свойство с указанным именем не найдено.

## Примеры



Показывает, как создать пользовательское свойство документа, содержащее дату и время.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_CustomDocumentProperties()->Add(u"AuthorizationDate", System::DateTime::get_Now());
System::DateTime authorizationDate = doc->get_CustomDocumentProperties()->idx_get(u"AuthorizationDate")->ToDateTime();
std::cout << System::String::Format(u"Document authorized on {0}", authorizationDate) << std::endl;
```

## См. также

* Class [DocumentProperty](../../documentproperty/)
* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
