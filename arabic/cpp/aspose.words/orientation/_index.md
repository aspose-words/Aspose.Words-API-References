---
title: "Aspose::Words::Orientation enum"
linktitle: "Orientation"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Orientation enum. يحدد اتجاه الصفحة في C++."
type: docs
weight: 104000
url: /ar/cpp/aspose.words/orientation/
---
## Orientation enum


يحدد اتجاه الصفحة.

```cpp
enum class Orientation
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Portrait | 1 | اتجاه الصفحة Portrait (ضيق وطويل). |
| Landscape | 2 | اتجاه الصفحة Landscape (واسع وقصير). |


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
