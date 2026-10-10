---
title: "Aspose::Words::BorderCollection::get_Color method"
linktitle: "get_Color"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::BorderCollection::get_Color method. يحصل على أو يضبط لون الحد في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words/bordercollection/get_color/
---
## BorderCollection::get_Color method


يحصل أو يضبط لون الحد.

```cpp
System::Drawing::Color Aspose::Words::BorderCollection::get_Color()
```

## ملاحظات


يعيد لون الحد الأول في المجموعة.

يضبط لون جميع الحدود في المجموعة باستثناء الحدود القطرية.

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
