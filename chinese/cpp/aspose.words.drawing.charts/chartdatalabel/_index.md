---
title: "Aspose::Words::Drawing::Charts::ChartDataLabel 类"
linktitle: "ChartDataLabel"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartDataLabel 类。表示图表点或趋势线上的数据标签。欲了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class


表示图表点或趋势线上的数据标签。要了解更多，请访问[Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/)文档文章。

```cpp
class ChartDataLabel : public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                       public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [ClearFormat](./clearformat/)() | 清除此数据标签的格式。属性将设置为父数据标签集合中定义的默认值。 |
| [get_Font](./get_font/)() | 提供对该数据标签的字体格式的访问。 |
| [get_Format](./get_format/)() | 提供对数据标签的填充和线条格式的访问。 |
| [get_Index](./get_index/)() | 指定包含元素的索引。此索引决定该元素适用于父对象的子集合中的哪一个。默认值为 0。 |
| [get_IsHidden](./get_ishidden/)() | 获取/设置指示此标签是否隐藏的标志。默认值为 **false**。 |
| [get_IsVisible](./get_isvisible/)() | 如果此数据标签有内容可显示，则返回 **true**。 |
| [get_Left](./get_left/)() | 获取或设置数据标签相对于图表左边缘或其由 [Position](./get_position/) 属性指定的位置的距离（单位为点），取决于 [LeftMode](./get_leftmode/) 属性的值。 |
| [get_LeftMode](./get_leftmode/)() | 获取或设置 [Left](./get_left/) 属性值的解释模式：是将数据标签的位置设置为相对于图表左边缘，还是相对于其由 [Position](./get_position/) 属性指定的位置。 |
| [get_NumberFormat](./get_numberformat/)() | 返回父元素的数字格式。 |
| [get_Orientation](./get_orientation/)() | 获取或设置标签文本的方向。 |
| [get_Position](./get_position/)() | 获取或设置数据标签的位置。 |
| [get_Rotation](./get_rotation/)() | 获取或设置标签的旋转角度（以度为单位）。 |
| [get_Separator](./get_separator/)() | 获取用于图表数据标签的字符串分隔符。默认是逗号，但对于仅显示类别名称和百分比的饼图，则使用换行符。 |
| [get_ShowBubbleSize](./get_showbubblesize/)() | 允许指定是否在图表的数据标签上显示气泡大小。仅适用于气泡图。默认值为 **false**。 |
| [get_ShowCategoryName](./get_showcategoryname/)() | 允许指定是否在图表的数据标签上显示类别名称。默认值为 **false**。 |
| [get_ShowDataLabelsRange](./get_showdatalabelsrange/)() | 允许指定是否在数据标签中显示来自数据标签范围的数值。默认值为 **false**。 |
| [get_ShowLeaderLines](./get_showleaderlines/)() | 允许指定是否显示数据标签的指引线。默认值为 **false**。 |
| [get_ShowLegendKey](./get_showlegendkey/)() | 允许指定是否在图表的数据标签上显示图例键。默认值为 **false**。 |
| [get_ShowPercentage](./get_showpercentage/)() | 允许指定是否在图表的数据标签上显示百分比值。默认值为 **false**。 |
| [get_ShowSeriesName](./get_showseriesname/)() | 返回一个布尔值，用于指示图表数据标签的系列名称显示行为。**true** 表示显示系列名称；**false** 表示隐藏。默认情况下为 **false**。 |
| [get_ShowValue](./get_showvalue/)() | 允许指定是否在数据标签中显示数值。默认值为 **false**。 |
| [get_Top](./get_top/)() | 获取或设置数据标签相对于图表顶部边缘或其由 [Position](./get_position/) 属性指定的位置的距离（单位为点），取决于 [TopMode](./get_topmode/) 属性的值。 |
| [get_TopMode](./get_topmode/)() | 获取或设置 [Top](./get_top/) 属性值的解释模式：是将数据标签的位置设置为相对于图表顶部边缘，还是相对于其由 [Position](./get_position/) 属性指定的位置。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsHidden](./set_ishidden/)(bool) | 获取/设置指示此标签是否隐藏的标志。默认值为 **false**。 |
| [set_Left](./set_left/)(double) | 用于设置 [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Left](./get_left/) 的 setter。 |
| [set_LeftMode](./set_leftmode/)(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode) | 用于设置 [Aspose::Words::Drawing::Charts::ChartDataLabel::get_LeftMode](./get_leftmode/) 的 setter。 |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | 用于设置 [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Orientation](./get_orientation/) 的 setter。 |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::ChartDataLabelPosition) | 用于设置 [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Position](./get_position/) 的 setter。 |
| [set_Rotation](./set_rotation/)(int32_t) | 用于设置 [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Rotation](./get_rotation/) 的 setter。 |
| [set_Separator](./set_separator/)(const System::String\&) | 设置图表数据标签使用的字符串分隔符。默认是逗号，但对于仅显示类别名称和百分比的饼图，则使用换行符。 |
| [set_ShowBubbleSize](./set_showbubblesize/)(bool) | 用于设置 [Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowBubbleSize](./get_showbubblesize/) 的 setter。 |
| [set_ShowCategoryName](./set_showcategoryname/)(bool) | 允许指定是否在图表的数据标签上显示类别名称。默认值为 **false**。 |
| [set_ShowDataLabelsRange](./set_showdatalabelsrange/)(bool) | 允许指定是否在数据标签中显示来自数据标签范围的数值。默认值为 **false**。 |
| [set_ShowLeaderLines](./set_showleaderlines/)(bool) | 允许指定是否显示数据标签的指引线。默认值为 **false**。 |
| [set_ShowLegendKey](./set_showlegendkey/)(bool) | 允许指定是否在图表的数据标签上显示图例键。默认值为 **false**。 |
| [set_ShowPercentage](./set_showpercentage/)(bool) | 允许指定是否在图表的数据标签上显示百分比值。默认值为 **false**。 |
| [set_ShowSeriesName](./set_showseriesname/)(bool) | 设置布尔值以指示图表数据标签的系列名称显示行为。**true** 表示显示系列名称；**false** 表示隐藏。默认 **false**。 |
| [set_ShowValue](./set_showvalue/)(bool) | 允许指定是否在数据标签中显示数值。默认值为 **false**。 |
| [set_Top](./set_top/)(double) | 用于设置 [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Top](./get_top/) 的 setter。 |
| [set_TopMode](./set_topmode/)(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode) | 用于设置 [Aspose::Words::Drawing::Charts::ChartDataLabel::get_TopMode](./get_topmode/) 的 setter。 |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
