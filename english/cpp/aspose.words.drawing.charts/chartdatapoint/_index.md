---
title: Aspose::Words::Drawing::Charts::ChartDataPoint class
linktitle: ChartDataPoint
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartDataPoint class. Allows to specify formatting of a single data point on the chart. To learn more, visit the Working with Charts documentation article in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.drawing.charts/chartdatapoint/
---
## ChartDataPoint class


Allows to specify formatting of a single data point on the chart. 
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) documentation article.

```cpp
class ChartDataPoint : public IChartDataPoint,
                       public Core::IChartFormatSource
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
| [set_Bubble3D](./set_bubble3d/)(bool) override | Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them. |
| [set_Explosion](./set_explosion/)(int32_t) override | Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts. |
| [set_InvertIfNegative](./set_invertifnegative/)(bool) override | Specifies whether the parent element shall inverts its colors if the value is negative. |
| virtual [get_Bubble3D](../ichartdatapoint/get_bubble3d/)() | Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them. |
| virtual [get_Explosion](../ichartdatapoint/get_explosion/)() | Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts. |
| virtual [get_InvertIfNegative](../ichartdatapoint/get_invertifnegative/)() | Specifies whether the parent element shall inverts its colors if the value is negative. |
| virtual [get_Marker](../ichartdatapoint/get_marker/)() | Specifies a data marker. Marker is automatically created when requested. |
| virtual [set_Bubble3D](../ichartdatapoint/set_bubble3d/)(bool) | Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them. |
| virtual [set_Explosion](../ichartdatapoint/set_explosion/)(int32_t) | Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts. |
| virtual [set_InvertIfNegative](../ichartdatapoint/set_invertifnegative/)(bool) | Specifies whether the parent element shall inverts its colors if the value is negative. |
## Remarks

 On a series, the [ChartDataPoint](./) object is a member of the [ChartDataPointCollection](../chartdatapointcollection/). The [ChartDataPointCollection](../chartdatapointcollection/) contains a [ChartDataPoint](./) object for each point. 
## See Also

* Interface [IChartDataPoint](../ichartdatapoint/)
* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
