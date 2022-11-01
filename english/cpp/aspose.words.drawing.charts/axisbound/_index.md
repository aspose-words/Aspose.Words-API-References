---
title: AxisBound
second_title: Aspose.Words for C++ API Reference
description: Represents minimum or maximum bound of axis values.
type: docs
weight: 1
url: /cpp/aspose.words.drawing.charts/axisbound/
---
## AxisBound class


Represents minimum or maximum bound of axis values.

```cpp
class AxisBound : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [AxisBound](./axisbound/)() | Creates a new instance indicating that axis bound should be determined automatically by a word-processing application. |
| [AxisBound](./axisbound/)(double) | Creates an axis bound represented as a number. |
| [AxisBound](./axisbound/)(System::DateTime) | Creates an axis bound represented as datetime value. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Determines whether the specified object is equal in value to the current object. |
| [get_IsAuto](./get_isauto/)() const | Returns a flag indicating that axis bound should be determined automatically. |
| [get_Value](./get_value/)() const | Returns numeric value of axis bound. |
| [get_ValueAsDate](./get_valueasdate/)() | Returns value of axis bound represented as datetime. |
| [GetHashCode](./gethashcode/)() const override | Serves as a hash function for this type. |
| [ToString](./tostring/)() const override | Returns a user-friendly string that displays the value of this object. |

Bound can be specified as a numeric, datetime or a special "auto" value.

The instances of this class are immutable.

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
yAxis->set_TickLabelPosition(AxisTickLabelPosition::High);
yAxis->set_MajorUnit(100.0);
yAxis->set_MinorUnit(50.0);
yAxis->get_DisplayUnit()->set_Unit(AxisBuiltInUnit::Hundreds);
yAxis->get_Scaling()->set_Minimum(MakeObject<AxisBound>(100.0));
yAxis->get_Scaling()->set_Maximum(MakeObject<AxisBound>(700.0));

doc->Save(ArtifactsDir + u"Charts.DateTimeValues.docx");
```

