---
title: "Aspose::Words::Drawing::Charts::ChartSeries::get_XValues 方法"
linktitle: "get_XValues"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartSeries::get_XValues 方法。获取此图表系列在 C++ 中的 X 值集合。"
type: docs
weight: 12334
url: /zh/cpp/aspose.words.drawing.charts/chartseries/get_xvalues/
---
## ChartSeries::get_XValues method


获取此图表系列的 X 值集合。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValueCollection> Aspose::Words::Drawing::Charts::ChartSeries::get_XValues()
```


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

* Class [ChartXValueCollection](../../chartxvaluecollection/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
