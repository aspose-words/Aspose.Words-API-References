---
title: "Méthode Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale"
linktitle: "get_BubbleScale"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale. Obtient ou définit la taille des bulles en pourcentage de leur taille par défaut en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.drawing.charts/chartseriesgroup/get_bubblescale/
---
## ChartSeriesGroup::get_BubbleScale method


Obtient ou définit la taille des bulles en pourcentage de leur taille par défaut.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale()
```

## Remarques


S'applique uniquement aux groupes de séries des types [Bubble](../../chartseriestype/) et [Bubble3D](../../chartseriestype/).

L'intervalle des valeurs acceptables va de 0 à 300 inclus. La valeur par défaut est 100.

## Exemples



Montrez comment définir la taille des bulles.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez un graphique à bulles 3D.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble3D, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = shape->get_Chart()->get_SeriesGroups()->idx_get(0);

// Définissez l'échelle des bulles à 200 %.
seriesGroup->set_BubbleScale(200);

doc->Save(get_ArtifactsDir() + u"Charts.BubbleScale.docx");
```

## Voir aussi

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
