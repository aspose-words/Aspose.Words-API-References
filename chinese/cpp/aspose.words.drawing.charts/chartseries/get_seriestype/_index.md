---
title: "Aspose::Words::Drawing::Charts::ChartSeries::get_SeriesType 方法"
linktitle: "get_SeriesType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartSeries::get_SeriesType 方法。获取此图表系列的类型（在 C++ 中）。"
type: docs
weight: 11500
url: /zh/cpp/aspose.words.drawing.charts/chartseries/get_seriestype/
---
## ChartSeries::get_SeriesType method


获取此图表系列的类型。

```cpp
Aspose::Words::Drawing::Charts::ChartSeriesType Aspose::Words::Drawing::Charts::ChartSeries::get_SeriesType()
```


## 示例



展示如何删除特定的图表系列。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Reporting engine template - Chart series.docx");
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Chart();

// 删除所有柱形类型的系列。
for (int32_t i = chart->get_Series()->get_Count() - 1; i >= 0; i--)
{
    if (chart->get_Series()->idx_get(i)->get_SeriesType() == Aspose::Words::Drawing::Charts::ChartSeriesType::Column)
    {
        chart->get_Series()->RemoveAt(i);
    }
}

chart->get_Series()->Add(u"Aspose Series", System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"}), System::MakeArray<double>({5.6, 7.1, 2.9, 8.9}));

doc->Save(get_ArtifactsDir() + u"Charts.RemoveSpecificChartSeries.docx");
```

## 另见

* Enum [ChartSeriesType](../../chartseriestype/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
