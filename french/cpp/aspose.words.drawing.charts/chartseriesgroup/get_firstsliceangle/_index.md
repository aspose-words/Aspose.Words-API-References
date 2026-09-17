---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle méthode"
linktitle: "get_FirstSliceAngle"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle méthode. Obtient ou définit l'angle, en degrés, de la première tranche du graphique circulaire parent en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.drawing.charts/chartseriesgroup/get_firstsliceangle/
---
## ChartSeriesGroup::get_FirstSliceAngle method


Obtient ou définit l'angle, en degrés, de la première tranche du graphique circulaire parent.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle()
```

## Remarques


S'applique aux groupes de séries des types [Pie](../../chartseriestype/), [Pie3D](../../chartseriestype/) et [Doughnut](../../chartseriestype/).

La plage de valeurs acceptables va de 0 à 360 inclusive. La valeur par défaut est 0.

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
