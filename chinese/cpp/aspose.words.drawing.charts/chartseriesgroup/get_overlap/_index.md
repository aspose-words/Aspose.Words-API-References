---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap 方法"
linktitle: "get_Overlap"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap 方法. 获取或设置系列条形或柱形的重叠百分比（C++）。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.drawing.charts/chartseriesgroup/get_overlap/
---
## ChartSeriesGroup::get_Overlap method


获取或设置系列条形或柱形的重叠百分比。

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap()
```

## 备注


适用于所有条形和柱形类型的系列组。

可接受值的范围为 -100 到 100（含）。值为 0 表示条形/柱形之间没有间距。如果值为 -100，条形/柱形之间的距离等于它们的宽度。值为 100 表示条形/柱形完全重叠。

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
