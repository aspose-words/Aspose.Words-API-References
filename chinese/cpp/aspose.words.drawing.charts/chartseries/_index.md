---
title: "Aspose::Words::Drawing::Charts::ChartSeries class"
linktitle: "ChartSeries"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartSeries class. 表示图表系列属性。要了解更多信息，请访问 C++ 中的文档文章。"
type: docs
weight: 16000
url: /zh/cpp/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class


表示图表系列属性。要了解更多，请访问[Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/)文档文章。

```cpp
class ChartSeries : public Aspose::Words::Drawing::Charts::IChartDataPoint,
                    public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | 将指定的 X 值添加到图表系列中。如果系列支持 Y 值和气泡大小，则它们在该 X 值处将为空。 |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | 将指定的 X 和 Y 值添加到图表系列中。 |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) | 将指定的 X 值、Y 值和气泡大小添加到图表系列中。 |
| [Clear](./clear/)() | 从图表系列中移除所有数据值。所有单个数据点和数据标签的格式将被清除。 |
| [ClearValues](./clearvalues/)() | 从图表系列中移除所有数据值，同时保留数据点和数据标签的格式。 |
| [CopyFormatFrom](./copyformatfrom/)(int32_t) | 从具有指定索引的数据点复制默认数据点格式。 |
| [get_Bubble3D](./get_bubble3d/)() override | 指定气泡图中的气泡是否应应用 3D 效果。 |
| [get_BubbleSizes](./get_bubblesizes/)() | 获取此图表系列的气泡大小集合。 |
| [get_DataLabels](./get_datalabels/)() | 指定整个系列的数据标签设置。 |
| [get_DataPoints](./get_datapoints/)() const | 返回此系列中所有数据点的格式对象集合。 |
| [get_Explosion](./get_explosion/)() override | 指定数据点应从饼图中心移动的距离。可以为负，负值表示未设置此属性且不应应用爆炸效果。仅适用于饼图。 |
| [get_Format](./get_format/)() | 提供对系列的填充和线条格式的访问。 |
| [get_HasDataLabels](./get_hasdatalabels/)() const | 获取或设置指示是否为系列显示数据标签的标志。 |
| [get_InvertIfNegative](./get_invertifnegative/)() override | 指定当值为负时，父元素是否应反转其颜色。 |
| [get_LegendEntry](./get_legendentry/)() | 获取此图表系列的图例项。 |
| [get_Marker](./get_marker/)() override | 指定数据标记。请求时会自动创建标记。 |
| [get_Name](./get_name/)() | 获取系列的名称，如果未显式设置名称，则使用索引生成。默认返回基于索引加一的 Series。 |
| [get_SeriesType](./get_seriestype/)() | 获取此图表系列的类型。 |
| [get_Smooth](./get_smooth/)() const | 允许指定是否使用 Catmull-Rom 样条平滑连接图表上的点的线条。 |
| [get_XValues](./get_xvalues/)() | 获取此图表系列的 X 值集合。 |
| [get_YValues](./get_yvalues/)() | 获取此图表系列的 Y 值集合。 |
| [GetType](./gettype/)() const override |  |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | 在指定索引处将指定的 X 值插入图表系列。如果系列支持 Y 值和气泡大小，则它们在该 X 值处将为空。 |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | 在指定索引处将指定的 X 和 Y 值插入图表系列。 |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) | 在指定索引处将指定的 X 值、Y 值和气泡大小插入图表系列。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(int32_t) | 在指定索引处从图表系列中移除 X 值、Y 值和（如果支持）气泡大小。相应的数据点和数据标签也会被移除。 |
| [set_Bubble3D](./set_bubble3d/)(bool) override | 用于 [Aspose::Words::Drawing::Charts::ChartSeries::get_Bubble3D](./get_bubble3d/) 的设置器。 |
| [set_Explosion](./set_explosion/)(int32_t) override | 指定数据点应从饼图中心移动的距离。可以为负，负值表示未设置此属性且不应应用爆炸效果。仅适用于饼图。 |
| [set_HasDataLabels](./set_hasdatalabels/)(bool) | 用于 [Aspose::Words::Drawing::Charts::ChartSeries::get_HasDataLabels](./get_hasdatalabels/) 的设置器。 |
| [set_InvertIfNegative](./set_invertifnegative/)(bool) override | 指定当值为负时，父元素是否应反转其颜色。 |
| [set_Name](./set_name/)(const System::String\&) | 设置系列的名称，如果未显式设置名称，则使用索引生成。默认返回基于索引加一的 Series。 |
| [set_Smooth](./set_smooth/)(bool) | 允许指定是否使用 Catmull-Rom 样条平滑连接图表上的点的线条。 |
| static [Type](./type/)() |  |
## 另见

* Interface [IChartDataPoint](../ichartdatapoint/)
* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
