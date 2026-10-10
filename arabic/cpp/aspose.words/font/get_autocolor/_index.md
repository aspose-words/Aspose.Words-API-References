---
title: "طريقة Aspose::Words::Font::get_AutoColor"
linktitle: "get_AutoColor"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Font::get_AutoColor. تُرجع اللون المحسوب الحالي للنص (أسود أو أبيض) لاستخدامه في ''auto color''. إذا لم يكن اللون ''auto'' فإنها تُرجع Color في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/font/get_autocolor/
---
## Font::get_AutoColor method


تُرجع اللون المحسوب الحالي للنص (أسود أو أبيض) لاستخدامه في 'auto color'. إذا لم يكن اللون 'auto' فإنها تُرجع [Color](../get_color/).

```cpp
System::Drawing::Color Aspose::Words::Font::get_AutoColor()
```

## ملاحظات


عندما يكون للنص 'automatic color'، يتم حساب اللون الفعلي للنص تلقائيًا بحيث يكون مقروءًا مقابل لون الخلفية. عند تغيير لون الخلفية، سيتحول لون النص تلقائيًا إلى الأسود أو الأبيض في MS Word لتعزيز الوضوح.

## أمثلة



يظهر كيفية تحسين قابلية القراءة عن طريق اختيار لون النص تلقائيًا بناءً على سطوع الخلفية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إذا لم يحدد كائن Font في المقطع لون النص، فسيتم تلقائيًا
// اختيار إما الأسود أو الأبيض اعتمادًا على لون الخلفية.
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());

// اللون الافتراضي للنص هو الأسود. إذا كان لون الخلفية داكنًا، سيكون من الصعب رؤية النص الأسود.
// لحل هذه المشكلة، ستعرض خاصية AutoColor هذا النص باللون الأبيض.
builder->get_Font()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_DarkBlue());

builder->Writeln(u"The text color automatically chosen for this run is white.");

ASSERT_EQ(System::Drawing::Color::get_White().ToArgb(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_Font()->get_AutoColor().ToArgb());

// إذا غيرنا الخلفية إلى لون فاتح، سيكون الأسود أكثر
// لون نص مناسب أكثر من الأبيض بحيث سيعرض اللون التلقائي النص بالأسود.
builder->get_Font()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());

builder->Writeln(u"The text color automatically chosen for this run is black.");

ASSERT_EQ(System::Drawing::Color::get_Black().ToArgb(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_Runs()->idx_get(0)->get_Font()->get_AutoColor().ToArgb());

doc->Save(get_ArtifactsDir() + u"Font.SetFontAutoColor.docx");
```

## انظر أيضًا

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
