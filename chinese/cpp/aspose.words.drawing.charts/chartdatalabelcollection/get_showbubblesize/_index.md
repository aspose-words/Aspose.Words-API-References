---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowBubbleSize 方法"
linktitle: "get_ShowBubbleSize"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowBubbleSize 方法。允许指定是否在整个系列的数据标签中显示气泡大小。仅适用于气泡图。默认值在 C++ 中为 false。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_showbubblesize/
---
## ChartDataLabelCollection::get_ShowBubbleSize method


允许指定是否在整个系列的数据标签中显示气泡大小。仅适用于气泡图。默认值为 **false**。

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowBubbleSize()
```


## 示例



展示如何使用气泡图的数据标签。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble, 500, 300)->get_Chart();

// 清除图表的演示数据系列，以便从空白图表开始。
chart->get_Series()->Clear();

// 添加一个自定义系列，包含每个气泡的 X/Y 坐标和直径。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<double>({2.9, 3.5, 1.1, 4.0, 4.0}), System::MakeArray<double>({1.9, 8.5, 2.1, 6.0, 1.5}), System::MakeArray<double>({9.0, 4.5, 2.5, 8.0, 5.0}));

// 启用数据标签，然后修改其外观。
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowBubbleSize(true);
dataLabels->set_ShowCategoryName(true);
dataLabels->set_ShowSeriesName(true);
dataLabels->set_Separator(u" & ");

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelsBubbleChart.docx");
```

## 另见

* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
