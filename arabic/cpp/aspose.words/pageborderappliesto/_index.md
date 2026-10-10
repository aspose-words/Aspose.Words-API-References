---
title: "Aspose::Words::PageBorderAppliesTo enum"
linktitle: "PageBorderAppliesTo"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::PageBorderAppliesTo enum. يحدد الصفحات التي يتم طباعة حد الصفحة عليها في C++."
type: docs
weight: 106000
url: /ar/cpp/aspose.words/pageborderappliesto/
---
## PageBorderAppliesTo enum


يحدد الصفحات التي يُطبع عليها حد الصفحة.

```cpp
enum class PageBorderAppliesTo
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| AllPages | 0 | يظهر حد الصفحة على جميع صفحات القسم. |
| FirstPage | 1 | يظهر حد الصفحة على الصفحة الأولى من القسم فقط. |
| OtherPages | 2 | يظهر حد الصفحة على جميع الصفحات باستثناء الصفحة الأولى من القسم. |


## أمثلة



يظهر كيفية إنشاء حد على شكل شريط أزرق عريض في أعلى الصفحة الأولى.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_BorderAlwaysInFront(false);
pageSetup->set_BorderDistanceFrom(Aspose::Words::PageBorderDistanceFrom::PageEdge);
pageSetup->set_BorderAppliesTo(Aspose::Words::PageBorderAppliesTo::FirstPage);

System::SharedPtr<Aspose::Words::Border> border = pageSetup->get_Borders()->idx_get(Aspose::Words::BorderType::Top);
border->set_LineStyle(Aspose::Words::LineStyle::Single);
border->set_LineWidth(30);
border->set_Color(System::Drawing::Color::get_Blue());
border->set_DistanceFromText(0);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorderProperties.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
