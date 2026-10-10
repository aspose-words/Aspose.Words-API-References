---
title: "فئة Aspose::Words::Properties::CustomDocumentProperties"
linktitle: "CustomDocumentProperties"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Properties::CustomDocumentProperties. مجموعة من خصائص المستند المخصصة. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.properties/customdocumentproperties/
---
## CustomDocumentProperties class


مجموعة من خصائص المستند المخصصة. لمعرفة المزيد، زر مقالة الوثائق [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/).

```cpp
class CustomDocumentProperties : public Aspose::Words::Properties::DocumentPropertyCollection
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::String\&) | ينشئ خاصية مستند مخصصة جديدة من نوع البيانات [String](../propertytype/). |
| [Add](./add/)(const System::String\&, int32_t) | ينشئ خاصية مستند مخصصة جديدة من نوع البيانات [Number](../propertytype/). |
| [Add](./add/)(const System::String\&, System::DateTime) | ينشئ خاصية مستند مخصصة جديدة من نوع البيانات [DateTime](../propertytype/). |
| [Add](./add/)(const System::String\&, bool) | ينشئ خاصية مستند مخصصة جديدة من نوع البيانات [Boolean](../propertytype/). |
| [Add](./add/)(const System::String\&, double) | ينشئ خاصية مستند مخصصة جديدة من نوع البيانات [Double](../propertytype/). |
| [AddLinkToContent](./addlinktocontent/)(const System::String\&, const System::String\&) | ينشئ خاصية مستند مخصصة مرتبطة بالمحتوى جديدة. |
| [Clear](../documentpropertycollection/clear/)() | يزيل جميع الخصائص من المجموعة. |
| [Contains](../documentpropertycollection/contains/)(const System::String\&) | يرجع **true** إذا كانت خاصية بالاسم المحدد موجودة في المجموعة. |
| [get_Count](../documentpropertycollection/get_count/)() | يحصل على عدد العناصر في المجموعة. |
| [GetEnumerator](../documentpropertycollection/getenumerator/)() override | يرجع كائن عداد يمكن استخدامه للتنقل عبر جميع العناصر في المجموعة. |
| [GetType](./gettype/)() const override |  |
| virtual [idx_get](../documentpropertycollection/idx_get/)(System::String) | يرجع كائن [DocumentProperty](../documentproperty/) بناءً على اسم الخاصية. |
| [idx_get](../documentpropertycollection/idx_get/)(int32_t) | يرجع كائن [DocumentProperty](../documentproperty/) بناءً على الفهرس. |
| [IndexOf](../documentpropertycollection/indexof/)(const System::String\&) | يحصل على فهرس الخاصية بالاسم. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../documentpropertycollection/remove/)(const System::String\&) | يزيل خاصية بالاسم المحدد من المجموعة. |
| [RemoveAt](../documentpropertycollection/removeat/)(int32_t) | يزيل خاصية في الفهرس المحدد. |
| static [Type](./type/)() |  |
## ملاحظات


كل كائن [DocumentProperty](../documentproperty/) يمثل خاصية مخصصة لوثيقة الحاوية.

أسماء الخصائص غير حساسة لحالة الأحرف.

الخصائص في المجموعة مرتبة أبجديًا حسب الاسم.

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

* Class [DocumentPropertyCollection](../documentpropertycollection/)
* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
