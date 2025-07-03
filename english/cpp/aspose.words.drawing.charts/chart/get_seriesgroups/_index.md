---
title: Aspose::Words::Drawing::Charts::Chart::get_SeriesGroups method
linktitle: get_SeriesGroups
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::Chart::get_SeriesGroups method. Provides access to a series group collection of this chart in C++.'
type: docs
weight: 6500
url: /cpp/aspose.words.drawing.charts/chart/get_seriesgroups/
---
## Chart::get_SeriesGroups method


Provides access to a series group collection of this chart.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection> Aspose::Words::Drawing::Charts::Chart::get_SeriesGroups()
```


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

* Class [ChartSeriesGroupCollection](../../chartseriesgroupcollection/)
* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
