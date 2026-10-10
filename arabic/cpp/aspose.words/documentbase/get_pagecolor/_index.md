---
title: "طريقة Aspose::Words::DocumentBase::get_PageColor"
linktitle: "get_PageColor"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBase::get_PageColor. تحصل على لون الصفحة للمستند أو تعينه. هذه الخاصية هي نسخة أبسط من BackgroundShape في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words/documentbase/get_pagecolor/
---
## DocumentBase::get_PageColor method


تحصل على لون الصفحة للمستند أو تعينه. هذه الخاصية هي نسخة أبسط من [BackgroundShape](../get_backgroundshape/).

```cpp
System::Drawing::Color Aspose::Words::DocumentBase::get_PageColor()
```

## ملاحظات


توفر هذه الخاصية طريقة بسيطة لتحديد لون صفحة صلب للمستند. ضبط هذه الخاصية ينشئ ويعين [BackgroundShape](../get_backgroundshape/) مناسب.

إذا لم يتم تعيين لون الصفحة (مثلاً لا يوجد شكل خلفية في المستند) تُعيد **Empty**.

## أمثلة



يوضح كيفية تعيين لون الخلفية لجميع صفحات المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->set_PageColor(System::Drawing::Color::get_LightGray());

doc->Save(get_ArtifactsDir() + u"DocumentBase.SetPageColor.docx");
```

## انظر أيضًا

* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
