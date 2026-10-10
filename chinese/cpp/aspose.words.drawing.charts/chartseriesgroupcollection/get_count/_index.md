---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::get_Count method"
linktitle: "get_Count"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::get_Count 方法。 在 C++ 中返回此集合中系列组的数量。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.drawing.charts/chartseriesgroupcollection/get_count/
---
## ChartSeriesGroupCollection::get_Count method


返回此集合中系列组的数量。

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::get_Count()
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
