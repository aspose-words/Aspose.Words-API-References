---
title: ChartNumberFormat
second_title: Aspose.Words for C++ API Reference
description: Represents number formatting of the parent element.
type: docs
weight: 183
url: /cpp/aspose.words.drawing.charts/chartnumberformat/
---
## ChartNumberFormat class


Represents number formatting of the parent element.

```cpp
class ChartNumberFormat : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_FormatCode](./get_formatcode/)() | Gets or sets the format code applied to a data label. |
| [get_IsLinkedToSource](./get_islinkedtosource/)() | Specifies whether the format code is linked to a source cell. Default is true. |
| [set_FormatCode](./set_formatcode/)(const System::String\&) | Setter for [Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode](./get_formatcode/). |
| [set_IsLinkedToSource](./set_islinkedtosource/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartNumberFormat::get_IsLinkedToSource](./get_islinkedtosource/). |

## Examples




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

