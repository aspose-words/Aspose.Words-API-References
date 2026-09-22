---
title: "طريقة Aspose::Words::Properties::DocumentProperty::ToBool"
linktitle: "ToBool"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Properties::DocumentProperty::ToBool. تُرجع قيمة الخاصية كقيمة منطقية (bool) في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words.properties/documentproperty/tobool/
---
## DocumentProperty::ToBool method


يعيد قيمة الخاصية كـ bool.

```cpp
bool Aspose::Words::Properties::DocumentProperty::ToBool()
```

## ملاحظات


يرمي استثناءً إذا لم يكن نوع الخاصية هو [Boolean](../../propertytype/).

## أمثلة



يعرض طرق تحويل الأنواع المختلفة للخصائص المخصصة للمستند.
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

## انظر أيضًا

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
