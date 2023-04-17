---
title: Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLegendKey method
linktitle: get_ShowLegendKey
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLegendKey method. Allows to specify whether legend key is to be displayed for the data labels of the entire series. Default value is false in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_showlegendkey/
---
## ChartDataLabelCollection::get_ShowLegendKey method


Allows to specify whether legend key is to be displayed for the data labels of the entire series. Default value is **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLegendKey()
```


## Examples



Shows how to work with data labels of a pie chart. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Chart> chart = builder->InsertChart(ChartType::Pie, 500, 300)->get_Chart();

// Clear the chart's demo data series to start with a clean chart.
chart->get_Series()->Clear();

// Insert a custom chart series with a category name for each of the sectors, and their frequency table.
SharedPtr<ChartSeries> series =
    chart->get_Series()->Add(u"Aspose Test Series", MakeArray<String>({u"Word", u"PDF", u"Excel"}), MakeArray<double>({2.7, 3.2, 0.8}));

// Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
series->set_HasDataLabels(true);
SharedPtr<ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowLeaderLines(true);
dataLabels->set_ShowLegendKey(true);
dataLabels->set_ShowPercentage(true);
dataLabels->set_ShowValue(true);
dataLabels->set_Separator(u"; ");

doc->Save(ArtifactsDir + u"Charts.DataLabelsPieChart.docx");
```

## See Also

* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
