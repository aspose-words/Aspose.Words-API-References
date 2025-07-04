---
title: Aspose::Words::Drawing::Charts::ChartDataLabelCollection class
linktitle: ChartDataLabelCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartDataLabelCollection class. Represents a collection of ChartDataLabel. To learn more, visit the  documentation article in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class


Represents a collection of [ChartDataLabel](../chartdatalabel/). To learn more, visit the [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) documentation article.

```cpp
class ChartDataLabelCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabel>>,
                                 public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                                 public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Methods

| Method | Description |
| --- | --- |
| [ClearFormat](./clearformat/)() | Clears format of all [ChartDataLabel](../chartdatalabel/) in this collection. |
| [get_Count](./get_count/)() | Returns the number of [ChartDataLabel](../chartdatalabel/) in this collection. |
| [get_Font](./get_font/)() | Provides access to the font formatting of the data labels of the entire series. |
| [get_Format](./get_format/)() | Provides access to fill and line formatting of the data labels. |
| [get_NumberFormat](./get_numberformat/)() | Gets an [ChartNumberFormat](../chartnumberformat/) instance allowing to set number format for the data labels of the entire series. |
| [get_Orientation](./get_orientation/)() | Gets or sets the text orientation of the data labels of the entire series. |
| [get_Position](./get_position/)() | Gets or sets the position of the data labels. |
| [get_Rotation](./get_rotation/)() | Gets or sets the rotation of the data labels of the entire series in degrees. |
| [get_Separator](./get_separator/)() | Gets or sets string separator used for the data labels of the entire series. The default is a comma, except for pie charts showing only category name and percentage, when a line break shall be used instead. |
| [get_ShowBubbleSize](./get_showbubblesize/)() | Allows to specify whether bubble size is to be displayed for the data labels of the entire series. Applies only to Bubble charts. Default value is **false**. |
| [get_ShowCategoryName](./get_showcategoryname/)() | Allows to specify whether category name is to be displayed for the data labels of the entire series. Default value is **false**. |
| [get_ShowDataLabelsRange](./get_showdatalabelsrange/)() | Allows to specify whether values from data labels range to be displayed in the data labels of the entire series. Default value is **false**. |
| [get_ShowLeaderLines](./get_showleaderlines/)() | Allows to specify whether data label leader lines need be shown for the data labels of the entire series. Default value is **false**. |
| [get_ShowLegendKey](./get_showlegendkey/)() | Allows to specify whether legend key is to be displayed for the data labels of the entire series. Default value is **false**. |
| [get_ShowPercentage](./get_showpercentage/)() | Allows to specify whether percentage value is to be displayed for the data labels of the entire series. Default value is **false**. Applies only to Pie charts. |
| [get_ShowSeriesName](./get_showseriesname/)() | Returns or sets a Boolean to indicate the series name display behavior for the data labels of the entire series. **true** to show the series name; **false** to hide. By default **false**. |
| [get_ShowValue](./get_showvalue/)() | Allows to specify whether values are to be displayed in the data labels of the entire series. Default value is **false**. |
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator object. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Returns [ChartDataLabel](../chartdatalabel/) for the specified index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Orientation](./get_orientation/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::ChartDataLabelPosition) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Position](./get_position/). |
| [set_Rotation](./set_rotation/)(int32_t) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Rotation](./get_rotation/). |
| [set_Separator](./set_separator/)(const System::String\&) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator](./get_separator/). |
| [set_ShowBubbleSize](./set_showbubblesize/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowBubbleSize](./get_showbubblesize/). |
| [set_ShowCategoryName](./set_showcategoryname/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowCategoryName](./get_showcategoryname/). |
| [set_ShowDataLabelsRange](./set_showdatalabelsrange/)(bool) | Allows to specify whether values from data labels range to be displayed in the data labels of the entire series. Default value is **false**. |
| [set_ShowLeaderLines](./set_showleaderlines/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLeaderLines](./get_showleaderlines/). |
| [set_ShowLegendKey](./set_showlegendkey/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLegendKey](./get_showlegendkey/). |
| [set_ShowPercentage](./set_showpercentage/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowPercentage](./get_showpercentage/). |
| [set_ShowSeriesName](./set_showseriesname/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowSeriesName](./get_showseriesname/). |
| [set_ShowValue](./set_showvalue/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowValue](./get_showvalue/). |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
