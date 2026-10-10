---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLegendKey 方法"
linktitle: "get_ShowLegendKey"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLegendKey 方法。允许指定是否在整个系列的数据标签中显示图例键。默认值在 C++ 中为 false。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_showlegendkey/
---
## ChartDataLabelCollection::get_ShowLegendKey method


允许指定是否在整个系列的数据标签中显示图例键。默认值为 **false**。

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLegendKey()
```


## 示例



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
