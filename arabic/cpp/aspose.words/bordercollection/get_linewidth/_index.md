---
title: "Aspose::Words::BorderCollection::get_LineWidth method"
linktitle: "get_LineWidth"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::BorderCollection::get_LineWidth method. يحصل على أو يضبط عرض الحد بالنقاط في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words/bordercollection/get_linewidth/
---
## BorderCollection::get_LineWidth method


يحصل أو يضبط عرض الحد بالنقاط.

```cpp
double Aspose::Words::BorderCollection::get_LineWidth()
```

## ملاحظات


يعيد عرض الحد الأول في المجموعة.

يضبط عرض جميع الحدود في المجموعة باستثناء الحدود القطرية.

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
