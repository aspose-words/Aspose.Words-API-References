---
title: "Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode 方法"
linktitle: "get_FormatCode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode 方法。获取或设置在 C++ 中应用于数据标签的格式代码。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.drawing.charts/chartnumberformat/get_formatcode/
---
## ChartNumberFormat::get_FormatCode method


获取或设置应用于数据标签的格式代码。

```cpp
System::String Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode()
```

## 备注


数字格式用于更改数值在数据标签中的显示方式，并且可以以非常创意的方式使用。数字格式示例：

数字 - "#,##0.00"

货币 - "\"\$\\"#,##0.00"

时间 - "[$-x-systime]h:mm:ss AM/PM"

日期 - "d/mm/yyyy"

百分比 - "0.00%"

分数 - "# ?/?"

科学计数 - "0.00E+00"

文本 - "@"

会计 - "_-\"\$\\"* #,##0.00_-;-\"\$\\"* #,##0.00_-;_-\"\$\\"* \"-\\"??_-;_-@_-"

自定义颜色 - "[Red]-#,##0.0"

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


展示如何为图表值设置格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// 清除图表的演示数据系列，以便从空白图表开始。
chart->get_Series()->Clear();

// 向图表添加一个自定义系列，X 轴使用类别，
// 并为 Y 轴提供相应的大数值。
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel", u"GoogleDocs", u"Note"}), System::MakeArray<double>({1900000, 850000, 2100000, 600000, 1500000}));

// 设置 Y 轴刻度标签的数字格式，使其不使用逗号分组数字。
chart->get_AxisY()->get_NumberFormat()->set_FormatCode(u"#,##0");

// 此标志可以覆盖上述值，并从源单元格获取数字格式。
ASSERT_FALSE(chart->get_AxisY()->get_NumberFormat()->get_IsLinkedToSource());

doc->Save(get_ArtifactsDir() + u"Charts.SetNumberFormatToChartAxis.docx");
```

## 另见

* Class [ChartNumberFormat](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
