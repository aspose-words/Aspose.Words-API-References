---
title: Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap method
linktitle: get_Overlap
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap method. Gets or sets the percentage of how much the series bars or columns overlap in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.drawing.charts/chartseriesgroup/get_overlap/
---
## ChartSeriesGroup::get_Overlap method


Gets or sets the percentage of how much the series bars or columns overlap.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap()
```

## Remarks


Applies to series groups of all bar and column types.

The range of acceptable values is from -100 to 100 inclusive. A value of 0 indicates that there is no space between bars/columns. If the value is -100, the distance between bars/columns is equal to their width. A value of 100 means that the bars/columns overlap completely.

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
