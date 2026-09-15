---
title: "طريقة Aspose::Words::Document::get_BuiltInDocumentProperties"
linktitle: "get_BuiltInDocumentProperties"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::get_BuiltInDocumentProperties. تُرجع مجموعة تمثل جميع خصائص المستند المدمجة في المستند في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words/document/get_builtindocumentproperties/
---
## Document::get_BuiltInDocumentProperties method


يعيد مجموعة تمثل جميع خصائص المستند المدمجة في المستند.

```cpp
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> Aspose::Words::Document::get_BuiltInDocumentProperties() const
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

* Class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
