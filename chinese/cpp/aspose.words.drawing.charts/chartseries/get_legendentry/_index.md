---
title: "Aspose::Words::Drawing::Charts::ChartSeries::get_LegendEntry 方法"
linktitle: "get_LegendEntry"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartSeries::get_LegendEntry 方法。获取此图表系列的图例项，适用于 C++。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.drawing.charts/chartseries/get_legendentry/
---
## ChartSeries::get_LegendEntry method


获取此图表系列的图例项。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegendEntry> Aspose::Words::Drawing::Charts::ChartSeries::get_LegendEntry()
```


## 示例



展示如何使用图例字体。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Reporting engine template - Chart series.docx");
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Chart();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> chartLegend = chart->get_Legend();
// 设置所有图例条目的默认字体大小。
chartLegend->get_Font()->set_Size(14);
// 更改特定图例条目的字体。
chartLegend->get_LegendEntries()->idx_get(1)->get_Font()->set_Italic(true);
chartLegend->get_LegendEntries()->idx_get(1)->get_Font()->set_Size(12);
// 获取图表系列的图例条目。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegendEntry> legendEntry = chart->get_Series()->idx_get(0)->get_LegendEntry();

doc->Save(get_ArtifactsDir() + u"Charts.LegendFont.docx");
```

## 另见

* Class [ChartLegendEntry](../../chartlegendentry/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
