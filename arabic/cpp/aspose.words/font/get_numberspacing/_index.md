---
title: "Aspose::Words::Font::get_NumberSpacing طريقة"
linktitle: "get_NumberSpacing"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Font::get_NumberSpacing طريقة. يحصل على أو يضبط نوع التباعد للرقم المعروض في C++."
type: docs
weight: 30500
url: /ar/cpp/aspose.words/font/get_numberspacing/
---
## Font::get_NumberSpacing method


الحصول أو تعيين نوع التباعد للرقم المعروض.

```cpp
Aspose::Words::NumSpacing Aspose::Words::Font::get_NumberSpacing()
```


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

* Enum [NumSpacing](../../numspacing/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
