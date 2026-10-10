---
title: "Aspose::Words::Drawing::Charts::ChartDataPoint 类"
linktitle: "ChartDataPoint"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartDataPoint 类。允许指定图表中单个数据点的格式。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.drawing.charts/chartdatapoint/
---
## ChartDataPoint class


允许指定图表上单个数据点的格式。要了解更多，请访问[Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/)文档文章。

```cpp
class ChartDataPoint : public Aspose::Words::Drawing::Charts::IChartDataPoint,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [ClearFormat](./clearformat/)() | 清除此数据点的格式。属性将设置为父系列中定义的默认值。 |
| [get_Bubble3D](./get_bubble3d/)() override | 指定气泡图中的气泡是否应应用 3D 效果。 |
| [get_Explosion](./get_explosion/)() override | 指定数据点应从饼图中心移动的距离。可以为负，负值表示未设置此属性且不应应用爆炸效果。仅适用于饼图。 |
| [get_Format](./get_format/)() | 提供对该数据点的填充和线条格式的访问。 |
| [get_Index](./get_index/)() | 此对象应用格式的数据点的索引。 |
| [get_InvertIfNegative](./get_invertifnegative/)() override | 指定当值为负时，父元素是否应反转其颜色。 |
| [get_Marker](./get_marker/)() override | 指定图表数据标记。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Bubble3D](./set_bubble3d/)(bool) override | 指定气泡图中的气泡是否应应用 3D 效果。 |
| [set_Explosion](./set_explosion/)(int32_t) override | 用于 [Aspose::Words::Drawing::Charts::ChartDataPoint::get_Explosion](./get_explosion/) 的设置器。 |
| [set_InvertIfNegative](./set_invertifnegative/)(bool) override | 指定当值为负时，父元素是否应反转其颜色。 |
| static [Type](./type/)() |  |
## 另见

* Interface [IChartDataPoint](../ichartdatapoint/)
* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
