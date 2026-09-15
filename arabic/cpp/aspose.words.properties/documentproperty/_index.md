---
title: "Aspose::Words::Properties::DocumentProperty فئة"
linktitle: "DocumentProperty"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Properties::DocumentProperty فئة. يمثل خاصية مستند مخصصة أو مدمجة. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.properties/documentproperty/
---
## DocumentProperty class


يمثل خاصية مستند مخصصة أو مضمنة. لمعرفة المزيد، زر مقالة الوثائق [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/).

```cpp
class DocumentProperty : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_IsLinkToContent](./get_islinktocontent/)() | يظهر ما إذا كانت هذه الخاصية مرتبطة بالمحتوى أم لا. |
| [get_LinkSource](./get_linksource/)() const | يحصل على مصدر خاصية المستند المخصصة المرتبطة. |
| [get_Name](./get_name/)() const | يعيد اسم الخاصية. |
| [get_Type](./get_type/)() const | يحصل على نوع البيانات للخاصية. |
| [get_Value](./get_value/)() | يحصل أو يضبط قيمة الخاصية. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Value](./set_value/)(const System::SharedPtr\<System::Object\>\&) | المُعيّن لـ [Aspose::Words::Properties::DocumentProperty::get_Value](./get_value/). |
| [ToBool](./tobool/)() | يعيد قيمة الخاصية كـ bool. |
| [ToByteArray](./tobytearray/)() | يعيد قيمة الخاصية كمصفوفة بايت. |
| [ToDateTime](./todatetime/)() | يعيد قيمة الخاصية كـ **DateTime** بتوقيت UTC. |
| [ToDouble](./todouble/)() | يعيد قيمة الخاصية كـ double. |
| [ToInt](./toint/)() | يعيد قيمة الخاصية كـ integer. |
| [ToString](./tostring/)() const override | يعيد قيمة الخاصية كسلسلة نصية مُنسقة وفقًا للغة الحالية. |
| static [Type](./type/)() |  |

## أمثلة



يظهر كيفية التعامل مع خصائص المستند المدمجة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");

// كائن "Document" يحتوي على بعض بياناته الوصفية في أعضائه.
std::cout << System::String::Format(u"Document filename:\n\t \"{0}\"", doc->get_OriginalFileName()) << std::endl;

// المستند أيضًا يخزن البيانات الوصفية في خصائصه المدمجة.
// كل خاصية مدمجة هي عضو في كائن المستند "BuiltInDocumentProperties".
std::cout << "Built-in Properties:" << std::endl;
for (auto&& docProperty : System::IterateOver(doc->get_BuiltInDocumentProperties()))
{
    std::cout << docProperty->get_Name() << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", docProperty->get_Type()) << std::endl;

    // بعض الخصائص قد تخزن قيمًا متعددة.
    if (System::ObjectExt::Is<System::Collections::Generic::ICollection<System::SharedPtr<System::Object>>>(docProperty->get_Value()))
    {
        for (auto&& value : System::IterateOver(System::AsCast<System::Collections::Generic::ICollection<System::SharedPtr<System::Object>>>(docProperty->get_Value())))
        {
            std::cout << System::String::Format(u"\tValue:\t\"{0}\"", value) << std::endl;
        }
    }
    else
    {
        std::cout << System::String::Format(u"\tValue:\t\"{0}\"", docProperty->get_Value()) << std::endl;
    }
}
```

## انظر أيضًا

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
