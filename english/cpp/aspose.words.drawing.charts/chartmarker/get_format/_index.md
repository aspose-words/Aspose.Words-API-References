---
title: Aspose::Words::Drawing::Charts::ChartMarker::get_Format method
linktitle: get_Format
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartMarker::get_Format method. Provides access to fill and line formatting of this marker in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.drawing.charts/chartmarker/get_format/
---
## ChartMarker::get_Format method


Provides access to fill and line formatting of this marker.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartFormat> Aspose::Words::Drawing::Charts::ChartMarker::get_Format()
```


## Examples



Show how to set marker formatting. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Delete default generated series.
chart->get_Series()->Clear();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"AW Series 1", System::MakeArray<double>({0.7, 1.8, 2.6, 3.9}), System::MakeArray<double>({2.7, 3.2, 0.8, 1.7}));

// Set marker formatting.
series->get_Marker()->set_Size(40);
series->get_Marker()->set_Symbol(Aspose::Words::Drawing::Charts::MarkerSymbol::Square);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPointCollection> dataPoints = series->get_DataPoints();
dataPoints->idx_get(0)->get_Marker()->get_Format()->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::Denim);
dataPoints->idx_get(0)->get_Marker()->get_Format()->get_Stroke()->set_ForeColor(System::Drawing::Color::get_Yellow());
dataPoints->idx_get(0)->get_Marker()->get_Format()->get_Stroke()->set_BackColor(System::Drawing::Color::get_Red());
dataPoints->idx_get(1)->get_Marker()->get_Format()->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::WaterDroplets);
dataPoints->idx_get(1)->get_Marker()->get_Format()->get_Stroke()->set_ForeColor(System::Drawing::Color::get_Yellow());
dataPoints->idx_get(1)->get_Marker()->get_Format()->get_Stroke()->set_Visible(false);
dataPoints->idx_get(2)->get_Marker()->get_Format()->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::GreenMarble);
dataPoints->idx_get(2)->get_Marker()->get_Format()->get_Stroke()->set_ForeColor(System::Drawing::Color::get_Yellow());
dataPoints->idx_get(3)->get_Marker()->get_Format()->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::Oak);
dataPoints->idx_get(3)->get_Marker()->get_Format()->get_Stroke()->set_ForeColor(System::Drawing::Color::get_Yellow());
dataPoints->idx_get(3)->get_Marker()->get_Format()->get_Stroke()->set_Transparency(0.5);

doc->Save(get_ArtifactsDir() + u"Charts.MarkerFormatting.docx");
```

## See Also

* Class [ChartFormat](../../chartformat/)
* Class [ChartMarker](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
