---
title: "Aspose::Words::Drawing::Charts::Chart::get_SeriesGroups 方法"
linktitle: "get_SeriesGroups"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::Chart::get_SeriesGroups 方法。提供对该图表系列组集合的访问（C++）。"
type: docs
weight: 6500
url: /zh/cpp/aspose.words.drawing.charts/chart/get_seriesgroups/
---
## Chart::get_SeriesGroups method


提供对本图表系列组集合的访问。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection> Aspose::Words::Drawing::Charts::Chart::get_SeriesGroups()
```


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

* Class [ChartSeriesGroupCollection](../../chartseriesgroupcollection/)
* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
