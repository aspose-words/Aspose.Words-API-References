---
title: Aspose::Words::Drawing::Charts::AxisScaling class
linktitle: AxisScaling
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::AxisScaling class. Represents the scaling options of the axis. To learn more, visit the  documentation article in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.drawing.charts/axisscaling/
---
## AxisScaling class


Represents the scaling options of the axis. To learn more, visit the [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) documentation article.

```cpp
class AxisScaling : public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource
```

## Methods

| Method | Description |
| --- | --- |
| [AxisScaling](./axisscaling/)() |  |
| [get_LogBase](./get_logbase/)() const | Gets or sets the logarithmic base for a logarithmic axis. |
| [get_Maximum](./get_maximum/)() | Gets or sets the maximum value of the axis. |
| [get_Minimum](./get_minimum/)() | Gets or sets minimum value of the axis. |
| [get_Type](./get_type/)() const | Gets or sets scaling type of the axis. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_LogBase](./set_logbase/)(double) | Setter for [Aspose::Words::Drawing::Charts::AxisScaling::get_LogBase](./get_logbase/). |
| [set_Maximum](./set_maximum/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::AxisBound\>\&) | Setter for [Aspose::Words::Drawing::Charts::AxisScaling::get_Maximum](./get_maximum/). |
| [set_Minimum](./set_minimum/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::AxisBound\>\&) | Setter for [Aspose::Words::Drawing::Charts::AxisScaling::get_Minimum](./get_minimum/). |
| [set_Type](./set_type/)(Aspose::Words::Drawing::Charts::AxisScaleType) | Setter for [Aspose::Words::Drawing::Charts::AxisScaling::get_Type](./get_type/). |
| static [Type](./type/)() |  |

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
