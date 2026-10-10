---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator 方法"
linktitle: "get_Separator"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator 方法。获取或设置用于整个系列数据标签的字符串分隔符。默认是逗号，但对于仅显示类别名称和百分比的饼图，则应使用换行符（在 C++ 中）。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_separator/
---
## ChartDataLabelCollection::get_Separator method


获取或设置整个系列数据标签使用的字符串分隔符。默认是逗号，除非是仅显示类别名称和百分比的饼图，此时应使用换行符。

```cpp
System::String Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator()
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


展示如何使用饼图的数据标签。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, 500, 300)->get_Chart();

// 清除图表的演示数据系列，以便从空白图表开始。
chart->get_Series()->Clear();

// 插入一个自定义图表系列，为每个扇区提供类别名称及其频率表。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel"}), System::MakeArray<double>({2.7, 3.2, 0.8}));

// 启用数据标签，以显示每个扇区的百分比和频率，并修改其外观。
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowLeaderLines(true);
dataLabels->set_ShowLegendKey(true);
dataLabels->set_ShowPercentage(true);
dataLabels->set_ShowValue(true);
dataLabels->set_Separator(u"; ");

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelsPieChart.docx");
```

## 另见

* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
