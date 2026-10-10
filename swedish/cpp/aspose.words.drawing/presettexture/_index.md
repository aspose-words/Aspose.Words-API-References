---
title: "Aspose::Words::Drawing::PresetTexture enum"
linktitle: "PresetTexture"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::PresetTexture enum. Anger textur som ska användas för att fylla en form i C++."
type: docs
weight: 32000
url: /sv/cpp/aspose.words.drawing/presettexture/
---
## PresetTexture enum


Anger textur som ska användas för att fylla en form.

```cpp
enum class PresetTexture
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | -1 | Ingen textur. |
| BlueTissuePaper | 1 | Blå tissuepapperstextur. |
| Bouquet | 2 | Bouquet-textur. |
| BrownMarble | 3 | Brun marmortextur. |
| Canvas | 4 | Canvas-textur. |
| Kork | 5 | Korktextur. |
| Denim | 6 | Denimtextur. |
| FishFossil | 7 | Fiskfossiltextur. |
| Granit | 8 | Granittextur. |
| GreenMarble | 9 | Grön marmortextur. |
| MediumWood | 10 | Medium trätextur. |
| Tidningspapper | 11 | Tidningspappers-textur. |
| Ek | 12 | Ektextur. |
| PaperBag | 13 | Papperspåsetextur. |
| Papyrus | 14 | Papyrustextur. |
| Pergament | 15 | Pergamenttextur. |
| PinkTissuePaper | 16 | Rosa pappersservetttextur. |
| PurpleMesh | 17 | Lila nättextur. |
| RecycledPaper | 18 | Återvunnen papperstextur. |
| Sand | 19 | Sandtextur. |
| Kontorsmaterial | 20 | Kontorsmaterialstextur. |
| Valnöt | 21 | Valnötstextur. |
| WaterDroplets | 22 | Vattendroppstextur. |
| WhiteMarble | 23 | Vit marmortextur. |
| WovenMat | 24 | Vävd mattextur. |


## Exempel



Visa hur man ställer in markörformatering.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Ta bort standardgenererad serie.
chart->get_Series()->Clear();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"AW Series 1", System::MakeArray<double>({0.7, 1.8, 2.6, 3.9}), System::MakeArray<double>({2.7, 3.2, 0.8, 1.7}));

// Ställ in markörformatering.
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

## Se även

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
