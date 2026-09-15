---
title: "Aspose::Words::NumSpacing enum"
linktitle: "NumSpacing"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::NumSpacing enum. يحدد القيم الممكنة التي يمكن عرض تباعد الأرقام فيها في C++."
type: docs
weight: 103500
url: /ar/cpp/aspose.words/numspacing/
---
## NumSpacing enum


يحدد القيم الممكنة التي يمكن عرض تباعد الأرقام بها.

```cpp
enum class NumSpacing
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| افتراضي | 0 | يحدد أن الأرقام تُعرض بالشكل الافتراضي للخط. |
| Proportional | 1 | يحدد أن أشكال الأرقام المصممة كمتباعدة نسبياً تُعرض إذا كان الخط يدعم ذلك. |
| Tabular | 2 | يحدد أن أشكال الأرقام المصممة على شكل جدولي تُعرض إذا كان الخط يدعمها. |


## أمثلة



يظهر كيفية تعيين نوع تباعد الرقم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// هذا التأثير مدعوم فقط في الإصدارات الأحدث من MS Word.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2019);

builder->Write(u"1 ");
builder->Write(u"This is an example");

System::SharedPtr<Aspose::Words::Run> run = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0);
if (run->get_Font()->get_NumberSpacing() == Aspose::Words::NumSpacing::Default)
{
    run->get_Font()->set_NumberSpacing(Aspose::Words::NumSpacing::Proportional);
}

doc->Save(get_ArtifactsDir() + u"Fonts.NumberSpacing.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
