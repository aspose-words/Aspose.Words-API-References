---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::RemoveAt method"
linktitle: "RemoveAt"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::RemoveAt 方法。 在指定的索引处移除一个系列组。 所有子系列将在 C++ 中从图表中移除。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words.drawing.charts/chartseriesgroupcollection/removeat/
---
## ChartSeriesGroupCollection::RemoveAt method


移除位于指定索引的系列组。所有子系列将从图表中移除。

```cpp
void Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::RemoveAt(int32_t index)
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

* Class [ChartSeriesGroupCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
