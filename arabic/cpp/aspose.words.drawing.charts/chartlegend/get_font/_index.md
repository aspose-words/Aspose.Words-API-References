---
title: "طريقة Aspose::Words::Drawing::Charts::ChartLegend::get_Font"
linktitle: "get_Font"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Charts::ChartLegend::get_Font. توفر الوصول إلى تنسيق الخط الافتراضي لمدخلات وسيلة الإيضاح. لتجاوز تنسيق الخط لمدخل وسيلة إيضاح محدد، استخدم الخاصية theFont في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.drawing.charts/chartlegend/get_font/
---
## ChartLegend::get_Font method


توفر الوصول إلى تنسيق الخط الافتراضي لمدخلات وسيلة الإيضاح. لتجاوز تنسيق الخط لمدخل وسيلة إيضاح محدد، استخدم الخاصية [Font](../../chartlegendentry/get_font/).

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Drawing::Charts::ChartLegend::get_Font()
```


## أمثلة



يظهر كيفية العمل مع خط الأسطورة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Reporting engine template - Chart series.docx");
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Chart();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> chartLegend = chart->get_Legend();
// حدد حجم الخط الافتراضي لجميع إدخالات الأسطورة.
chartLegend->get_Font()->set_Size(14);
// غيّر الخط لإدخال أسطورة محدد.
chartLegend->get_LegendEntries()->idx_get(1)->get_Font()->set_Italic(true);
chartLegend->get_LegendEntries()->idx_get(1)->get_Font()->set_Size(12);
// احصل على إدخال الأسطورة لسلسلة المخطط.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegendEntry> legendEntry = chart->get_Series()->idx_get(0)->get_LegendEntry();

doc->Save(get_ArtifactsDir() + u"Charts.LegendFont.docx");
```

## انظر أيضًا

* Class [Font](../../../aspose.words/font/)
* Class [ChartLegend](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
