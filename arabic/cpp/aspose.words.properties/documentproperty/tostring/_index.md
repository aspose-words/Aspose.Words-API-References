---
title: "Aspose::Words::Properties::DocumentProperty::ToString طريقة"
linktitle: "ToString"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Properties::DocumentProperty::ToString. تُرجع قيمة الخاصية كسلسلة مُنسّقة وفقًا للمنطقة الحالية في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words.properties/documentproperty/tostring/
---
## DocumentProperty::ToString method


يعيد قيمة الخاصية كسلسلة نصية مُنسقة وفقًا للغة الحالية.

```cpp
System::String Aspose::Words::Properties::DocumentProperty::ToString() const override
```

## ملاحظات


يحوّل خاصية منطقية إلى "Y" أو "N". يحوّل خاصية تاريخ إلى سلسلة تاريخ قصيرة. بالنسبة لجميع الأنواع الأخرى، يحوّل الخاصية باستخدام Object.ToString().

## أمثلة



يظهر كيفية العمل مع خصائص المستند المخصصة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");

// كل مستند يحتوي على مجموعة من الخصائص المخصصة، والتي، مثل الخصائص المدمجة، هي أزواج مفتاح-قيمة.
// المستند يحتوي على قائمة ثابتة من الخصائص المدمجة. المستخدم ينشئ جميع الخصائص المخصصة.
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
