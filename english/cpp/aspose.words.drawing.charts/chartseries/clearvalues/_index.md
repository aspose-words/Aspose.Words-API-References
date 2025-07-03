---
title: Aspose::Words::Drawing::Charts::ChartSeries::ClearValues method
linktitle: ClearValues
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartSeries::ClearValues method. Removes all data values from the chart series with preserving the format of the data points and data labels in C++.'
type: docs
weight: 1750
url: /cpp/aspose.words.drawing.charts/chartseries/clearvalues/
---
## ChartSeries::ClearValues method


Removes all data values from the chart series with preserving the format of the data points and data labels.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::ClearValues()
```


## Examples



Shows how to populate chart series with data. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// Clear X and Y values of the first series.
series1->ClearValues();

// Populate the series with data.
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(5), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(5));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(7), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(11));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(9));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series2 = chart->get_Series()->idx_get(1);
// Clear X and Y values of the second series.
series2->Clear();

// Populate the series with data.
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(2), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(4));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(4), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(6), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(14));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(8), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## See Also

* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
