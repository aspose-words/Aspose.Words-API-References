---
title: Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize method
linktitle: get_SecondSectionSize
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize method. Gets or sets the size of the pie chart secondary section as a percentage in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words.drawing.charts/chartseriesgroup/get_secondsectionsize/
---
## ChartSeriesGroup::get_SecondSectionSize method


Gets or sets the size of the pie chart secondary section as a percentage.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize()
```

## Remarks


Applies to series groups of the [PieOfPie](../../chartseriestype/) and [PieOfBar](../../chartseriestype/) types.

The range of acceptable values is from 5 to 200 inclusive. The default value is 75.

## Examples



Shows how to create and format pie of Pie chart. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::PieOfPie, 440, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
// Delete the default generated series.
chart->get_Series()->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"});
chart->get_Series()->Add(u"Series 1", categories, System::MakeArray<double>({11, 8, 4, 3}));

// Format the Pie of Pie chart.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = chart->get_SeriesGroups()->idx_get(0);
seriesGroup->set_GapWidth(10);
seriesGroup->set_SecondSectionSize(77);

doc->Save(get_ArtifactsDir() + u"Charts.PieOfPieChart.docx");
```

## See Also

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
