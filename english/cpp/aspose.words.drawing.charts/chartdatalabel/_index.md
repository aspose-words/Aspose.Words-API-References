---
title: Aspose::Words::Drawing::Charts::ChartDataLabel class
linktitle: ChartDataLabel
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartDataLabel class. Represents data label on a chart point or trendline. To learn more, visit the  documentation article in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class


Represents data label on a chart point or trendline. To learn more, visit the [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) documentation article.

```cpp
class ChartDataLabel : public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                       public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Methods

| Method | Description |
| --- | --- |
| [ClearFormat](./clearformat/)() | Clears format of this data label. The properties are set to the default values defined in the parent data label collection. |
| [get_Font](./get_font/)() | Provides access to the font formatting of this data label. |
| [get_Format](./get_format/)() | Provides access to fill and line formatting of the data label. |
| [get_Index](./get_index/)() | Specifies the index of the containing element. This index shall determine which of the parent's children collection this element applies to. Default value is 0. |
| [get_IsHidden](./get_ishidden/)() | Gets/sets a flag indicating whether this label is hidden. The default value is **false**. |
| [get_IsVisible](./get_isvisible/)() | Returns **true** if this data label has something to display. |
| [get_Left](./get_left/)() | Gets or sets the distance of the data label in points from the left edge of the chart or from the position specified by its [Position](./get_position/) property, depending on the value of the [LeftMode](./get_leftmode/) property. |
| [get_LeftMode](./get_leftmode/)() | Gets or sets the interpretation mode of the [Left](./get_left/) property value: whether it sets the location of the data label from the left edge of the chart of from the position specified by its [Position](./get_position/) property. |
| [get_NumberFormat](./get_numberformat/)() | Returns number format of the parent element. |
| [get_Orientation](./get_orientation/)() | Gets or sets the orientation of the label text. |
| [get_Position](./get_position/)() | Gets or sets the position of the data label. |
| [get_Rotation](./get_rotation/)() | Gets or sets the rotation of the label in degrees. |
| [get_Separator](./get_separator/)() | Gets string separator used for the data labels on a chart. The default is a comma, except for pie charts showing only category name and percentage, when a line break shall be used instead. |
| [get_ShowBubbleSize](./get_showbubblesize/)() | Allows to specify if bubble size is to be displayed for the data labels on a chart. Applies only to Bubble charts. Default value is **false**. |
| [get_ShowCategoryName](./get_showcategoryname/)() | Allows to specify if category name is to be displayed for the data labels on a chart. Default value is **false**. |
| [get_ShowDataLabelsRange](./get_showdatalabelsrange/)() | Allows to specify if values from data labels range to be displayed in the data labels. Default value is **false**. |
| [get_ShowLeaderLines](./get_showleaderlines/)() | Allows to specify if data label leader lines need be shown. Default value is **false**. |
| [get_ShowLegendKey](./get_showlegendkey/)() | Allows to specify if legend key is to be displayed for the data labels on a chart. Default value is **false**. |
| [get_ShowPercentage](./get_showpercentage/)() | Allows to specify if percentage value is to be displayed for the data labels on a chart. Default value is **false**. |
| [get_ShowSeriesName](./get_showseriesname/)() | Returns a Boolean to indicate the series name display behavior for the data labels on a chart. **true** to show the series name; **false** to hide. By default **false**. |
| [get_ShowValue](./get_showvalue/)() | Allows to specify if values are to be displayed in the data labels. Default value is **false**. |
| [get_Top](./get_top/)() | Gets or sets the distance of the data label in points from the top edge of the chart or from the position specified by its [Position](./get_position/) property, depending on the value of the [TopMode](./get_topmode/) property. |
| [get_TopMode](./get_topmode/)() | Gets or sets the interpretation mode of the [Top](./get_top/) property value: whether it sets the location of the data label from the top edge of the chart of from the position specified by its [Position](./get_position/) property. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsHidden](./set_ishidden/)(bool) | Gets/sets a flag indicating whether this label is hidden. The default value is **false**. |
| [set_Left](./set_left/)(double) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Left](./get_left/). |
| [set_LeftMode](./set_leftmode/)(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabel::get_LeftMode](./get_leftmode/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Orientation](./get_orientation/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::ChartDataLabelPosition) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Position](./get_position/). |
| [set_Rotation](./set_rotation/)(int32_t) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Rotation](./get_rotation/). |
| [set_Separator](./set_separator/)(const System::String\&) | Sets string separator used for the data labels on a chart. The default is a comma, except for pie charts showing only category name and percentage, when a line break shall be used instead. |
| [set_ShowBubbleSize](./set_showbubblesize/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowBubbleSize](./get_showbubblesize/). |
| [set_ShowCategoryName](./set_showcategoryname/)(bool) | Allows to specify if category name is to be displayed for the data labels on a chart. Default value is **false**. |
| [set_ShowDataLabelsRange](./set_showdatalabelsrange/)(bool) | Allows to specify if values from data labels range to be displayed in the data labels. Default value is **false**. |
| [set_ShowLeaderLines](./set_showleaderlines/)(bool) | Allows to specify if data label leader lines need be shown. Default value is **false**. |
| [set_ShowLegendKey](./set_showlegendkey/)(bool) | Allows to specify if legend key is to be displayed for the data labels on a chart. Default value is **false**. |
| [set_ShowPercentage](./set_showpercentage/)(bool) | Allows to specify if percentage value is to be displayed for the data labels on a chart. Default value is **false**. |
| [set_ShowSeriesName](./set_showseriesname/)(bool) | Sets a Boolean to indicate the series name display behavior for the data labels on a chart. **true** to show the series name; **false** to hide. By default **false**. |
| [set_ShowValue](./set_showvalue/)(bool) | Allows to specify if values are to be displayed in the data labels. Default value is **false**. |
| [set_Top](./set_top/)(double) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Top](./get_top/). |
| [set_TopMode](./set_topmode/)(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabel::get_TopMode](./get_topmode/). |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
