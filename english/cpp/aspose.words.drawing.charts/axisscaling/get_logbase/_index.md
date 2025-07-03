---
title: Aspose::Words::Drawing::Charts::AxisScaling::get_LogBase method
linktitle: get_LogBase
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::AxisScaling::get_LogBase method. Gets or sets the logarithmic base for a logarithmic axis in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.drawing.charts/axisscaling/get_logbase/
---
## AxisScaling::get_LogBase method


Gets or sets the logarithmic base for a logarithmic axis.

```cpp
double Aspose::Words::Drawing::Charts::AxisScaling::get_LogBase() const
```

## Remarks


The property is not supported by MS Office 2016 new charts.

Valid range of a floating point value is greater than or equal to 2 and less than or equal to 1000. The property has effect only if [Type](../get_type/) is set to [Logarithmic](../../axisscaletype/).

Setting this property sets the [Type](../get_type/) property to [Logarithmic](../../axisscaletype/).

## Examples



Shows how to apply logarithmic scaling to a chart axis. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Clear the chart's demo data series to start with a clean chart.
chart->get_Series()->Clear();

// Insert a series with X/Y coordinates for five points.
chart->get_Series()->Add(u"Series 1", System::MakeArray<double>({1.0, 2.0, 3.0, 4.0, 5.0}), System::MakeArray<double>({1.0, 20.0, 400.0, 8000.0, 160000.0}));

// The scaling of the X-axis is linear by default,
// displaying evenly incrementing values that cover our X-value range (0, 1, 2, 3...).
// A linear axis is not ideal for our Y-values
// since the points with the smaller Y-values will be harder to read.
// A logarithmic scaling with a base of 20 (1, 20, 400, 8000...)
// will spread the plotted points, allowing us to read their values on the chart more easily.
chart->get_AxisY()->get_Scaling()->set_Type(Aspose::Words::Drawing::Charts::AxisScaleType::Logarithmic);
chart->get_AxisY()->get_Scaling()->set_LogBase(20);

doc->Save(get_ArtifactsDir() + u"Charts.AxisScaling.docx");
```

## See Also

* Class [AxisScaling](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
