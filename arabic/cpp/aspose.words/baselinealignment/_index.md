---
title: "Aspose::Words::BaselineAlignment تعداد"
linktitle: "BaselineAlignment"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::BaselineAlignment تعداد. يحدد الموضع الرأسي للخطوط على سطر في C++."
type: docs
weight: 80500
url: /ar/cpp/aspose.words/baselinealignment/
---
## BaselineAlignment enum


يحدد الموضع الرأسي للخطوط على السطر.

```cpp
enum class BaselineAlignment
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| أعلى | 0 | محاذاة على أعلى كل خط. |
| وسط | 1 | محاذاة نقاط المركز لكل خط. |
| خط الأساس | 2 | محاذاة إلى خط أساس الفقرة. |
| أسفل | 3 | محاذاة إلى أسفل كل خط. |
| تلقائي | 4 | يتم تعديل خط الأساس تلقائيًا. |


## أمثلة



يوضح كيفية ضبط الموضع الرأسي للخطوط على سطر.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat();
if (format->get_BaselineAlignment() == Aspose::Words::BaselineAlignment::Auto)
{
    format->set_BaselineAlignment(Aspose::Words::BaselineAlignment::Top);
}

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphBaselineAlignment.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
