---
title: "Aspose::Words::PageSetup::get_BorderDistanceFrom method"
linktitle: "get_BorderDistanceFrom"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::PageSetup::get_BorderDistanceFrom method. يحصل على أو يضبط قيمة تشير إلى ما إذا كان حد الصفحة المحدد يُقاس من حافة الصفحة أو من النص الذي يحيط به في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words/pagesetup/get_borderdistancefrom/
---
## PageSetup::get_BorderDistanceFrom method


يحصل أو يعيّن قيمة تشير إلى ما إذا كان حد الصفحة المحدد يُقاس من حافة الصفحة أو من النص الذي يحيط به.

```cpp
Aspose::Words::PageBorderDistanceFrom Aspose::Words::PageSetup::get_BorderDistanceFrom()
```


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

* Enum [PageBorderDistanceFrom](../../pageborderdistancefrom/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
