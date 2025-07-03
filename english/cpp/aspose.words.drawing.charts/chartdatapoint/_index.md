---
title: Aspose::Words::Drawing::Charts::ChartDataPoint class
linktitle: ChartDataPoint
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartDataPoint class. Allows to specify formatting of a single data point on the chart. To learn more, visit the  documentation article in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.drawing.charts/chartdatapoint/
---
## ChartDataPoint class


Allows to specify formatting of a single data point on the chart. To learn more, visit the [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) documentation article.

```cpp
class ChartDataPoint : public Aspose::Words::Drawing::Charts::IChartDataPoint,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Methods

| Method | Description |
| --- | --- |
| [ClearFormat](./clearformat/)() | Clears format of this data point. The properties are set to the default values defined in the parent series. |
| [get_Bubble3D](./get_bubble3d/)() override | Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them. |
| [get_Explosion](./get_explosion/)() override | Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts. |
| [get_Format](./get_format/)() | Provides access to fill and line formatting of this data point. |
| [get_Index](./get_index/)() | Index of the data point this object applies formatting to. |
| [get_InvertIfNegative](./get_invertifnegative/)() override | Specifies whether the parent element shall inverts its colors if the value is negative. |
| [get_Marker](./get_marker/)() override | Specifies chart data marker. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Bubble3D](./set_bubble3d/)(bool) override | Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them. |
| [set_Explosion](./set_explosion/)(int32_t) override | Setter for [Aspose::Words::Drawing::Charts::ChartDataPoint::get_Explosion](./get_explosion/). |
| [set_InvertIfNegative](./set_invertifnegative/)(bool) override | Specifies whether the parent element shall inverts its colors if the value is negative. |
| static [Type](./type/)() |  |
## See Also

* Interface [IChartDataPoint](../ichartdatapoint/)
* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
