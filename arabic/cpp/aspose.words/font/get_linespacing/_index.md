---
title: "طريقة Aspose::Words::Font::get_LineSpacing"
linktitle: "get_LineSpacing"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Font::get_LineSpacing. تُرجع تباعد السطر لهذا الخط (بالنقاط) في C++."
type: docs
weight: 21000
url: /ar/cpp/aspose.words/font/get_linespacing/
---
## Font::get_LineSpacing method


يعيد تباعد الأسطر لهذا الخط (بالنقاط).

```cpp
double Aspose::Words::Font::get_LineSpacing()
```


## أمثلة



يوضح كيفية الحصول على تباعد سطر الخط، بالنقاط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// قم بتعيين خطوط مختلفة لـ DocumentBuilder وتحقق من تباعد السطر الخاص بها.
builder->get_Font()->set_Name(u"Calibri");
ASPOSE_ASSERT_EQ(14.6484375, builder->get_Font()->get_LineSpacing());

builder->get_Font()->set_Name(u"Times New Roman");
ASPOSE_ASSERT_EQ(13.798828125, builder->get_Font()->get_LineSpacing());
```

## انظر أيضًا

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
