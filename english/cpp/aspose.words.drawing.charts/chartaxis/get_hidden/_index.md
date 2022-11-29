---
title: get_Hidden
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a flag indicating whether this axis is hidden or not.
type: docs
weight: 92
url: /cpp/aspose.words.drawing.charts/chartaxis/get_hidden/
---
## ChartAxis::get_Hidden method


Gets or sets a flag indicating whether this axis is hidden or not.

```cpp
bool Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden()
```


## Examples



Shows how to hide chart axes. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> shape = builder->InsertChart(ChartType::Line, 500, 300);
SharedPtr<Chart> chart = shape->get_Chart();

// Clear the chart's demo data series to start with a clean chart.
chart->get_Series()->Clear();

// Add a custom series with categories for the X-axis, and respective decimal values for the Y-axis.
chart->get_Series()->Add(u"AW Series 1", MakeArray<String>({u"Item 1", u"Item 2", u"Item 3", u"Item 4", u"Item 5"}),
                         MakeArray<double>({1.2, 0.3, 2.1, 2.9, 4.2}));

// Hide the chart axes to simplify the appearance of the chart.
chart->get_AxisX()->set_Hidden(true);
chart->get_AxisY()->set_Hidden(true);

doc->Save(ArtifactsDir + u"Charts.HideChartAxis.docx");
```

## See Also

* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words](../../../)
