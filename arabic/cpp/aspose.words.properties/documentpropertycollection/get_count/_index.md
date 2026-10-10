---
title: "Aspose::Words::Properties::DocumentPropertyCollection::get_Count طريقة"
linktitle: "get_Count"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Properties::DocumentPropertyCollection::get_Count method. يحصل على عدد العناصر في المجموعة في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.properties/documentpropertycollection/get_count/
---
## DocumentPropertyCollection::get_Count method


يحصل على عدد العناصر في المجموعة.

```cpp
int32_t Aspose::Words::Properties::DocumentPropertyCollection::get_Count()
```


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

* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
