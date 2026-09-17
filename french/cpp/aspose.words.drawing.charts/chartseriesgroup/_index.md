---
title: "classe Aspose::Words::Drawing::Charts::ChartSeriesGroup"
linktitle: "ChartSeriesGroup"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "classe Aspose::Words::Drawing::Charts::ChartSeriesGroup. Représente les propriétés d'un groupe de séries de graphique, c’est‑à‑dire les propriétés des séries de graphique du même type associées aux mêmes axes en C++."
type: docs
weight: 17334
url: /fr/cpp/aspose.words.drawing.charts/chartseriesgroup/
---
## ChartSeriesGroup class


Représente les propriétés d'un groupe de séries de graphique, c'est‑à‑dire les propriétés des séries de même type associées aux mêmes axes.

```cpp
class ChartSeriesGroup : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_AxisGroup](./get_axisgroup/)() | Obtient ou définit le groupe d'axes auquel ce groupe de séries appartient. |
| [get_AxisX](./get_axisx/)() | Fournit l'accès aux propriétés de l'axe X de ce groupe de séries. |
| [get_AxisY](./get_axisy/)() | Fournit l'accès aux propriétés de l'axe Y de ce groupe de séries. |
| [get_BubbleScale](./get_bubblescale/)() | Obtient ou définit la taille des bulles en pourcentage de leur taille par défaut. |
| [get_DoughnutHoleSize](./get_doughnutholesize/)() | Obtient ou définit la taille du trou du graphique en anneau parent en pourcentage. |
| [get_FirstSliceAngle](./get_firstsliceangle/)() | Obtient ou définit l'angle, en degrés, de la première tranche du graphique circulaire parent. |
| [get_GapWidth](./get_gapwidth/)() | Obtient ou définit le pourcentage de l'écart de largeur entre les éléments du graphique. |
| [get_Overlap](./get_overlap/)() | Obtient ou définit le pourcentage de chevauchement des barres ou colonnes de la série. |
| [get_SecondSectionSize](./get_secondsectionsize/)() | Obtient ou définit la taille de la section secondaire du diagramme circulaire en pourcentage. |
| [get_Series](./get_series/)() | Obtient une collection de séries appartenant à ce groupe de séries. |
| [get_SeriesType](./get_seriestype/)() | Obtient le type de séries de graphique inclus dans ce groupe. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AxisGroup](./set_axisgroup/)(Aspose::Words::Drawing::Charts::AxisGroup) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_AxisGroup](./get_axisgroup/). |
| [set_BubbleScale](./set_bubblescale/)(int32_t) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale](./get_bubblescale/). |
| [set_DoughnutHoleSize](./set_doughnutholesize/)(int32_t) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_DoughnutHoleSize](./get_doughnutholesize/). |
| [set_FirstSliceAngle](./set_firstsliceangle/)(int32_t) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle](./get_firstsliceangle/). |
| [set_GapWidth](./set_gapwidth/)(int32_t) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth](./get_gapwidth/). |
| [set_Overlap](./set_overlap/)(int32_t) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap](./get_overlap/). |
| [set_SecondSectionSize](./set_secondsectionsize/)(int32_t) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize](./get_secondsectionsize/). |
| static [Type](./type/)() |  |
## Remarques


Les graphiques combinés contiennent plusieurs groupes de séries de graphiques, avec un groupe distinct pour chaque type de série.

De plus, vous pouvez créer un groupe de séries de graphiques pour attribuer des axes secondaires à une ou plusieurs séries de graphiques.

Pour en savoir plus, consultez l'article de documentation [Travailler avec les graphiques](https://docs.aspose.com/words/cpp/working-with-charts/).

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
