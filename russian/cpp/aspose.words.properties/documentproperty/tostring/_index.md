---
title: "Aspose::Words::Properties::DocumentProperty::ToString метод"
linktitle: "ToString"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Properties::DocumentProperty::ToString метод. Возвращает значение свойства в виде строки, отформатированной в соответствии с текущей локалью в C++."
type: docs
weight: 15000
url: /ru/cpp/aspose.words.properties/documentproperty/tostring/
---
## DocumentProperty::ToString method


Возвращает значение свойства как строку, отформатированную в соответствии с текущей локалью.

```cpp
System::String Aspose::Words::Properties::DocumentProperty::ToString() const override
```

## Примечания


Преобразует логическое свойство в "Y" или "N". Преобразует свойство даты в короткую строку даты. Для всех остальных типов преобразует свойство с помощью Object.ToString().

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


Показывает различные методы преобразования типов пользовательских свойств документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

System::DateTime authDate = System::DateTime::get_Today();
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", authDate);
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

ASPOSE_ASSERT_EQ(true, properties->idx_get(u"Authorized")->ToBool());
ASSERT_EQ(u"John Doe", System::ObjectExt::ToString(properties->idx_get(u"Authorized By")));
ASSERT_EQ(authDate, properties->idx_get(u"Authorized Date")->ToDateTime());
ASSERT_EQ(1, properties->idx_get(u"Authorized Revision")->ToInt());
ASPOSE_ASSERT_EQ(123.45, properties->idx_get(u"Authorized Amount")->ToDouble());
```

## См. также

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
