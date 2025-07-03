---
title: Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle method
linktitle: get_FirstSliceAngle
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle method. Gets or sets the angle, in degrees, of the first slice of the parent pie chart in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.drawing.charts/chartseriesgroup/get_firstsliceangle/
---
## ChartSeriesGroup::get_FirstSliceAngle method


Gets or sets the angle, in degrees, of the first slice of the parent pie chart.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle()
```

## Remarks


Applies to series groups of the [Pie](../../chartseriestype/), [Pie3D](../../chartseriestype/) and [Doughnut](../../chartseriestype/) types.

The range of acceptable values is from 0 to 360 inclusive. The default value is 0.

## Examples



Shows how to create and format Doughnut chart. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Doughnut, 400, 400);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
// Delete the default generated series.
chart->get_Series()->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"});
chart->get_Series()->Add(u"Series 1", categories, System::MakeArray<double>({4, 2, 5}));

// Format the Doughnut chart.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = chart->get_SeriesGroups()->idx_get(0);
seriesGroup->set_DoughnutHoleSize(10);
seriesGroup->set_FirstSliceAngle(270);

doc->Save(get_ArtifactsDir() + u"Charts.DoughnutChart.docx");
```

## See Also

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
