---
title: "طريقة Aspose::Words::Document::get_CustomDocumentProperties"
linktitle: "get_CustomDocumentProperties"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::get_CustomDocumentProperties. تُرجع مجموعة تمثل جميع خصائص المستند المخصصة للمستند في C++."
type: docs
weight: 18000
url: /ar/cpp/aspose.words/document/get_customdocumentproperties/
---
## Document::get_CustomDocumentProperties method


يعيد مجموعة تمثل جميع خصائص المستند المخصصة للمستند.

```cpp
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> Aspose::Words::Document::get_CustomDocumentProperties()
```


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

* Class [CustomDocumentProperties](../../../aspose.words.properties/customdocumentproperties/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
