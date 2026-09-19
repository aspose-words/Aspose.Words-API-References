---
title: "Aspose::Words::Drawing::PresetTexture enum"
linktitle: "PresetTexture"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::PresetTexture enum. Specifica la texture da utilizzare per riempire una forma in C++."
type: docs
weight: 32000
url: /it/cpp/aspose.words.drawing/presettexture/
---
## PresetTexture enum


Specifica la texture da utilizzare per riempire una forma.

```cpp
enum class PresetTexture
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | -1 | Nessuna texture. |
| BlueTissuePaper | 1 | Texture di carta tissue blu. |
| Bouquet | 2 | Texture bouquet. |
| BrownMarble | 3 | Texture di marmo marrone. |
| Canvas | 4 | Texture di tela. |
| Cork | 5 | Texture di sughero. |
| Denim | 6 | Texture di denim. |
| FishFossil | 7 | Texture di fossile di pesce. |
| Granite | 8 | Texture di granito. |
| GreenMarble | 9 | Texture di marmo verde. |
| MediumWood | 10 | Texture di legno medio. |
| Newsprint | 11 | Texture di carta da giornale. |
| Oak | 12 | Texture di quercia. |
| PaperBag | 13 | Texture di sacchetto di carta. |
| Papyrus | 14 | Texture di papiro. |
| Parchment | 15 | Texture di pergamena. |
| PinkTissuePaper | 16 | Texture di carta di stoffa rosa. |
| PurpleMesh | 17 | Texture a rete viola. |
| RecycledPaper | 18 | Texture di carta riciclata. |
| Sabbia | 19 | Texture di sabbia. |
| Cartoleria | 20 | Texture di cartoleria. |
| Noce | 21 | Texture di noce. |
| WaterDroplets | 22 | Texture di gocce d'acqua. |
| WhiteMarble | 23 | Texture di marmo bianco. |
| WovenMat | 24 | Texture di tappetino intrecciato. |


## Esempi



Mostra come impostare la formattazione del marcatore.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Elimina la serie generata di default.
chart->get_Series()->Clear();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"AW Series 1", System::MakeArray<double>({0.7, 1.8, 2.6, 3.9}), System::MakeArray<double>({2.7, 3.2, 0.8, 1.7}));

// Imposta la formattazione del marcatore.
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

## Vedi anche

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
