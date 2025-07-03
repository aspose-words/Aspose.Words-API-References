---
title: Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale method
linktitle: get_BubbleScale
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale method. Gets or sets the size of the bubbles as a percentage of their default size in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.drawing.charts/chartseriesgroup/get_bubblescale/
---
## ChartSeriesGroup::get_BubbleScale method


Gets or sets the size of the bubbles as a percentage of their default size.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale()
```

## Remarks


Applies only to series groups of the [Bubble](../../chartseriestype/) and [Bubble3D](../../chartseriestype/) types.

The range of acceptable values is from 0 to 300 inclusive. The default value is 100.

## Examples



Show how to set size of the bubbles. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a bubble 3D chart.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble3D, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = shape->get_Chart()->get_SeriesGroups()->idx_get(0);

// Set bubble scale to 200%.
seriesGroup->set_BubbleScale(200);

doc->Save(get_ArtifactsDir() + u"Charts.BubbleScale.docx");
```

## See Also

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
