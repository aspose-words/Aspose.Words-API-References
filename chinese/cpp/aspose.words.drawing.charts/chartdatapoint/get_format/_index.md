---
title: "Aspose::Words::Drawing::Charts::ChartDataPoint::get_Format 方法"
linktitle: "get_Format"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartDataPoint::get_Format 方法。提供对 C++ 中此数据点的填充和线条格式的访问。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.drawing.charts/chartdatapoint/get_format/
---
## ChartDataPoint::get_Format method


提供对该数据点的填充和线条格式的访问。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartFormat> Aspose::Words::Drawing::Charts::ChartDataPoint::get_Format()
```


## 示例



展示如何为柱状图的各类别设置单独的格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// 删除默认生成的系列。
chart->get_Series()->Clear();

// 添加新系列。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Series 1", System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"}), System::MakeArray<double>({1, 2, 3, 4}));

// 设置柱形格式。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPointCollection> dataPoints = series->get_DataPoints();
dataPoints->idx_get(0)->get_Format()->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::Denim);
dataPoints->idx_get(1)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Red());
dataPoints->idx_get(2)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Yellow());
dataPoints->idx_get(3)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Blue());

doc->Save(get_ArtifactsDir() + u"Charts.DataPointsFormatting.docx");
```

## 另见

* Class [ChartFormat](../../chartformat/)
* Class [ChartDataPoint](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
