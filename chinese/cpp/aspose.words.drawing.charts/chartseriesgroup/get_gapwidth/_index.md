---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth 方法"
linktitle: "get_GapWidth"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth 方法。获取或设置图表元素之间间隙宽度的百分比，适用于 C++。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.drawing.charts/chartseriesgroup/get_gapwidth/
---
## ChartSeriesGroup::get_GapWidth method


获取或设置图表元素之间间隙宽度的百分比。

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth()
```

## 备注


仅适用于 bar、column、pie-of-bar、pie-of-pie、histogram、box&whisker、waterfall 和 funnel 类型的系列组。

可接受值的范围为 0 到 500（含）。对于基于条形/柱形的系列组，该属性表示条形簇之间的间距，以其宽度的百分比表示。对于 pie-of-pie 和 bar-of-pie 图表，这表示主次部分之间的间距。

## 示例



展示如何配置间隙宽度和重叠。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = shape->get_Chart()->get_SeriesGroups()->idx_get(0);

// 设置列间隙宽度和重叠。
seriesGroup->set_GapWidth(450);
seriesGroup->set_Overlap(-75);

doc->Save(get_ArtifactsDir() + u"Charts.ConfigureGapOverlap.docx");
```

## 另见

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
