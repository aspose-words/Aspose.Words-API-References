---
title: "Méthode Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap"
linktitle: "get_Overlap"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap. Obtient ou définit le pourcentage de chevauchement des barres ou colonnes de séries en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.drawing.charts/chartseriesgroup/get_overlap/
---
## ChartSeriesGroup::get_Overlap method


Obtient ou définit le pourcentage de chevauchement des barres ou colonnes de la série.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap()
```

## Remarques


S'applique aux groupes de séries de tous les types de barres et de colonnes.

La plage de valeurs acceptables va de -100 à 100 inclusive. Une valeur de 0 indique qu'il n'y a aucun espace entre les barres/colonnes. Si la valeur est -100, la distance entre les barres/colonnes est égale à leur largeur. Une valeur de 100 signifie que les barres/colonnes se chevauchent complètement.

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
