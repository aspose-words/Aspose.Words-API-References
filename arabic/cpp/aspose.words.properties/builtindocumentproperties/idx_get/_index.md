---
title: "طريقة Aspose::Words::Properties::BuiltInDocumentProperties::idx_get"
linktitle: "idx_get"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Properties::BuiltInDocumentProperties::idx_get. تُعيد كائن DocumentProperty بحسب اسم الخاصية في C++."
type: docs
weight: 35000
url: /ar/cpp/aspose.words.properties/builtindocumentproperties/idx_get/
---
## BuiltInDocumentProperties::idx_get method


تُعيد كائن [DocumentProperty](../../documentproperty/) بحسب اسم الخاصية.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::BuiltInDocumentProperties::idx_get(System::String name) override
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| name | System::String | اسم الخاصية غير حساس لحالة الأحرف المراد استرجاعه. |
## ملاحظات


أسماء السلاسل للخصائص تتطابق مع أسماء الخصائص المكتوبة المتاحة من [BuiltInDocumentProperties](../).

إذا طلبت خاصية غير موجودة في المستند، ولكن اسم الخاصية يُعترف به كاسم مدمج صالح، يتم إنشاء [DocumentProperty](../../documentproperty/) جديد، يُضاف إلى المجموعة ويُعاد. تُعطى الخاصية التي تم إنشاؤها حديثًا قيمة افتراضية (سلسلة فارغة، صفر، **false** أو DateTime.MinValue حسب نوع الخاصية المدمجة).

إذا طلبت خاصية غير موجودة في المستند ولم يُعترف بالاسم كاسم مدمج، يتم إرجاع **null**.

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

## انظر أيضًا

* Class [DocumentProperty](../../documentproperty/)
* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
