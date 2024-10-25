---
title: Aspose::Words::Drawing::Charts::AxisTickLabelPosition enum
linktitle: AxisTickLabelPosition
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::AxisTickLabelPosition enum. Specifies the possible positions for tick labels in C++.'
type: docs
weight: 24000
url: /cpp/aspose.words.drawing.charts/axisticklabelposition/
---
## AxisTickLabelPosition enum


Specifies the possible positions for tick labels.

```cpp
enum class AxisTickLabelPosition
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| High | 0 | Specifies the axis labels shall be at the high end of the perpendicular axis. |
| Low | 1 | Specifies the axis labels shall be at the low end of the perpendicular axis. |
| NextToAxis | 2 | Specifies the axis labels shall be next to the axis. |
| None | 3 | Specifies the axis labels are not drawn. |
| Default | n/a | Specifies default value of tick labels position. |


## Examples



Shows how to insert chart with date/time values. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> shape = builder->InsertChart(ChartType::Line, 500, 300);
SharedPtr<Chart> chart = shape->get_Chart();

// Clear the chart's demo data series to start with a clean chart.
chart->get_Series()->Clear();

// Add a custom series containing date/time values for the X-axis, and respective decimal values for the Y-axis.
chart->get_Series()->Add(u"Aspose Test Series",
                         MakeArray<System::DateTime>({System::DateTime(2017, 11, 6), System::DateTime(2017, 11, 9), System::DateTime(2017, 11, 15),
                                                      System::DateTime(2017, 11, 21), System::DateTime(2017, 11, 25), System::DateTime(2017, 11, 29)}),
                         MakeArray<double>({1.2, 0.3, 2.1, 2.9, 4.2, 5.3}));

// Set lower and upper bounds for the X-axis.
SharedPtr<ChartAxis> xAxis = chart->get_AxisX();
xAxis->get_Scaling()->set_Minimum(MakeObject<AxisBound>(System::DateTime(2017, 11, 5).ToOADate()));
xAxis->get_Scaling()->set_Maximum(MakeObject<AxisBound>(System::DateTime(2017, 12, 3)));

// Set the major units of the X-axis to a week, and the minor units to a day.
xAxis->set_BaseTimeUnit(AxisTimeUnit::Days);
xAxis->set_MajorUnit(7.0);
xAxis->set_MajorTickMark(AxisTickMark::Cross);
xAxis->set_MinorUnit(1.0);
xAxis->set_MinorTickMark(AxisTickMark::Outside);

// Define Y-axis properties for decimal values.
SharedPtr<ChartAxis> yAxis = chart->get_AxisY();
yAxis->get_TickLabels()->set_Position(AxisTickLabelPosition::High);
yAxis->set_MajorUnit(100.0);
yAxis->set_MinorUnit(50.0);
yAxis->get_DisplayUnit()->set_Unit(AxisBuiltInUnit::Hundreds);
yAxis->get_Scaling()->set_Minimum(MakeObject<AxisBound>(100.0));
yAxis->get_Scaling()->set_Maximum(MakeObject<AxisBound>(700.0));

doc->Save(ArtifactsDir + u"Charts.DateTimeValues.docx");
```

## See Also

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
