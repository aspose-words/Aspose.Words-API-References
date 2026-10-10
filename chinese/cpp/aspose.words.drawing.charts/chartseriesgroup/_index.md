---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup 类"
linktitle: "ChartSeriesGroup"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup 类。表示图表系列组的属性，即在 C++ 中与相同坐标轴关联的相同类型图表系列的属性。"
type: docs
weight: 17334
url: /zh/cpp/aspose.words.drawing.charts/chartseriesgroup/
---
## ChartSeriesGroup class


表示图表系列组的属性，即具有相同类型并关联到相同坐标轴的图表系列的属性。

```cpp
class ChartSeriesGroup : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_AxisGroup](./get_axisgroup/)() | 获取或设置此系列组所属的坐标轴组。 |
| [get_AxisX](./get_axisx/)() | 提供对该系列组 X 轴属性的访问。 |
| [get_AxisY](./get_axisy/)() | 提供对该系列组 Y 轴属性的访问。 |
| [get_BubbleScale](./get_bubblescale/)() | 获取或设置气泡的大小，作为其默认大小的百分比。 |
| [get_DoughnutHoleSize](./get_doughnutholesize/)() | 获取或设置父环形图的孔大小，作为百分比。 |
| [get_FirstSliceAngle](./get_firstsliceangle/)() | 获取或设置父饼图第一块的角度（以度为单位）。 |
| [get_GapWidth](./get_gapwidth/)() | 获取或设置图表元素之间间隙宽度的百分比。 |
| [get_Overlap](./get_overlap/)() | 获取或设置系列条形或柱形的重叠百分比。 |
| [get_SecondSectionSize](./get_secondsectionsize/)() | 获取或设置饼图次要部分的大小，作为百分比。 |
| [get_Series](./get_series/)() | 获取属于此系列组的系列集合。 |
| [get_SeriesType](./get_seriestype/)() | 获取此组中包含的图表系列类型。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AxisGroup](./set_axisgroup/)(Aspose::Words::Drawing::Charts::AxisGroup) | 设置 [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_AxisGroup](./get_axisgroup/). |
| [set_BubbleScale](./set_bubblescale/)(int32_t) | 设置 [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale](./get_bubblescale/). |
| [set_DoughnutHoleSize](./set_doughnutholesize/)(int32_t) | 设置 [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_DoughnutHoleSize](./get_doughnutholesize/). |
| [set_FirstSliceAngle](./set_firstsliceangle/)(int32_t) | 设置 [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle](./get_firstsliceangle/). |
| [set_GapWidth](./set_gapwidth/)(int32_t) | 设置 [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth](./get_gapwidth/). |
| [set_Overlap](./set_overlap/)(int32_t) | 设置 [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap](./get_overlap/). |
| [set_SecondSectionSize](./set_secondsectionsize/)(int32_t) | 设置 [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize](./get_secondsectionsize/). |
| static [Type](./type/)() |  |
## 备注


组合图表包含多个图表系列组，每种系列类型都有一个单独的组。

此外，您可以创建一个图表系列组，以将次要坐标轴分配给一个或多个图表系列。

欲了解更多信息，请访问[Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/)文档文章。

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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
