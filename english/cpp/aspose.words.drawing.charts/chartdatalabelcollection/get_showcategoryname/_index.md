---
title: Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowCategoryName method
linktitle: get_ShowCategoryName
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowCategoryName method. Allows to specify whether category name is to be displayed for the data labels of the entire series. Default value is false in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_showcategoryname/
---
## ChartDataLabelCollection::get_ShowCategoryName method


Allows to specify whether category name is to be displayed for the data labels of the entire series. Default value is **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowCategoryName()
```


## Examples



Shows how to work with data labels of a bubble chart. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Chart> chart = builder->InsertChart(ChartType::Bubble, 500, 300)->get_Chart();

// Clear the chart's demo data series to start with a clean chart.
chart->get_Series()->Clear();

// Add a custom series with X/Y coordinates and diameter of each of the bubbles.
SharedPtr<ChartSeries> series = chart->get_Series()->Add(u"Aspose Test Series", MakeArray<double>({2.9, 3.5, 1.1, 4.0, 4.0}),
                                                         MakeArray<double>({1.9, 8.5, 2.1, 6.0, 1.5}), MakeArray<double>({9.0, 4.5, 2.5, 8.0, 5.0}));

// Enable data labels, and then modify their appearance.
series->set_HasDataLabels(true);
SharedPtr<ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowBubbleSize(true);
dataLabels->set_ShowCategoryName(true);
dataLabels->set_ShowSeriesName(true);
dataLabels->set_Separator(u" & ");

doc->Save(ArtifactsDir + u"Charts.DataLabelsBubbleChart.docx");
```

## See Also

* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
