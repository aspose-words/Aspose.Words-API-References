---
title: "Aspose::Words::Font::get_Outline طريقة"
linktitle: "get_Outline"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Font::get_Outline طريقة. صحيح إذا كان الخط مُنسقًا كحد خارجي في C++."
type: docs
weight: 31000
url: /ar/cpp/aspose.words/font/get_outline/
---
## Font::get_Outline method


صحيح إذا كان الخط منسقًا كحدود.

```cpp
bool Aspose::Words::Font::get_Outline()
```


## أمثلة



يظهر كيفية إنشاء مقطع نصي مُنسق كحد خارجي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// اضبط علامة Outline لتغيير لون تعبئة النص إلى الأبيض و
// اترك حدًا رفيعًا حول كل حرف بلون النص الأصلي.
builder->get_Font()->set_Outline(true);
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text has an outline.");

doc->Save(get_ArtifactsDir() + u"Font.Outline.docx");
```

## انظر أيضًا

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
