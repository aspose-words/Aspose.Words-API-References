---
title: "Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden 方法"
linktitle: "get_Hidden"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden 方法。获取或设置一个标志，指示此轴在 C++ 中是否隐藏。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words.drawing.charts/chartaxis/get_hidden/
---
## ChartAxis::get_Hidden method


获取或设置一个标志，指示此轴是否隐藏。

```cpp
bool Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden()
```


## 示例



展示如何隐藏图表坐标轴。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// 清除图表的演示数据系列，以便从空白图表开始。
chart->get_Series()->Clear();

// 添加一个自定义系列，为 X 轴提供类别，并为 Y 轴提供相应的小数值。
chart->get_Series()->Add(u"AW Series 1", System::MakeArray<System::String>({u"Item 1", u"Item 2", u"Item 3", u"Item 4", u"Item 5"}), System::MakeArray<double>({1.2, 0.3, 2.1, 2.9, 4.2}));

// 隐藏图表坐标轴以简化图表的外观。
chart->get_AxisX()->set_Hidden(true);
chart->get_AxisY()->set_Hidden(true);

doc->Save(get_ArtifactsDir() + u"Charts.HideChartAxis.docx");
```

## 另见

* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
