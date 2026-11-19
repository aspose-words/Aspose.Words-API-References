---
title: Aspose::Words::Properties::DocumentProperty::ToBool method
linktitle: ToBool
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Properties::DocumentProperty::ToBool method. Returns the property value as bool in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words.properties/documentproperty/tobool/
---
## DocumentProperty::ToBool method


Returns the property value as bool.

```cpp
bool Aspose::Words::Properties::DocumentProperty::ToBool()
```

## Remarks


Throws an exception if the property type is not [Boolean](../../propertytype/).
## Examples


Shows various type conversion methods of custom document properties.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

System::DateTime authDate = System::DateTime::get_Today();
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", authDate);
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

ASPOSE_ASSERT_EQ(properties->idx_get(u"Authorized")->ToBool(), true);
ASSERT_EQ(System::ObjectExt::ToString(properties->idx_get(u"Authorized By")), u"John Doe");
ASSERT_EQ(properties->idx_get(u"Authorized Date")->ToDateTime(), authDate);
ASSERT_EQ(properties->idx_get(u"Authorized Revision")->ToInt(), 1);
ASPOSE_ASSERT_EQ(properties->idx_get(u"Authorized Amount")->ToDouble(), 123.45);
```
## See Also

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
