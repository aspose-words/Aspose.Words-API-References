---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_AxisGroup 方法"
linktitle: "get_AxisGroup"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_AxisGroup 方法. 获取或设置此系列组所属的坐标轴组（C++）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.drawing.charts/chartseriesgroup/get_axisgroup/
---
## ChartSeriesGroup::get_AxisGroup method


获取或设置此系列组所属的坐标轴组。

```cpp
Aspose::Words::Drawing::Charts::AxisGroup Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_AxisGroup()
```


## 示例



展示如何使用图表的次要坐标轴。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();

// 删除默认生成的系列。
series->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"});
series->Add(u"Series 1 of primary series group", categories, System::MakeArray<double>({2, 3, 4}));
series->Add(u"Series 2 of primary series group", categories, System::MakeArray<double>({5, 2, 3}));

// 创建一个额外的系列组，同样为折线类型。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> newSeriesGroup = chart->get_SeriesGroups()->Add(Aspose::Words::Drawing::Charts::ChartSeriesType::Line);
// 为新系列组指定使用次要坐标轴。
newSeriesGroup->set_AxisGroup(Aspose::Words::Drawing::Charts::AxisGroup::Secondary);
// 隐藏次要 X 轴。
newSeriesGroup->get_AxisX()->set_Hidden(true);
// 定义次要 Y 轴的标题。
newSeriesGroup->get_AxisY()->get_Title()->set_Show(true);
newSeriesGroup->get_AxisY()->get_Title()->set_Text(u"Secondary Y axis");

ASSERT_EQ(Aspose::Words::Drawing::Charts::ChartSeriesType::Line, newSeriesGroup->get_SeriesType());

// 向新系列组添加一个系列。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series3 = newSeriesGroup->get_Series()->Add(u"Series of secondary series group", categories, System::MakeArray<double>({13, 11, 16}));
series3->get_Format()->get_Stroke()->set_Weight(3.5);

doc->Save(get_ArtifactsDir() + u"Charts.SecondaryAxis.docx");
```

## 另见

* Enum [AxisGroup](../../axisgroup/)
* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
