---
title: "Aspose::Words::Style::get_AutomaticallyUpdate طريقة"
linktitle: "get_AutomaticallyUpdate"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Style::get_AutomaticallyUpdate طريقة. يحدد ما إذا كان هذا النمط يُعاد تعريفه تلقائيًا بناءً على القيمة المناسبة في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/style/get_automaticallyupdate/
---
## Style::get_AutomaticallyUpdate method


يحدد ما إذا كان هذا النمط يُعاد تعريفه تلقائيًا بناءً على القيمة المناسبة.

```cpp
bool Aspose::Words::Style::get_AutomaticallyUpdate() const
```

## ملاحظات


إذا تم تعيين قيمة الخاصية إلى true، يقوم MS Word تلقائيًا بإعادة تعريف النمط الحالي عندما يتم تغيير تنسيق الفقرة المناسب.

خاصية AutomaticallyUpdate تنطبق على أنماط الفقرات فقط.

القيمة الافتراضية هي **false**.

## أمثلة



يظهر كيفية إنشاء وتطبيق نمط مخصص.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
style->get_Font()->set_Name(u"Times New Roman");
style->get_Font()->set_Size(16);
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
// إعادة تعريف النمط تلقائيًا.
style->set_AutomaticallyUpdate(true);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// تطبيق أحد الأنماط من المستند على الفقرة التي ينشئها مُنشئ المستند.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Style> firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

ASPOSE_ASSERT_EQ(style, firstParagraphStyle);

// إزالة نمطنا المخصص من مجموعة أنماط المستند.
doc->get_Styles()->idx_get(u"MyStyle")->Remove();

firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

// أي نص كان يستخدم نمطًا مُزالًا يعود إلى التنسيق الافتراضي.
ASSERT_FALSE(doc->get_Styles()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Style>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Style> s)>>([](System::SharedPtr<Aspose::Words::Style> s) -> bool
{
    return s->get_Name() == u"MyStyle";
}))));
ASSERT_EQ(u"Times New Roman", firstParagraphStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(12.0, firstParagraphStyle->get_Font()->get_Size());
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), firstParagraphStyle->get_Font()->get_Color().ToArgb());
```

## انظر أيضًا

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
