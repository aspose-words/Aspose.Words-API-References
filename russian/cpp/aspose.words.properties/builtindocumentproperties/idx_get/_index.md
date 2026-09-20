---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::idx_get метод"
linktitle: "idx_get"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::idx_get метод. Возвращает объект DocumentProperty по имени свойства в C++."
type: docs
weight: 35000
url: /ru/cpp/aspose.words.properties/builtindocumentproperties/idx_get/
---
## BuiltInDocumentProperties::idx_get method


Возвращает объект [DocumentProperty](../../documentproperty/) по имени свойства.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::BuiltInDocumentProperties::idx_get(System::String name) override
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| name | System::String | Имя свойства без учета регистра для получения. |
## Примечания


Строковые имена свойств соответствуют именам типизированных свойств, доступных из [BuiltInDocumentProperties](../).

Если вы запрашиваете свойство, отсутствующее в документе, но имя свойства распознаётся как допустимое встроенное имя, создаётся новый [DocumentProperty](../../documentproperty/), добавляется в коллекцию и возвращается. Новому свойству присваивается значение по умолчанию (пустая строка, ноль, **false** или DateTime.MinValue в зависимости от типа встроенного свойства).

Если вы запрашиваете свойство, отсутствующее в документе, и имя не распознаётся как встроенное, возвращается **null**.

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
* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
