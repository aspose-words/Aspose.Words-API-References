---
title: Aspose::Words::Drawing::PresetTexture enum
linktitle: PresetTexture
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::PresetTexture enum. Specifies texture to be used to fill a shape in C++.'
type: docs
weight: 32000
url: /cpp/aspose.words.drawing/presettexture/
---
## PresetTexture enum


Specifies texture to be used to fill a shape.

```cpp
enum class PresetTexture
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | -1 | No Texture. |
| BlueTissuePaper | 1 | Blue tissue paper texture. |
| Bouquet | 2 | Bouquet texture. |
| BrownMarble | 3 | Brown marble texture. |
| Canvas | 4 | Canvas texture. |
| Cork | 5 | Cork texture. |
| Denim | 6 | Denim texture. |
| FishFossil | 7 | Fish fossil texture. |
| Granite | 8 | Granite texture. |
| GreenMarble | 9 | Green marble texture. |
| MediumWood | 10 | Medium wood texture. |
| Newsprint | 11 | Newsprint texture. |
| Oak | 12 | Oak texture. |
| PaperBag | 13 | Paper bag texture. |
| Papyrus | 14 | Papyrus texture. |
| Parchment | 15 | Parchment texture. |
| PinkTissuePaper | 16 | Pink tissue paper texture. |
| PurpleMesh | 17 | Purple mesh texture. |
| RecycledPaper | 18 | Recycled paper texture. |
| Sand | 19 | Sand texture. |
| Stationery | 20 | Stationery texture. |
| Walnut | 21 | Walnut texture. |
| WaterDroplets | 22 | Water droplets texture. |
| WhiteMarble | 23 | White marble texture. |
| WovenMat | 24 | Woven mat texture. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
