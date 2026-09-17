---
title: "Aspose::Words::Drawing::Charts::AxisGroup enum"
linktitle: "AxisGroup"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::AxisGroup enum. Représente un type de groupe d'axe de graphique en C++."
type: docs
weight: 22500
url: /fr/cpp/aspose.words.drawing.charts/axisgroup/
---
## AxisGroup enum


Représente un type de groupe d'axes de graphique.

```cpp
enum class AxisGroup
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Primaire | 0 | Spécifie le groupe d'axe primaire. |
| Secondaire | 1 | Spécifie le groupe d'axe secondaire. |


## Exemples



Montre comment travailler avec l'axe secondaire du graphique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();

// Supprimer la série générée par défaut.
series->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"});
series->Add(u"Series 1 of primary series group", categories, System::MakeArray<double>({2, 3, 4}));
series->Add(u"Series 2 of primary series group", categories, System::MakeArray<double>({5, 2, 3}));

// Créez un groupe de séries supplémentaire, également de type ligne.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> newSeriesGroup = chart->get_SeriesGroups()->Add(Aspose::Words::Drawing::Charts::ChartSeriesType::Line);
// Spécifiez l'utilisation des axes secondaires pour le nouveau groupe de séries.
newSeriesGroup->set_AxisGroup(Aspose::Words::Drawing::Charts::AxisGroup::Secondary);
// Masquez l'axe X secondaire.
newSeriesGroup->get_AxisX()->set_Hidden(true);
// Définissez le titre de l'axe Y secondaire.
newSeriesGroup->get_AxisY()->get_Title()->set_Show(true);
newSeriesGroup->get_AxisY()->get_Title()->set_Text(u"Secondary Y axis");

ASSERT_EQ(Aspose::Words::Drawing::Charts::ChartSeriesType::Line, newSeriesGroup->get_SeriesType());

// Ajoutez une série au nouveau groupe de séries.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series3 = newSeriesGroup->get_Series()->Add(u"Series of secondary series group", categories, System::MakeArray<double>({13, 11, 16}));
series3->get_Format()->get_Stroke()->set_Weight(3.5);

doc->Save(get_ArtifactsDir() + u"Charts.SecondaryAxis.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
