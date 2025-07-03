---
title: Aspose::Words::Drawing::Charts::ChartSeriesGroup class
linktitle: ChartSeriesGroup
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartSeriesGroup class. Represents properties of a chart series group, that is, the properties of chart series of the same type associated with the same axes in C++.'
type: docs
weight: 17334
url: /cpp/aspose.words.drawing.charts/chartseriesgroup/
---
## ChartSeriesGroup class


Represents properties of a chart series group, that is, the properties of chart series of the same type associated with the same axes.

```cpp
class ChartSeriesGroup : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_AxisGroup](./get_axisgroup/)() | Gets or sets the axis group to which this series group belongs. |
| [get_AxisX](./get_axisx/)() | Provides access to properties of the X axis of this series group. |
| [get_AxisY](./get_axisy/)() | Provides access to properties of the Y axis of this series group. |
| [get_BubbleScale](./get_bubblescale/)() | Gets or sets the size of the bubbles as a percentage of their default size. |
| [get_DoughnutHoleSize](./get_doughnutholesize/)() | Gets or sets the hole size of the parent doughnut chart as a percentage. |
| [get_FirstSliceAngle](./get_firstsliceangle/)() | Gets or sets the angle, in degrees, of the first slice of the parent pie chart. |
| [get_GapWidth](./get_gapwidth/)() | Gets or sets the percentage of gap width between chart elements. |
| [get_Overlap](./get_overlap/)() | Gets or sets the percentage of how much the series bars or columns overlap. |
| [get_SecondSectionSize](./get_secondsectionsize/)() | Gets or sets the size of the pie chart secondary section as a percentage. |
| [get_Series](./get_series/)() | Gets a collection of series that belong to this series group. |
| [get_SeriesType](./get_seriestype/)() | Gets the type of chart series included in this group. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AxisGroup](./set_axisgroup/)(Aspose::Words::Drawing::Charts::AxisGroup) | Setter for [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_AxisGroup](./get_axisgroup/). |
| [set_BubbleScale](./set_bubblescale/)(int32_t) | Setter for [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale](./get_bubblescale/). |
| [set_DoughnutHoleSize](./set_doughnutholesize/)(int32_t) | Setter for [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_DoughnutHoleSize](./get_doughnutholesize/). |
| [set_FirstSliceAngle](./set_firstsliceangle/)(int32_t) | Setter for [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle](./get_firstsliceangle/). |
| [set_GapWidth](./set_gapwidth/)(int32_t) | Setter for [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth](./get_gapwidth/). |
| [set_Overlap](./set_overlap/)(int32_t) | Setter for [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap](./get_overlap/). |
| [set_SecondSectionSize](./set_secondsectionsize/)(int32_t) | Setter for [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize](./get_secondsectionsize/). |
| static [Type](./type/)() |  |
## Remarks


Combo charts contains multiple chart series groups, with a separate group for each series type.

Also, you can create a chart series group to assign secondary axes to one or more chart series.

To learn more, visit the [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) documentation article.

## Examples



Shows how to work with the secondary axis of chart. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();

// Delete default generated series.
series->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"});
series->Add(u"Series 1 of primary series group", categories, System::MakeArray<double>({2, 3, 4}));
series->Add(u"Series 2 of primary series group", categories, System::MakeArray<double>({5, 2, 3}));

// Create an additional series group, also of the line type.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> newSeriesGroup = chart->get_SeriesGroups()->Add(Aspose::Words::Drawing::Charts::ChartSeriesType::Line);
// Specify the use of secondary axes for the new series group.
newSeriesGroup->set_AxisGroup(Aspose::Words::Drawing::Charts::AxisGroup::Secondary);
// Hide the secondary X axis.
newSeriesGroup->get_AxisX()->set_Hidden(true);
// Define title of the secondary Y axis.
newSeriesGroup->get_AxisY()->get_Title()->set_Show(true);
newSeriesGroup->get_AxisY()->get_Title()->set_Text(u"Secondary Y axis");

ASSERT_EQ(Aspose::Words::Drawing::Charts::ChartSeriesType::Line, newSeriesGroup->get_SeriesType());

// Add a series to the new series group.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series3 = newSeriesGroup->get_Series()->Add(u"Series of secondary series group", categories, System::MakeArray<double>({13, 11, 16}));
series3->get_Format()->get_Stroke()->set_Weight(3.5);

doc->Save(get_ArtifactsDir() + u"Charts.SecondaryAxis.docx");
```

## See Also

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
