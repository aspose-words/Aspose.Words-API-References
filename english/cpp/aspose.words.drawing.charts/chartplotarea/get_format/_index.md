---
title: Aspose::Words::Drawing::Charts::ChartPlotArea::get_Format method
linktitle: get_Format
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartPlotArea::get_Format method. Provides access to fill and line formatting of the plot area in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words.drawing.charts/chartplotarea/get_format/
---
## ChartPlotArea::get_Format method


Provides access to fill and line formatting of the plot area.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartFormat> Aspose::Words::Drawing::Charts::ChartPlotArea::get_Format()
```

## Examples


Shows how to set fill and line formatting for the plot area of a chart.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(ChartType::Column, static_cast<double>(432), static_cast<double>(252));
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Delete default generated series and add our own.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();
seriesColl->Clear();
auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2"});
seriesColl->Add(u"Series 1", categories, System::MakeArray<double>({1, 2}));
seriesColl->Add(u"Series 2", categories, System::MakeArray<double>({3, 4}));

// Fill the plot area with a gradient and outline it with a thin blue line.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartPlotArea> plotArea = chart->get_PlotArea();
plotArea->get_Format()->get_Fill()->OneColorGradient(System::Drawing::Color::get_LightBlue(), GradientStyle::DiagonalUp, GradientVariant::Variant2, static_cast<double>(1));
plotArea->get_Format()->get_Stroke()->set_ForeColor(System::Drawing::Color::get_Blue());
plotArea->get_Format()->get_Stroke()->set_Weight(0.25);

doc->Save(get_ArtifactsDir() + u"Charts.PlotAreaFormat.docx");
```
## See Also

* Class [ChartFormat](../../chartformat/)
* Class [ChartPlotArea](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
