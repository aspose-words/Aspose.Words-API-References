---
title: "Aspose::Words::Drawing::Charts::ChartSeries::get_HasDataLabels 方法"
linktitle: "get_HasDataLabels"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartSeries::get_HasDataLabels 方法。获取或设置一个标志，指示是否在 C++ 中为该系列显示数据标签。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.drawing.charts/chartseries/get_hasdatalabels/
---
## ChartSeries::get_HasDataLabels method


获取或设置指示是否为系列显示数据标签的标志。

```cpp
bool Aspose::Words::Drawing::Charts::ChartSeries::get_HasDataLabels() const
```


## 示例



展示如何为图表系列启用和配置数据标签。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 添加折线图，然后清除其演示数据系列，以获得一个干净的图表，
// 随后设置标题。
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Series()->Clear();
chart->get_Title()->set_Text(u"Monthly sales report");

// 插入一个自定义图表系列，以月份作为 X 轴的类别，
// 并为 Y 轴提供相应的十进制数值。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Revenue", System::MakeArray<System::String>({u"January", u"February", u"March"}), System::MakeArray<double>({25.611, 21.439, 33.750}));

// 启用数据标签，然后为显示在数据标签中的数值应用自定义数字格式。
// 此格式会将显示的十进制数值视为数百万美元。
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->get_NumberFormat()->set_FormatCode(u"\"US$\" #,##0.000\"M\"");
dataLabels->get_Font()->set_Size(12);

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelNumberFormat.docx");
```

## 另见

* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
