---
title: Aspose::Words::Properties::DocumentProperty::ToDateTime method
linktitle: ToDateTime
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Properties::DocumentProperty::ToDateTime method. Returns the property value as DateTime in UTC in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words.properties/documentproperty/todatetime/
---
## DocumentProperty::ToDateTime method


Returns the property value as **DateTime** in UTC.

```cpp
System::DateTime Aspose::Words::Properties::DocumentProperty::ToDateTime()
```

## Remarks


Throws an exception if the property type is not [DateTime](../../propertytype/).

Microsoft Word stores only the date part (no time) for custom date properties.

## Examples



Shows how to create a custom document property which contains a date and time. 
```cpp
auto doc = MakeObject<Document>();

doc->get_CustomDocumentProperties()->Add(u"AuthorizationDate", System::DateTime::get_Now());

std::cout << "Document authorized on " << doc->get_CustomDocumentProperties()->idx_get(u"AuthorizationDate")->ToDateTime() << std::endl;
```


Shows various type conversion methods of custom document properties. 
```cpp
auto doc = MakeObject<Document>();
SharedPtr<CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

System::DateTime authDate = System::DateTime::get_Today();
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", String(u"John Doe"));
properties->Add(u"Authorized Date", authDate);
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

ASPOSE_ASSERT_EQ(true, properties->idx_get(u"Authorized")->ToBool());
ASSERT_EQ(u"John Doe", System::ObjectExt::ToString(properties->idx_get(u"Authorized By")));
ASSERT_EQ(authDate, properties->idx_get(u"Authorized Date")->ToDateTime());
ASSERT_EQ(1, properties->idx_get(u"Authorized Revision")->ToInt());
ASPOSE_ASSERT_EQ(123.45, properties->idx_get(u"Authorized Amount")->ToDouble());
```

## See Also

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
