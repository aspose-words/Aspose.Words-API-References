---
title: AxisBound
second_title: Aspose.Words for C++ API Reference
description: Creates a new instance indicating that axis bound should be determined automatically by a word-processing application.
type: docs
weight: 14
url: /cpp/aspose.words.drawing.charts/axisbound/axisbound/
---
## AxisBound::AxisBound() constructor


Creates a new instance indicating that axis bound should be determined automatically by a word-processing application.

```cpp
Aspose::Words::Drawing::Charts::AxisBound::AxisBound()
```

## See Also

* Class [AxisBound](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words](../../../)
## AxisBound::AxisBound(double) constructor


Creates an axis bound represented as a number.

```cpp
Aspose::Words::Drawing::Charts::AxisBound::AxisBound(double value)
```


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


Shows how to set custom axis bounds. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> chartShape = builder->InsertChart(ChartType::Scatter, 450, 300);
SharedPtr<Chart> chart = chartShape->get_Chart();

// Clear the chart's demo data series to start with a clean chart.
chart->get_Series()->Clear();

// Add a series with two decimal arrays. The first array contains the X-values,
// and the second contains corresponding Y-values for points in the scatter chart.
chart->get_Series()->Add(u"Series 1", MakeArray<double>({1.1, 5.4, 7.9, 3.5, 2.1, 9.7}), MakeArray<double>({2.1, 0.3, 0.6, 3.3, 1.4, 1.9}));

// By default, default scaling is applied to the graph's X and Y-axes,
// so that both their ranges are big enough to encompass every X and Y-value of every series.
ASSERT_TRUE(chart->get_AxisX()->get_Scaling()->get_Minimum()->get_IsAuto());

// We can define our own axis bounds.
// In this case, we will make both the X and Y-axis rulers show a range of 0 to 10.
chart->get_AxisX()->get_Scaling()->set_Minimum(MakeObject<AxisBound>(0.0));
chart->get_AxisX()->get_Scaling()->set_Maximum(MakeObject<AxisBound>(10.0));
chart->get_AxisY()->get_Scaling()->set_Minimum(MakeObject<AxisBound>(0.0));
chart->get_AxisY()->get_Scaling()->set_Maximum(MakeObject<AxisBound>(10.0));

ASSERT_FALSE(chart->get_AxisX()->get_Scaling()->get_Minimum()->get_IsAuto());
ASSERT_FALSE(chart->get_AxisY()->get_Scaling()->get_Minimum()->get_IsAuto());

// Create a line chart with a series requiring a range of dates on the X-axis, and decimal values for the Y-axis.
chartShape = builder->InsertChart(ChartType::Line, 450, 300);
chart = chartShape->get_Chart();
chart->get_Series()->Clear();

ArrayPtr<System::DateTime> dates =
    MakeArray<System::DateTime>({System::DateTime(1973, 5, 11), System::DateTime(1981, 2, 4), System::DateTime(1985, 9, 23),
                                 System::DateTime(1989, 6, 28), System::DateTime(1994, 12, 15)});

chart->get_Series()->Add(u"Series 1", dates, MakeArray<double>({3.0, 4.7, 5.9, 7.1, 8.9}));

// We can set axis bounds in the form of dates as well, limiting the chart to a period.
// Setting the range to 1980-1990 will omit the two of the series values
// that are outside of the range from the graph.
chart->get_AxisX()->get_Scaling()->set_Minimum(MakeObject<AxisBound>(System::DateTime(1980, 1, 1)));
chart->get_AxisX()->get_Scaling()->set_Maximum(MakeObject<AxisBound>(System::DateTime(1990, 1, 1)));

doc->Save(ArtifactsDir + u"Charts.AxisBound.docx");
```

## See Also

* Class [AxisBound](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words](../../../)
## AxisBound::AxisBound(System::DateTime) constructor


Creates an axis bound represented as datetime value.

```cpp
Aspose::Words::Drawing::Charts::AxisBound::AxisBound(System::DateTime datetime)
```


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


Shows how to set custom axis bounds. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> chartShape = builder->InsertChart(ChartType::Scatter, 450, 300);
SharedPtr<Chart> chart = chartShape->get_Chart();

// Clear the chart's demo data series to start with a clean chart.
chart->get_Series()->Clear();

// Add a series with two decimal arrays. The first array contains the X-values,
// and the second contains corresponding Y-values for points in the scatter chart.
chart->get_Series()->Add(u"Series 1", MakeArray<double>({1.1, 5.4, 7.9, 3.5, 2.1, 9.7}), MakeArray<double>({2.1, 0.3, 0.6, 3.3, 1.4, 1.9}));

// By default, default scaling is applied to the graph's X and Y-axes,
// so that both their ranges are big enough to encompass every X and Y-value of every series.
ASSERT_TRUE(chart->get_AxisX()->get_Scaling()->get_Minimum()->get_IsAuto());

// We can define our own axis bounds.
// In this case, we will make both the X and Y-axis rulers show a range of 0 to 10.
chart->get_AxisX()->get_Scaling()->set_Minimum(MakeObject<AxisBound>(0.0));
chart->get_AxisX()->get_Scaling()->set_Maximum(MakeObject<AxisBound>(10.0));
chart->get_AxisY()->get_Scaling()->set_Minimum(MakeObject<AxisBound>(0.0));
chart->get_AxisY()->get_Scaling()->set_Maximum(MakeObject<AxisBound>(10.0));

ASSERT_FALSE(chart->get_AxisX()->get_Scaling()->get_Minimum()->get_IsAuto());
ASSERT_FALSE(chart->get_AxisY()->get_Scaling()->get_Minimum()->get_IsAuto());

// Create a line chart with a series requiring a range of dates on the X-axis, and decimal values for the Y-axis.
chartShape = builder->InsertChart(ChartType::Line, 450, 300);
chart = chartShape->get_Chart();
chart->get_Series()->Clear();

ArrayPtr<System::DateTime> dates =
    MakeArray<System::DateTime>({System::DateTime(1973, 5, 11), System::DateTime(1981, 2, 4), System::DateTime(1985, 9, 23),
                                 System::DateTime(1989, 6, 28), System::DateTime(1994, 12, 15)});

chart->get_Series()->Add(u"Series 1", dates, MakeArray<double>({3.0, 4.7, 5.9, 7.1, 8.9}));

// We can set axis bounds in the form of dates as well, limiting the chart to a period.
// Setting the range to 1980-1990 will omit the two of the series values
// that are outside of the range from the graph.
chart->get_AxisX()->get_Scaling()->set_Minimum(MakeObject<AxisBound>(System::DateTime(1980, 1, 1)));
chart->get_AxisX()->get_Scaling()->set_Maximum(MakeObject<AxisBound>(System::DateTime(1990, 1, 1)));

doc->Save(ArtifactsDir + u"Charts.AxisBound.docx");
```

## See Also

* Class [AxisBound](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words](../../../)
