---
title: "طريقة Aspose::Words::Border::get_DistanceFromText"
linktitle: "get_DistanceFromText"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Border::get_DistanceFromText. تحصل أو تعيّن مسافة الحد من النص أو من حافة الصفحة بالنقاط في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words/border/get_distancefromtext/
---
## Border::get_DistanceFromText method


يحصل أو يضبط مسافة الحد من النص أو من حافة الصفحة بالنقاط.

```cpp
double Aspose::Words::Border::get_DistanceFromText()
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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
