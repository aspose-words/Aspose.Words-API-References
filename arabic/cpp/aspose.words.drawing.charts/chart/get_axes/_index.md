---
title: "Aspose::Words::Drawing::Charts::Chart::get_Axes طريقة"
linktitle: "get_Axes"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::Chart::get_Axes طريقة. يحصل على مجموعة من جميع محاور هذا المخطط في C++."
type: docs
weight: 1500
url: /ar/cpp/aspose.words.drawing.charts/chart/get_axes/
---
## Chart::get_Axes method


يحصل على مجموعة جميع محاور هذا المخطط.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisCollection> Aspose::Words::Drawing::Charts::Chart::get_Axes()
```


## أمثلة



يعرض كيفية العمل مع مجموعة المحاور.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// إخفاء خطوط الشبكة الرئيسية على المحاور Y الأساسية والثانوية.
for (auto&& axis : System::IterateOver(chart->get_Axes()))
{
    if (axis->get_Type() == Aspose::Words::Drawing::Charts::ChartAxisType::Value)
    {
        axis->set_HasMajorGridlines(false);
    }
}

doc->Save(get_ArtifactsDir() + u"Charts.AxisCollection.docx");
```

## انظر أيضًا

* Class [ChartAxisCollection](../../chartaxiscollection/)
* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
