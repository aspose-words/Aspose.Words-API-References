---
title: "Aspose::Words::PageBorderDistanceFrom enum"
linktitle: "PageBorderDistanceFrom"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::PageBorderDistanceFrom enum. يحدد موضع حد الصفحة بالنسبة لهامش الصفحة في C++."
type: docs
weight: 107000
url: /ar/cpp/aspose.words/pageborderdistancefrom/
---
## PageBorderDistanceFrom enum


يحدد موضع حد الصفحة بالنسبة لهامش الصفحة.

```cpp
enum class PageBorderDistanceFrom
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Text | 0 | [الحد](../border/) يتم قياس الموضع من هامش الصفحة. |
| PageEdge | 1 | [الحد](../border/) يتم قياس الموضع من حافة الصفحة. |


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
