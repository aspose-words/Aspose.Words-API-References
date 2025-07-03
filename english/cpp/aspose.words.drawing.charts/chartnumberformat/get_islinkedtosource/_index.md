---
title: Aspose::Words::Drawing::Charts::ChartNumberFormat::get_IsLinkedToSource method
linktitle: get_IsLinkedToSource
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartNumberFormat::get_IsLinkedToSource method. Specifies whether the format code is linked to a source cell. Default is true in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.drawing.charts/chartnumberformat/get_islinkedtosource/
---
## ChartNumberFormat::get_IsLinkedToSource method


Specifies whether the format code is linked to a source cell. Default is true.

```cpp
bool Aspose::Words::Drawing::Charts::ChartNumberFormat::get_IsLinkedToSource()
```


## Examples



Shows how to set formatting for chart values. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Clear the chart's demo data series to start with a clean chart.
chart->get_Series()->Clear();

// Add a custom series to the chart with categories for the X-axis,
// and large respective numeric values for the Y-axis.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel", u"GoogleDocs", u"Note"}), System::MakeArray<double>({1900000, 850000, 2100000, 600000, 1500000}));

// Set the number format of the Y-axis tick labels to not group digits with commas.
chart->get_AxisY()->get_NumberFormat()->set_FormatCode(u"#,##0");

// This flag can override the above value and draw the number format from the source cell.
ASSERT_FALSE(chart->get_AxisY()->get_NumberFormat()->get_IsLinkedToSource());

doc->Save(get_ArtifactsDir() + u"Charts.SetNumberFormatToChartAxis.docx");
```

## See Also

* Class [ChartNumberFormat](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
