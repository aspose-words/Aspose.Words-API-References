---
title: "طريقة Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay"
linktitle: "get_Overlay"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay. تحدد ما إذا كان يُسمح لعناصر المخطط الأخرى بتغطية وسيلة الإيضاح. القيمة الافتراضية هي false في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.drawing.charts/chartlegend/get_overlay/
---
## ChartLegend::get_Overlay method


يحدد ما إذا كان يُسمح لعناصر المخطط الأخرى بالتداخل مع وسيلة الإيضاح. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay() const
```


## أمثلة



يظهر كيفية تعديل مظهر وسيلة إيضاح المخطط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(3, chart->get_Series()->get_Count());
ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

// انقل وسيلة إيضاح المخطط إلى الزاوية العليا اليمنى.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> legend = chart->get_Legend();
legend->set_Position(Aspose::Words::Drawing::Charts::LegendPosition::TopRight);

// امنح عناصر المخطط الأخرى، مثل الرسم البياني، مساحة أكبر بالسماح لها بالتداخل مع وسيلة الإيضاح.
legend->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartLegend.docx");
```

## انظر أيضًا

* Class [ChartLegend](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
