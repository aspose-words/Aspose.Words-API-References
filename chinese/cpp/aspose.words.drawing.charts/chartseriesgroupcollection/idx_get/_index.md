---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::idx_get method"
linktitle: "idx_get"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::idx_get 方法。 在 C++ 中返回指定索引处的 ChartSeriesGroup。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words.drawing.charts/chartseriesgroupcollection/idx_get/
---
## ChartSeriesGroupCollection::idx_get method


返回位于指定索引的 [ChartSeriesGroup](../../chartseriesgroup/)。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::idx_get(int32_t index)
```


## 示例



展示如何移除次要坐标轴。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Combo chart.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection> seriesGroups = chart->get_SeriesGroups();

// 查找次要坐标轴并从集合中移除。
for (int32_t i = 0; i < seriesGroups->get_Count(); i++)
{
    if (seriesGroups->idx_get(i)->get_AxisGroup() == Aspose::Words::Drawing::Charts::AxisGroup::Secondary)
    {
        seriesGroups->RemoveAt(i);
    }
}
```

## 另见

* Class [ChartSeriesGroup](../../chartseriesgroup/)
* Class [ChartSeriesGroupCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
