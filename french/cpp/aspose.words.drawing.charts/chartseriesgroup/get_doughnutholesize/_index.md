---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_DoughnutHoleSize méthode"
linktitle: "get_DoughnutHoleSize"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_DoughnutHoleSize méthode. Obtient ou définit la taille du trou du diagramme doughnut parent en pourcentage en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.drawing.charts/chartseriesgroup/get_doughnutholesize/
---
## ChartSeriesGroup::get_DoughnutHoleSize method


Obtient ou définit la taille du trou du graphique en anneau parent en pourcentage.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_DoughnutHoleSize()
```

## Remarques


S'applique uniquement aux groupes de séries du type [Doughnut](../../chartseriestype/).

L'intervalle des valeurs acceptables va de 0 à 90 inclus. La valeur par défaut est 75.

## Exemples



Montre comment créer et formater un graphique Doughnut.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Doughnut, 400, 400);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
// Supprime la série générée par défaut.
chart->get_Series()->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"});
chart->get_Series()->Add(u"Series 1", categories, System::MakeArray<double>({4, 2, 5}));

// Formate le graphique Doughnut.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = chart->get_SeriesGroups()->idx_get(0);
seriesGroup->set_DoughnutHoleSize(10);
seriesGroup->set_FirstSliceAngle(270);

doc->Save(get_ArtifactsDir() + u"Charts.DoughnutChart.docx");
```

## Voir aussi

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
