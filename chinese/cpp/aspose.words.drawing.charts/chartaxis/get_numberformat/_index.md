---
title: "Aspose::Words::Drawing::Charts::ChartAxis::get_NumberFormat 方法"
linktitle: "get_NumberFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartAxis::get_NumberFormat 方法。返回一个 ChartNumberFormat 对象，允许在 C++ 中为坐标轴定义数字格式。"
type: docs
weight: 20000
url: /zh/cpp/aspose.words.drawing.charts/chartaxis/get_numberformat/
---
## ChartAxis::get_NumberFormat method


返回一个 [ChartNumberFormat](../../chartnumberformat/) 对象，允许为坐标轴定义数字格式。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartNumberFormat> Aspose::Words::Drawing::Charts::ChartAxis::get_NumberFormat()
```


## 示例



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

* Class [ChartNumberFormat](../../chartnumberformat/)
* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
