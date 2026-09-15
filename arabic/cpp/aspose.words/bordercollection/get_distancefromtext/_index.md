---
title: "Aspose::Words::BorderCollection::get_DistanceFromText method"
linktitle: "get_DistanceFromText"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::BorderCollection::get_DistanceFromText method. تحصّل أو تعيّن مسافة الحد من النص بالنقاط في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words/bordercollection/get_distancefromtext/
---
## BorderCollection::get_DistanceFromText method


يحصل أو يضبط المسافة بين الحد والنص بالنقاط.

```cpp
double Aspose::Words::BorderCollection::get_DistanceFromText()
```

## ملاحظات


تحصل على المسافة من النص للحد الأول.

يضبط المسافة من النص لجميع الحدود في المجموعة باستثناء الحدود القطرية.

ليس له أي تأثير وسيتم إعادة ضبطه تلقائيًا إلى الصفر لحدود خلايا الجدول.

## أمثلة



يظهر كيفية إنشاء حد صفحة متموج أخضر مع ظل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();

pageSetup->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DoubleWave);
pageSetup->get_Borders()->set_LineWidth(2);
pageSetup->get_Borders()->set_Color(System::Drawing::Color::get_Green());
pageSetup->get_Borders()->set_DistanceFromText(24);
pageSetup->get_Borders()->set_Shadow(true);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorders.docx");
```

## انظر أيضًا

* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
