---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize méthode"
linktitle: "get_SecondSectionSize"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize method. Obtient ou définit la taille de la section secondaire du diagramme circulaire en pourcentage en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words.drawing.charts/chartseriesgroup/get_secondsectionsize/
---
## ChartSeriesGroup::get_SecondSectionSize method


Obtient ou définit la taille de la section secondaire du diagramme circulaire en pourcentage.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize()
```

## Remarques


S'applique aux groupes de séries des types [PieOfPie](../../chartseriestype/) et [PieOfBar](../../chartseriestype/).

L'intervalle des valeurs acceptables va de 5 à 200 inclus. La valeur par défaut est 75.

## Exemples



Montre comment créer et formater le diagramme pie of Pie.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::PieOfPie, 440, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
// Supprime la série générée par défaut.
chart->get_Series()->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"});
chart->get_Series()->Add(u"Series 1", categories, System::MakeArray<double>({11, 8, 4, 3}));

// Formate le diagramme Pie of Pie.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = chart->get_SeriesGroups()->idx_get(0);
seriesGroup->set_GapWidth(10);
seriesGroup->set_SecondSectionSize(77);

doc->Save(get_ArtifactsDir() + u"Charts.PieOfPieChart.docx");
```

## Voir aussi

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
