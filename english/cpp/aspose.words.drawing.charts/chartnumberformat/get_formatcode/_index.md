---
title: get_FormatCode
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the format code applied to a data label.
type: docs
weight: 14
url: /cpp/aspose.words.drawing.charts/chartnumberformat/get_formatcode/
---
## ChartNumberFormat::get_FormatCode method


Gets or sets the format code applied to a data label.

```cpp
System::String Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode()
```

## Remarks


Number formatting is used to change the way a value appears in data label and can be used in some very creative ways. The examples of number formats:

Number - "#,##0.00"

Currency - "\"\$\\"#,##0.00"

Time - "[$-x-systime]h:mm:ss AM/PM"

Date - "d/mm/yyyy"

Percentage - "0.00%"

Fraction - "# ?/?"

Scientific - "0.00E+00"

Text - "@"

Accounting - "_-\"\$\\"* #,##0.00_-;-\"\$\\"* #,##0.00_-;_-\"\$\\"* \"-\\"??_-;_-@_-"

Custom with color - "[Red]-#,##0.0"

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


Shows how to set formatting for chart values. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> shape = builder->InsertChart(ChartType::Column, 500, 300);
SharedPtr<Chart> chart = shape->get_Chart();

// Clear the chart's demo data series to start with a clean chart.
chart->get_Series()->Clear();

// Add a custom series to the chart with categories for the X-axis,
// and large respective numeric values for the Y-axis.
chart->get_Series()->Add(u"Aspose Test Series", MakeArray<String>({u"Word", u"PDF", u"Excel", u"GoogleDocs", u"Note"}),
                         MakeArray<double>({1900000, 850000, 2100000, 600000, 1500000}));

// Set the number format of the Y-axis tick labels to not group digits with commas.
chart->get_AxisY()->get_NumberFormat()->set_FormatCode(u"#,##0");

// This flag can override the above value and draw the number format from the source cell.
ASSERT_FALSE(chart->get_AxisY()->get_NumberFormat()->get_IsLinkedToSource());

doc->Save(ArtifactsDir + u"Charts.SetNumberFormatToChartAxis.docx");
```

## See Also

* Class [ChartNumberFormat](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words](../../../)
