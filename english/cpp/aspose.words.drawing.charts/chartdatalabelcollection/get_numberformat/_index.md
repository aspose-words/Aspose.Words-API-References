---
title: get_NumberFormat
second_title: Aspose.Words for C++ API Reference
description: Gets an ChartNumberFormat instance allowing to set number format for the data labels of the entire series.
type: docs
weight: 53
url: /cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_numberformat/
---
## ChartDataLabelCollection::get_NumberFormat method


Gets an [ChartNumberFormat](../../chartnumberformat/) instance allowing to set number format for the data labels of the entire series.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartNumberFormat> Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_NumberFormat()
```


## Examples



Shows how to enable and configure data labels for a chart series. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Add a line chart, then clear its demo data series to start with a clean chart,
// and then set a title.
SharedPtr<Shape> shape = builder->InsertChart(ChartType::Line, 500, 300);
SharedPtr<Chart> chart = shape->get_Chart();
chart->get_Series()->Clear();
chart->get_Title()->set_Text(u"Monthly sales report");

// Insert a custom chart series with months as categories for the X-axis,
// and respective decimal amounts for the Y-axis.
SharedPtr<ChartSeries> series =
    chart->get_Series()->Add(u"Revenue", MakeArray<String>({u"January", u"February", u"March"}), MakeArray<double>({25.611, 21.439, 33.750}));

// Enable data labels, and then apply a custom number format for values displayed in the data labels.
// This format will treat displayed decimal values as millions of US Dollars.
series->set_HasDataLabels(true);
SharedPtr<ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->get_NumberFormat()->set_FormatCode(u"\"US$\" #,##0.000\"M\"");

doc->Save(ArtifactsDir + u"Charts.DataLabelNumberFormat.docx");
```

## See Also

* Class [ChartNumberFormat](../../chartnumberformat/)
* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words](../../../)
