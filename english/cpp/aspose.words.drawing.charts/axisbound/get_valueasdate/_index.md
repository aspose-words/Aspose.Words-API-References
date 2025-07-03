---
title: Aspose::Words::Drawing::Charts::AxisBound::get_ValueAsDate method
linktitle: get_ValueAsDate
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::AxisBound::get_ValueAsDate method. Returns value of axis bound represented as datetime in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.drawing.charts/axisbound/get_valueasdate/
---
## AxisBound::get_ValueAsDate method


Returns value of axis bound represented as datetime.

```cpp
System::DateTime Aspose::Words::Drawing::Charts::AxisBound::get_ValueAsDate()
```


## Examples



Shows how to set custom axis bounds. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Clear the chart's demo data series to start with a clean chart.
chart->get_Series()->Clear();

// Add a series with two decimal arrays. The first array contains the X-values,
// and the second contains corresponding Y-values for points in the scatter chart.
chart->get_Series()->Add(u"Series 1", System::MakeArray<double>({1.1, 5.4, 7.9, 3.5, 2.1, 9.7}), System::MakeArray<double>({2.1, 0.3, 0.6, 3.3, 1.4, 1.9}));

// By default, default scaling is applied to the graph's X and Y-axes,
// so that both their ranges are big enough to encompass every X and Y-value of every series.
ASSERT_TRUE(chart->get_AxisX()->get_Scaling()->get_Minimum()->get_IsAuto());

// We can define our own axis bounds.
// In this case, we will make both the X and Y-axis rulers show a range of 0 to 10.
chart->get_AxisX()->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(0.0));
chart->get_AxisX()->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(10.0));
chart->get_AxisY()->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(0.0));
chart->get_AxisY()->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(10.0));

ASSERT_FALSE(chart->get_AxisX()->get_Scaling()->get_Minimum()->get_IsAuto());
ASSERT_FALSE(chart->get_AxisY()->get_Scaling()->get_Minimum()->get_IsAuto());

// Create a line chart with a series requiring a range of dates on the X-axis, and decimal values for the Y-axis.
chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 300);
chart = chartShape->get_Chart();
chart->get_Series()->Clear();

System::ArrayPtr<System::DateTime> dates = System::MakeArray<System::DateTime>({System::DateTime(1973, 5, 11), System::DateTime(1981, 2, 4), System::DateTime(1985, 9, 23), System::DateTime(1989, 6, 28), System::DateTime(1994, 12, 15)});

chart->get_Series()->Add(u"Series 1", dates, System::MakeArray<double>({3.0, 4.7, 5.9, 7.1, 8.9}));

// We can set axis bounds in the form of dates as well, limiting the chart to a period.
// Setting the range to 1980-1990 will omit the two of the series values
// that are outside of the range from the graph.
chart->get_AxisX()->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(1980, 1, 1)));
chart->get_AxisX()->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(1990, 1, 1)));

doc->Save(get_ArtifactsDir() + u"Charts.AxisBound.docx");
```

## See Also

* Class [AxisBound](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
