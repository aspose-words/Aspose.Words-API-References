---
title: Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth method
linktitle: get_GapWidth
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth method. Gets or sets the percentage of gap width between chart elements in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.drawing.charts/chartseriesgroup/get_gapwidth/
---
## ChartSeriesGroup::get_GapWidth method


Gets or sets the percentage of gap width between chart elements.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth()
```

## Remarks


Applies only to series groups of the bar, column, pie-of-bar, pie-of-pie, histogram, box&whisker, waterfall and funnel types.

The range of acceptable values is from 0 to 500 inclusive. For bar/column-based series groups, the property represents the space between bar clusters as a percentage of their width. For pie-of-pie and bar-of-pie charts, this is the space between the primary and secondary sections of the chart.

## Examples



Show how to configure gap width and overlap. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = shape->get_Chart()->get_SeriesGroups()->idx_get(0);

// Set column gap width and overlap.
seriesGroup->set_GapWidth(450);
seriesGroup->set_Overlap(-75);

doc->Save(get_ArtifactsDir() + u"Charts.ConfigureGapOverlap.docx");
```

## See Also

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
