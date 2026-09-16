---
title: "Aspose::Words::Drawing::Charts::ChartYValueCollection::get_FormatCode 方法"
linktitle: "get_FormatCode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartYValueCollection::get_FormatCode 方法。获取或设置应用于 Y 值的格式代码（C++）。"
type: docs
weight: 2500
url: /zh/cpp/aspose.words.drawing.charts/chartyvaluecollection/get_formatcode/
---
## ChartYValueCollection::get_FormatCode method


获取或设置应用于 Y 值的格式代码。

```cpp
System::String Aspose::Words::Drawing::Charts::ChartYValueCollection::get_FormatCode()
```

## 备注


数字格式用于更改图表中数值的显示方式。以下是数字格式示例：

数字 - "#,##0.00"

货币 - "\"\$\\"#,##0.00"

时间 - "[$-x-systime]h:mm:ss AM/PM"

日期 - "d/mm/yyyy"

百分比 - "0.00%"

分数 - "# ?/?"

科学计数 - "0.00E+00"

会计 - "_-\"\$\\"* #,##0.00_-;-\"\$\\"* #,##0.00_-;_-\"\$\\"* \"-\\"??_-;_-@_-"

自定义颜色 - "[Red]-#,##0.0"

## 示例



展示如何使用图表数据的格式代码。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入气泡图。
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// 删除默认生成的系列。
chart->get_Series()->Clear();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Series1", System::MakeArray<double>({1, 1.9, 2.45, 3}), System::MakeArray<double>({1, -0.9, 1.82, 0}), System::MakeArray<double>({2, 1.1, 2.95, 2}));

// 显示数据标签。
series->set_HasDataLabels(true);
series->get_DataLabels()->set_ShowCategoryName(true);
series->get_DataLabels()->set_ShowValue(true);
series->get_DataLabels()->set_ShowBubbleSize(true);

// 设置数据格式代码。
series->get_XValues()->set_FormatCode(u"#,##0.0#");
series->get_YValues()->set_FormatCode(u"#,##0.0#;[Red]\\-#,##0.0#");
series->get_BubbleSizes()->set_FormatCode(u"#,##0.0#");

doc->Save(get_ArtifactsDir() + u"Charts.FormatCode.docx");
```

## 另见

* Class [ChartYValueCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
