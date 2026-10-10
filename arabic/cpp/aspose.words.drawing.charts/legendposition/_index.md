---
title: "تعداد Aspose::Words::Drawing::Charts::LegendPosition"
linktitle: "LegendPosition"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "تعداد Aspose::Words::Drawing::Charts::LegendPosition. يحدد المواقع الممكنة لوسيلة إيضاح المخطط في C++."
type: docs
weight: 29000
url: /ar/cpp/aspose.words.drawing.charts/legendposition/
---
## LegendPosition enum


يحدد المواقع الممكنة لوسيلة إيضاح المخطط.

```cpp
enum class LegendPosition
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | 0 | لن يتم عرض وسيلة إيضاح للمخطط. |
| أسفل | 1 | يحدد أن يتم رسم وسيلة الإيضاح في أسفل المخطط. |
| يسار | 2 | يحدد أن يتم رسم وسيلة الإيضاح على يسار المخطط. |
| يمين | 3 | يحدد أن يتم رسم وسيلة الإيضاح على يمين المخطط. |
| أعلى | 4 | يحدد أن يتم رسم وسيلة الإيضاح في أعلى المخطط. |
| أعلى اليمين | 5 | يحدد أن يتم رسم وسيلة الإيضاح في أعلى يمين المخطط. |


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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
