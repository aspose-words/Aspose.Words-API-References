---
title: "Aspose::Words::Drawing::Charts::Chart::get_Axes 方法"
linktitle: "get_Axes"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::Chart::get_Axes 方法。获取此图表所有轴的集合（C++）。"
type: docs
weight: 1500
url: /zh/cpp/aspose.words.drawing.charts/chart/get_axes/
---
## Chart::get_Axes method


获取此图表的所有坐标轴集合。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisCollection> Aspose::Words::Drawing::Charts::Chart::get_Axes()
```


## 示例



展示如何使用轴集合。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// 隐藏主 Y 轴和次 Y 轴上的主网格线。
for (auto&& axis : System::IterateOver(chart->get_Axes()))
{
    if (axis->get_Type() == Aspose::Words::Drawing::Charts::ChartAxisType::Value)
    {
        axis->set_HasMajorGridlines(false);
    }
}

doc->Save(get_ArtifactsDir() + u"Charts.AxisCollection.docx");
```

## 另见

* Class [ChartAxisCollection](../../chartaxiscollection/)
* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
