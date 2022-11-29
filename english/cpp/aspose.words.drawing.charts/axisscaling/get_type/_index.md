---
title: get_Type
second_title: Aspose.Words for C++ API Reference
description: Gets or sets scaling type of the axis.
type: docs
weight: 53
url: /cpp/aspose.words.drawing.charts/axisscaling/get_type/
---
## AxisScaling::get_Type method


Gets or sets scaling type of the axis.

```cpp
Aspose::Words::Drawing::Charts::AxisScaleType Aspose::Words::Drawing::Charts::AxisScaling::get_Type() const
```


## Examples



Shows how to apply logarithmic scaling to a chart axis. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> chartShape = builder->InsertChart(ChartType::Scatter, 450, 300);
SharedPtr<Chart> chart = chartShape->get_Chart();

// Clear the chart's demo data series to start with a clean chart.
chart->get_Series()->Clear();

// Insert a series with X/Y coordinates for five points.
chart->get_Series()->Add(u"Series 1", MakeArray<double>({1.0, 2.0, 3.0, 4.0, 5.0}), MakeArray<double>({1.0, 20.0, 400.0, 8000.0, 160000.0}));

// The scaling of the X-axis is linear by default,
// displaying evenly incrementing values that cover our X-value range (0, 1, 2, 3...).
// A linear axis is not ideal for our Y-values
// since the points with the smaller Y-values will be harder to read.
// A logarithmic scaling with a base of 20 (1, 20, 400, 8000...)
// will spread the plotted points, allowing us to read their values on the chart more easily.
chart->get_AxisY()->get_Scaling()->set_Type(AxisScaleType::Logarithmic);
chart->get_AxisY()->get_Scaling()->set_LogBase(20);

doc->Save(ArtifactsDir + u"Charts.AxisScaling.docx");
```

## See Also

* Enum [AxisScaleType](../../axisscaletype/)
* Class [AxisScaling](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words](../../../)
