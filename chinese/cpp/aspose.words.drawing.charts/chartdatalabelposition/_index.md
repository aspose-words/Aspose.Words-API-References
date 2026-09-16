---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelPosition 枚举"
linktitle: "ChartDataLabelPosition"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelPosition 枚举。指定在 C++ 中图表数据标签的位置。"
type: docs
weight: 27334
url: /zh/cpp/aspose.words.drawing.charts/chartdatalabelposition/
---
## ChartDataLabelPosition enum


指定图表数据标签的位置。

```cpp
enum class ChartDataLabelPosition
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 居中 | 0 | 指定数据标签应显示在数据标记的中心位置。 |
| 左 | 1 | 指定数据标签应显示在数据标记的左侧。 |
| 右 | 2 | 指定数据标签应显示在数据标记的右侧。 |
| Above | 3 | 指定数据标签应显示在数据标记的上方。 |
| Below | 4 | 指定数据标签应显示在数据标记的下方。 |
| InsideBase | 5 | 指定数据标签应显示在数据标记的基部内部。 |
| InsideEnd | 6 | 指定数据标签应显示在数据标记的末端内部。 |
| OutsideEnd | 7 | 指定数据标签应显示在数据标记的末端外部。 |
| BestFit | 8 | 指定数据标签应显示在最合适的位置。 |


## 示例



展示如何设置数据标签的位置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入柱形图。
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();

// 删除默认生成的系列。
seriesColl->Clear();

// 添加系列。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = seriesColl->Add(u"Series 1", System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"}), System::MakeArray<double>({4, 5, 6}));

// 显示数据标签并设置字体颜色。
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->get_Font()->set_Color(System::Drawing::Color::get_White());

// 设置数据标签位置。
dataLabels->set_Position(Aspose::Words::Drawing::Charts::ChartDataLabelPosition::InsideBase);
dataLabels->idx_get(0)->set_Position(Aspose::Words::Drawing::Charts::ChartDataLabelPosition::OutsideEnd);
dataLabels->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_DarkRed());

doc->Save(get_ArtifactsDir() + u"Charts.LabelPosition.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
