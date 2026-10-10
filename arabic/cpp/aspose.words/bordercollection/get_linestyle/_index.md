---
title: "طريقة Aspose::Words::BorderCollection::get_LineStyle"
linktitle: "get_LineStyle"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::BorderCollection::get_LineStyle. يحصل على أو يضبط نمط الحدود في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words/bordercollection/get_linestyle/
---
## BorderCollection::get_LineStyle method


يحصل أو يضبط نمط الحد.

```cpp
Aspose::Words::LineStyle Aspose::Words::BorderCollection::get_LineStyle()
```

## ملاحظات


يعيد نمط الحد الأول في المجموعة.

يضبط نمط جميع الحدود في المجموعة باستثناء الحدود القطرية.

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

* Enum [LineStyle](../../linestyle/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
