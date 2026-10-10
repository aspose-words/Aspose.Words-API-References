---
title: "Aspose::Words::Drawing::PresetTexture enum"
linktitle: "PresetTexture"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::PresetTexture enum. Spécifie la texture à utiliser pour remplir une forme en C++."
type: docs
weight: 32000
url: /fr/cpp/aspose.words.drawing/presettexture/
---
## PresetTexture enum


Spécifie la texture à utiliser pour remplir une forme.

```cpp
enum class PresetTexture
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | -1 | Pas de texture. |
| BlueTissuePaper | 1 | Texture de papier de soie bleu. |
| Bouquet | 2 | Texture de bouquet. |
| BrownMarble | 3 | Texture de marbre brun. |
| Canvas | 4 | Texture de toile. |
| Cork | 5 | Texture de liège. |
| Denim | 6 | Texture de denim. |
| FishFossil | 7 | Texture de fossile de poisson. |
| Granite | 8 | Texture de granit. |
| GreenMarble | 9 | Texture de marbre vert. |
| MediumWood | 10 | Texture de bois moyen. |
| Newsprint | 11 | Texture de papier journal. |
| Oak | 12 | Texture de chêne. |
| PaperBag | 13 | Texture de sac en papier. |
| Papyrus | 14 | Texture de papyrus. |
| Parchment | 15 | Texture de parchemin. |
| PinkTissuePaper | 16 | Texture de papier de soie rose. |
| PurpleMesh | 17 | Texture de maille violette. |
| RecycledPaper | 18 | Texture de papier recyclé. |
| Sable | 19 | Texture de sable. |
| Papeterie | 20 | Texture de papeterie. |
| Noyer | 21 | Texture de noyer. |
| WaterDroplets | 22 | Texture de gouttelettes d'eau. |
| WhiteMarble | 23 | Texture de marbre blanc. |
| WovenMat | 24 | Texture de tapis tissé. |


## Exemples



Afficher comment définir le formatage du marqueur.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Supprimer la série générée par défaut.
chart->get_Series()->Clear();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"AW Series 1", System::MakeArray<double>({0.7, 1.8, 2.6, 3.9}), System::MakeArray<double>({2.7, 3.2, 0.8, 1.7}));

// Définir le formatage du marqueur.
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

## Voir aussi

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
