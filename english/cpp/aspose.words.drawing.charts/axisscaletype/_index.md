---
title: Aspose::Words::Drawing::Charts::AxisScaleType enum
linktitle: AxisScaleType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::AxisScaleType enum. Specifies the possible scale types for an axis in C++.'
type: docs
weight: 23000
url: /cpp/aspose.words.drawing.charts/axisscaletype/
---
## AxisScaleType enum


Specifies the possible scale types for an axis.

```cpp
enum class AxisScaleType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Linear | 0 | Linear scaling. |
| Logarithmic | 1 | Logarithmic scaling. |


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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
