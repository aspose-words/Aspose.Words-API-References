---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection class"
linktitle: "ChartDataLabelCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection class. 表示 ChartDataLabel 的集合。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class


表示一个 [ChartDataLabel](../chartdatalabel/) 的集合。欲了解更多，请访问 [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) 文档文章。

```cpp
class ChartDataLabelCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabel>>,
                                 public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                                 public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [ClearFormat](./clearformat/)() | 清除此集合中所有 [ChartDataLabel](../chartdatalabel/) 的格式。 |
| [get_Count](./get_count/)() | 返回此集合中 [ChartDataLabel](../chartdatalabel/) 的数量。 |
| [get_Font](./get_font/)() | 提供对整个系列数据标签字体格式的访问。 |
| [get_Format](./get_format/)() | 提供对数据标签填充和线条格式的访问。 |
| [get_NumberFormat](./get_numberformat/)() | 获取一个 [ChartNumberFormat](../chartnumberformat/) 实例，以便为整个系列的数据标签设置数字格式。 |
| [get_Orientation](./get_orientation/)() | 获取或设置整个系列数据标签的文字方向。 |
| [get_Position](./get_position/)() | 获取或设置数据标签的位置。 |
| [get_Rotation](./get_rotation/)() | 获取或设置整个系列数据标签的旋转角度（以度为单位）。 |
| [get_Separator](./get_separator/)() | 获取或设置整个系列数据标签使用的字符串分隔符。默认是逗号，除非是仅显示类别名称和百分比的饼图，此时应使用换行符。 |
| [get_ShowBubbleSize](./get_showbubblesize/)() | 允许指定是否在整个系列的数据标签中显示气泡大小。仅适用于气泡图。默认值为 **false**。 |
| [get_ShowCategoryName](./get_showcategoryname/)() | 允许指定是否在整个系列的数据标签中显示类别名称。默认值为 **false**。 |
| [get_ShowDataLabelsRange](./get_showdatalabelsrange/)() | 允许指定是否在整个系列的数据标签中显示数据标签范围的值。默认值为 **false**。 |
| [get_ShowLeaderLines](./get_showleaderlines/)() | 允许指定是否在整个系列的数据标签中显示数据标签引导线。默认值为 **false**。 |
| [get_ShowLegendKey](./get_showlegendkey/)() | 允许指定是否在整个系列的数据标签中显示图例键。默认值为 **false**。 |
| [get_ShowPercentage](./get_showpercentage/)() | 允许指定是否在整个系列的数据标签中显示百分比值。默认值为 **false**。仅适用于饼图。 |
| [get_ShowSeriesName](./get_showseriesname/)() | 返回或设置一个布尔值，以指示整个系列的数据标签中系列名称的显示行为。**true** 表示显示系列名称；**false** 表示隐藏。默认情况下为 **false**。 |
| [get_ShowValue](./get_showvalue/)() | 允许指定是否在整个系列的数据标签中显示数值。默认值为 **false**。 |
| [GetEnumerator](./getenumerator/)() override | 返回一个枚举器对象。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | 返回指定索引的 [ChartDataLabel](../chartdatalabel/)。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | 设置 [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Orientation](./get_orientation/) 的 setter。 |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::ChartDataLabelPosition) | 设置 [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Position](./get_position/) 的 setter。 |
| [set_Rotation](./set_rotation/)(int32_t) | 设置 [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Rotation](./get_rotation/) 的 setter。 |
| [set_Separator](./set_separator/)(const System::String\&) | 设置 [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator](./get_separator/) 的 setter。 |
| [set_ShowBubbleSize](./set_showbubblesize/)(bool) | 设置 [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowBubbleSize](./get_showbubblesize/) 的 setter。 |
| [set_ShowCategoryName](./set_showcategoryname/)(bool) | 设置 [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowCategoryName](./get_showcategoryname/) 的 setter。 |
| [set_ShowDataLabelsRange](./set_showdatalabelsrange/)(bool) | 允许指定是否在整个系列的数据标签中显示数据标签范围的值。默认值为 **false**。 |
| [set_ShowLeaderLines](./set_showleaderlines/)(bool) | 设置 [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLeaderLines](./get_showleaderlines/) 的 setter。 |
| [set_ShowLegendKey](./set_showlegendkey/)(bool) | 设置 [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLegendKey](./get_showlegendkey/) 的 setter。 |
| [set_ShowPercentage](./set_showpercentage/)(bool) | 设置 [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowPercentage](./get_showpercentage/) 的 setter。 |
| [set_ShowSeriesName](./set_showseriesname/)(bool) | 设置 [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowSeriesName](./get_showseriesname/) 的 setter。 |
| [set_ShowValue](./set_showvalue/)(bool) | 设置 [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowValue](./get_showvalue/) 的 setter。 |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
