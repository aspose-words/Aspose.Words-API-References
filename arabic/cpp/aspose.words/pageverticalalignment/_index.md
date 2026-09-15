---
title: "تعداد Aspose::Words::PageVerticalAlignment"
linktitle: "PageVerticalAlignment"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "تعداد Aspose::Words::PageVerticalAlignment. يحدد محاذاة النص عموديًا على كل صفحة في C++."
type: docs
weight: 108000
url: /ar/cpp/aspose.words/pageverticalalignment/
---
## PageVerticalAlignment enum


يحدد ضبط النص عموديًا على كل صفحة.

```cpp
enum class PageVerticalAlignment
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| أسفل | 3 | النص محاذى في أسفل الصفحة. |
| وسط | 1 | النص محاذى في منتصف الصفحة. |
| محاذاة | 2 | يتم توزيع النص لملء الصفحة. |
| أعلى | 0 | يتم محاذاة النص إلى أعلى الصفحة. |


## أمثلة



يُظهر كيفية تطبيق وإرجاع إعدادات إعداد الصفحة إلى الأقسام في مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// عدّل خصائص إعداد الصفحة للقسم الحالي للمنشئ وأضف نصًا.
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_VerticalAlignment(Aspose::Words::PageVerticalAlignment::Center);
builder->Writeln(u"This is the first section, which landscape oriented with vertically centered text.");

// إذا بدأنا قسمًا جديدًا باستخدام منشئ المستند،
// سوف يرث خصائص إعداد الصفحة الحالية للمنشئ.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Orientation::Landscape, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Center, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

// يمكننا إرجاع خصائص إعداد الصفحة الخاصة به إلى القيم الافتراضية باستخدام طريقة "ClearFormatting".
builder->get_PageSetup()->ClearFormatting();

ASSERT_EQ(Aspose::Words::Orientation::Portrait, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Top, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

builder->Writeln(u"This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ClearFormatting.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
