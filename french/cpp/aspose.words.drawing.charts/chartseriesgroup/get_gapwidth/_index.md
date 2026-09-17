---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth méthode"
linktitle: "get_GapWidth"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth méthode. Obtient ou définit le pourcentage de largeur d'écart entre les éléments du diagramme en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.drawing.charts/chartseriesgroup/get_gapwidth/
---
## ChartSeriesGroup::get_GapWidth method


Obtient ou définit le pourcentage de l'écart de largeur entre les éléments du graphique.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth()
```

## Remarques


S'applique uniquement aux groupes de séries des types barre, colonne, secteur‑de‑barre, secteur‑de‑secteur, histogramme, boîte & moustaches, cascade et entonnoir.

L'intervalle des valeurs acceptables va de 0 à 500 inclus. Pour les groupes de séries basés sur des barres/colonnes, la propriété représente l'espace entre les groupes de barres en pourcentage de leur largeur. Pour les graphiques secteur‑de‑secteur et secteur‑de‑barre, il s'agit de l'espace entre les sections principale et secondaire du graphique.

## Exemples



Montrez comment configurer la largeur d'écart et le chevauchement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = shape->get_Chart()->get_SeriesGroups()->idx_get(0);

// Définissez la largeur d'écart des colonnes et le chevauchement.
seriesGroup->set_GapWidth(450);
seriesGroup->set_Overlap(-75);

doc->Save(get_ArtifactsDir() + u"Charts.ConfigureGapOverlap.docx");
```

## Voir aussi

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
