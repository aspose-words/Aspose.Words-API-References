---
title: "Aspose::Words::Properties::DocumentPropertyCollection::idx_get طريقة"
linktitle: "idx_get"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Properties::DocumentPropertyCollection::idx_get طريقة. تُرجع كائن DocumentProperty حسب الفهرس في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.properties/documentpropertycollection/idx_get/
---
## DocumentPropertyCollection::idx_get(int32_t) method


تُرجع كائن [DocumentProperty](../../documentproperty/) حسب الفهرس.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::DocumentPropertyCollection::idx_get(int32_t index)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| index | int32_t | الفهرس الصفري للـ [DocumentProperty](../../documentproperty/) المراد استرجاعه. |

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
* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentPropertyCollection::idx_get(System::String) method


تُعيد كائن [DocumentProperty](../../documentproperty/) بحسب اسم الخاصية.

```cpp
virtual System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::DocumentPropertyCollection::idx_get(System::String name)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| name | System::String | اسم الخاصية غير حساس لحالة الأحرف المراد استرجاعه. |
## ملاحظات


تُرجع **null** إذا لم يتم العثور على خاصية بالاسم المحدد.

## أمثلة



يوضح كيفية إنشاء خاصية مستند مخصصة تحتوي على تاريخ ووقت.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_CustomDocumentProperties()->Add(u"AuthorizationDate", System::DateTime::get_Now());
System::DateTime authorizationDate = doc->get_CustomDocumentProperties()->idx_get(u"AuthorizationDate")->ToDateTime();
std::cout << System::String::Format(u"Document authorized on {0}", authorizationDate) << std::endl;
```

## انظر أيضًا

* Class [DocumentProperty](../../documentproperty/)
* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
