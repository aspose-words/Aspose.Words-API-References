---
title: "Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion 方法"
linktitle: "get_Explosion"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion 方法。指定数据点应从饼图中心移动的距离。可以为负，负值表示属性未设置且不应应用爆炸效果。仅适用于 C++ 中的饼图。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.drawing.charts/ichartdatapoint/get_explosion/
---
## IChartDataPoint::get_Explosion method


指定数据点应从饼图中心移动的距离。可以为负，负值表示未设置此属性且不应应用爆炸效果。仅适用于饼图。

```cpp
virtual int32_t Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion()=0
```


## 示例



展示如何将饼图的切片从中心移开。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, 500, 350);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Sales", chart->get_Series()->idx_get(0)->get_Name());

// 饼图的“切片”可以通过相应数据点的 Explosion 属性，以一定距离从中心移开。
// 向饼图的第一部分添加一个数据点，并将其从中心向外移动 10 个点。
// 如果不存在，Aspose.Words 会自动创建数据点。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPoint> dataPoint = chart->get_Series()->idx_get(0)->get_DataPoints()->idx_get(0);
dataPoint->set_Explosion(10);

// 将第二部分以更大的距离移开。
dataPoint = chart->get_Series()->idx_get(0)->get_DataPoints()->idx_get(1);
dataPoint->set_Explosion(40);

doc->Save(get_ArtifactsDir() + u"Charts.PieChartExplosion.docx");
```

## 另见

* Interface [IChartDataPoint](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
