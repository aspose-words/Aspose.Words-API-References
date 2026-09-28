---
title: "Aspose::Words::Properties::DocumentProperty::ToInt метод"
linktitle: "ToInt"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Properties::DocumentProperty::ToInt метод. Возвращает значение свойства как целое число в C++."
type: docs
weight: 14000
url: /ru/cpp/aspose.words.properties/documentproperty/toint/
---
## DocumentProperty::ToInt method


Возвращает значение свойства как integer.

```cpp
int32_t Aspose::Words::Properties::DocumentProperty::ToInt()
```


## Примеры



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
