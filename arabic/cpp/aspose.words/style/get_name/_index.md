---
title: "Aspose::Words::Style::get_Name طريقة"
linktitle: "get_Name"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Style::get_Name طريقة. يحصل على أو يحدد اسم النمط في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words/style/get_name/
---
## Style::get_Name method


يحصل أو يضبط اسم النمط.

```cpp
System::String Aspose::Words::Style::get_Name() const
```

## ملاحظات


لا يمكن أن تكون سلسلة فارغة.

إذا كان هناك نمط بالفعل بهذا الاسم في المجموعة، فسيتم استبدال هذا النمط به. جميع العقد المتأثرة ستشير إلى النمط الجديد.

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


يوضح كيفية استنساخ نمط المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// طريقة AddCopy تنشئ نسخة من النمط المحدد و
// يقوم تلقائيًا بإنشاء اسم جديد للنمط، مثل "Heading 1_0".
System::SharedPtr<Aspose::Words::Style> newStyle = doc->get_Styles()->AddCopy(doc->get_Styles()->idx_get(u"Heading 1"));

// استخدم خاصية "Name" الخاصة بالنمط لتغيير الاسم التعريفي للنمط.
newStyle->set_Name(u"My Heading 1");

// المستند الآن يحتوي على نمطين مظهرهما متطابق لكن بأسماء مختلفة.
// تغيير إعدادات أحد الأنماط لا يؤثر على الآخر.
newStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

ASSERT_EQ(u"My Heading 1", newStyle->get_Name());
ASSERT_EQ(u"Heading 1", doc->get_Styles()->idx_get(u"Heading 1")->get_Name());

ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Type(), newStyle->get_Type());
ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Name(), newStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Size(), newStyle->get_Font()->get_Size());
ASPOSE_ASSERT_NE(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Color(), newStyle->get_Font()->get_Color());
```

## انظر أيضًا

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
