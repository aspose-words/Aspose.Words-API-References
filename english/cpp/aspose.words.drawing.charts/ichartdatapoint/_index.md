---
title: Aspose::Words::Drawing::Charts::IChartDataPoint interface
linktitle: IChartDataPoint
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::IChartDataPoint interface. Contains properties of a single data point on the chart in C++.'
type: docs
weight: 19000
url: /cpp/aspose.words.drawing.charts/ichartdatapoint/
---
## IChartDataPoint interface


Contains properties of a single data point on the chart.

```cpp
class IChartDataPoint : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [get_Bubble3D](./get_bubble3d/)() | Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them. |
| virtual [get_Explosion](./get_explosion/)() | Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts. |
| virtual [get_InvertIfNegative](./get_invertifnegative/)() | Specifies whether the parent element shall inverts its colors if the value is negative. |
| virtual [get_Marker](./get_marker/)() | Specifies a data marker. Marker is automatically created when requested. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [set_Bubble3D](./set_bubble3d/)(bool) | Setter for [Aspose::Words::Drawing::Charts::IChartDataPoint::get_Bubble3D](./get_bubble3d/). |
| virtual [set_Explosion](./set_explosion/)(int32_t) | Setter for [Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion](./get_explosion/). |
| virtual [set_InvertIfNegative](./set_invertifnegative/)(bool) | Specifies whether the parent element shall inverts its colors if the value is negative. |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
