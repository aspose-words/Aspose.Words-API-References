---
title: Aspose::Words::Drawing::Charts::ChartDataLabelPosition enum
linktitle: ChartDataLabelPosition
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartDataLabelPosition enum. Specifies the position for a chart data label in C++.'
type: docs
weight: 27334
url: /cpp/aspose.words.drawing.charts/chartdatalabelposition/
---
## ChartDataLabelPosition enum


Specifies the position for a chart data label.

```cpp
enum class ChartDataLabelPosition
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Center | 0 | Specifies that a data label should be displayed centered on a data marker. |
| Left | 1 | Specifies that a data label should be displayed to the left of a data marker. |
| Right | 2 | Specifies that a data label should be displayed to the right of a data marker. |
| Above | 3 | Specifies that a data label should be displayed above a data marker. |
| Below | 4 | Specifies that a data label should be displayed below a data marker. |
| InsideBase | 5 | Specifies that a data label should be displayed inside the base of a data marker. |
| InsideEnd | 6 | Specifies that a data label should be displayed inside the end of a data marker. |
| OutsideEnd | 7 | Specifies that a data label should be displayed outside the end of a data marker. |
| BestFit | 8 | Specifies that a data label should be displayed in the most appropriate position. |


## Examples



Shows how to set the position of the data label. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert column chart.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();

// Delete default generated series.
seriesColl->Clear();

// Add series.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = seriesColl->Add(u"Series 1", System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"}), System::MakeArray<double>({4, 5, 6}));

// Show data labels and set font color.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->get_Font()->set_Color(System::Drawing::Color::get_White());

// Set data label position.
dataLabels->set_Position(Aspose::Words::Drawing::Charts::ChartDataLabelPosition::InsideBase);
dataLabels->idx_get(0)->set_Position(Aspose::Words::Drawing::Charts::ChartDataLabelPosition::OutsideEnd);
dataLabels->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_DarkRed());

doc->Save(get_ArtifactsDir() + u"Charts.LabelPosition.docx");
```

## See Also

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
