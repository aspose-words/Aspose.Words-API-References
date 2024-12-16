---
title: Aspose::Words::Drawing::Charts::ChartSeriesGroup class
linktitle: ChartSeriesGroup
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartSeriesGroup class. Represents properties of a chart series group, that is, the properties of chart series of the same type associated with the same axes in C++.'
type: docs
weight: 17334
url: /cpp/aspose.words.drawing.charts/chartseriesgroup/
---
## ChartSeriesGroup class


Represents properties of a chart series group, that is, the properties of chart series of the same type associated with the same axes.

```cpp
class ChartSeriesGroup : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_AxisGroup](./get_axisgroup/)() | Gets the axis group to which this series group belongs. |
| [get_AxisX](./get_axisx/)() | Provides access to properties of the X axis of this series group. |
| [get_AxisY](./get_axisy/)() | Provides access to properties of the Y axis of this series group. |
| [get_BubbleScale](./get_bubblescale/)() | Gets or sets the size of the bubbles as a percentage of their default size. |
| [get_DoughnutHoleSize](./get_doughnutholesize/)() | Gets or sets the hole size of the parent doughnut chart as a percentage. |
| [get_FirstSliceAngle](./get_firstsliceangle/)() | Gets or sets the angle, in degrees, of the first slice of the parent pie chart. |
| [get_GapWidth](./get_gapwidth/)() | Gets or sets the percentage of gap width between chart elements. |
| [get_Overlap](./get_overlap/)() | Gets or sets the percentage of how much the series bars or columns overlap. |
| [get_SecondSectionSize](./get_secondsectionsize/)() | Gets or sets the size of the pie chart secondary section as a percentage. |
| [get_Series](./get_series/)() | Gets a collection of series that belong to this series group. |
| [get_SeriesType](./get_seriestype/)() | Gets the type of chart series included in this group. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AxisGroup](./set_axisgroup/)(Aspose::Words::Drawing::Charts::AxisGroup) | Sets the axis group to which this series group belongs. |
| [set_BubbleScale](./set_bubblescale/)(int32_t) | Setter for [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale](./get_bubblescale/). |
| [set_DoughnutHoleSize](./set_doughnutholesize/)(int32_t) | Setter for [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_DoughnutHoleSize](./get_doughnutholesize/). |
| [set_FirstSliceAngle](./set_firstsliceangle/)(int32_t) | Setter for [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle](./get_firstsliceangle/). |
| [set_GapWidth](./set_gapwidth/)(int32_t) | Setter for [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth](./get_gapwidth/). |
| [set_Overlap](./set_overlap/)(int32_t) | Setter for [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap](./get_overlap/). |
| [set_SecondSectionSize](./set_secondsectionsize/)(int32_t) | Setter for [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize](./get_secondsectionsize/). |
| static [Type](./type/)() |  |
## Remarks


Combo charts contains multiple chart series groups, with a separate group for each series type.

Also, you can create a chart series group to assign secondary axes to one or more chart series.

To learn more, visit the [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) documentation article. 
## See Also

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
