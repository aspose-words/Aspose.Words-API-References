---
title: "طريقة Aspose::Words::Style::get_Document"
linktitle: "get_Document"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Style::get_Document. تحصل على المستند المالِك في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words/style/get_document/
---
## Style::get_Document method


يحصل على المستند المالِك.

```cpp
System::SharedPtr<Aspose::Words::DocumentBase> Aspose::Words::Style::get_Document()
```


## أمثلة



يوضح كيفية الوصول إلى مجموعة أنماط المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(4, doc->get_Styles()->get_Count());

// عدّ وسرد جميع الأنماط التي يحتويها المستند الذي تم إنشاؤه باستخدام Aspose.Words بشكل افتراضي.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Style>>> stylesEnum = doc->get_Styles()->GetEnumerator();
    while (stylesEnum->MoveNext())
    {
        System::SharedPtr<Aspose::Words::Style> curStyle = stylesEnum->get_Current();
        std::cout << System::String::Format(u"Style name:\t\"{0}\", of type \"{1}\"", curStyle->get_Name(), curStyle->get_Type()) << std::endl;
        std::cout << System::String::Format(u"\tSubsequent style:\t{0}", curStyle->get_NextParagraphStyleName()) << std::endl;
        std::cout << System::String::Format(u"\tIs heading:\t\t\t{0}", curStyle->get_IsHeading()) << std::endl;
        std::cout << System::String::Format(u"\tIs QuickStyle:\t\t{0}", curStyle->get_IsQuickStyle()) << std::endl;

        ASPOSE_ASSERT_EQ(doc, curStyle->get_Document());
    }
}
```

## انظر أيضًا

* Class [DocumentBase](../../documentbase/)
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
