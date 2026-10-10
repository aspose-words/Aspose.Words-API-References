---
title: "Aspose::Words::Drawing::Charts::ChartSeries::get_Format 方法"
linktitle: "get_Format"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartSeries::get_Format 方法。提供对系列填充和线条格式的访问（在 C++ 中）。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.drawing.charts/chartseries/get_format/
---
## ChartSeries::get_Format method


提供对系列的填充和线条格式的访问。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartFormat> Aspose::Words::Drawing::Charts::ChartSeries::get_Format()
```


## 示例



展示如何设置系列颜色。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();

// 删除默认生成的系列。
seriesColl->Clear();

// 创建类别名称数组。
auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2"});

// 添加新系列。值数组和类别数组必须大小相同。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = seriesColl->Add(u"Series 1", categories, System::MakeArray<double>({1, 2}));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series2 = seriesColl->Add(u"Series 2", categories, System::MakeArray<double>({3, 4}));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series3 = seriesColl->Add(u"Series 3", categories, System::MakeArray<double>({5, 6}));

// 设置系列颜色。
series1->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Red());
series2->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Yellow());
series3->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Blue());

doc->Save(get_ArtifactsDir() + u"Charts.SeriesColor.docx");
```

## 另见

* Class [ChartFormat](../../chartformat/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
