---
title: "Класс Aspose::Words::Properties::CustomDocumentProperties"
linktitle: "CustomDocumentProperties"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Properties::CustomDocumentProperties. Коллекция пользовательских свойств документа. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.properties/customdocumentproperties/
---
## CustomDocumentProperties class


Коллекция пользовательских свойств документа. Чтобы узнать больше, посетите статью документации [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/).

```cpp
class CustomDocumentProperties : public Aspose::Words::Properties::DocumentPropertyCollection
```

## Методы

| Метод | Описание |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::String\&) | Создаёт новое пользовательское свойство документа типа данных [String](../propertytype/). |
| [Add](./add/)(const System::String\&, int32_t) | Создаёт новое пользовательское свойство документа типа данных [Number](../propertytype/). |
| [Add](./add/)(const System::String\&, System::DateTime) | Создаёт новое пользовательское свойство документа типа данных [DateTime](../propertytype/). |
| [Add](./add/)(const System::String\&, bool) | Создаёт новое пользовательское свойство документа типа данных [Boolean](../propertytype/). |
| [Add](./add/)(const System::String\&, double) | Создаёт новое пользовательское свойство документа типа данных [Double](../propertytype/). |
| [AddLinkToContent](./addlinktocontent/)(const System::String\&, const System::String\&) | Создает новое пользовательское свойство документа, связанное с содержимым. |
| [Clear](../documentpropertycollection/clear/)() | Удаляет все свойства из коллекции. |
| [Contains](../documentpropertycollection/contains/)(const System::String\&) | Возвращает **true**, если в коллекции существует свойство с указанным именем. |
| [get_Count](../documentpropertycollection/get_count/)() | Получает количество элементов в коллекции. |
| [GetEnumerator](../documentpropertycollection/getenumerator/)() override | Возвращает объект‑перечислитель, который можно использовать для перебора всех элементов в коллекции. |
| [GetType](./gettype/)() const override |  |
| virtual [idx_get](../documentpropertycollection/idx_get/)(System::String) | Возвращает объект [DocumentProperty](../documentproperty/) по имени свойства. |
| [idx_get](../documentpropertycollection/idx_get/)(int32_t) | Возвращает объект [DocumentProperty](../documentproperty/) по индексу. |
| [IndexOf](../documentpropertycollection/indexof/)(const System::String\&) | Получает индекс свойства по имени. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../documentpropertycollection/remove/)(const System::String\&) | Удаляет из коллекции свойство с указанным именем. |
| [RemoveAt](../documentpropertycollection/removeat/)(int32_t) | Удаляет свойство по указанному индексу. |
| static [Type](./type/)() |  |
## Примечания


Каждый объект [DocumentProperty](../documentproperty/) представляет пользовательское свойство контейнерного документа.

Имена свойств не чувствительны к регистру.

Свойства в коллекции сортируются в алфавитном порядке по имени.

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

* Class [DocumentPropertyCollection](../documentpropertycollection/)
* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
