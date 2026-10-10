---
title: "Aspose::Words::Properties::DocumentProperty::get_Value طريقة"
linktitle: "get_Value"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Properties::DocumentProperty::get_Value. تحصّل على قيمة الخاصية أو تعينها في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.properties/documentproperty/get_value/
---
## DocumentProperty::get_Value method


يحصل أو يضبط قيمة الخاصية.

```cpp
System::SharedPtr<System::Object> Aspose::Words::Properties::DocumentProperty::get_Value()
```

## ملاحظات


لا يمكن أن تكون **null**.

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

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
