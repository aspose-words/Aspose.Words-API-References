---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelPosition enum"
linktitle: "ChartDataLabelPosition"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelPosition enum. Spécifie la position d’une étiquette de données de graphique en C++."
type: docs
weight: 27334
url: /fr/cpp/aspose.words.drawing.charts/chartdatalabelposition/
---
## ChartDataLabelPosition enum


Spécifie la position d'une étiquette de données de graphique.

```cpp
enum class ChartDataLabelPosition
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Centre | 0 | Spécifie qu’une étiquette de données doit être affichée centrée sur un marqueur de données. |
| Gauche | 1 | Spécifie qu’une étiquette de données doit être affichée à gauche d’un marqueur de données. |
| Droite | 2 | Spécifie qu’une étiquette de données doit être affichée à droite d’un marqueur de données. |
| Above | 3 | Spécifie qu’une étiquette de données doit être affichée au-dessus d’un marqueur de données. |
| Below | 4 | Spécifie qu’une étiquette de données doit être affichée en dessous d’un marqueur de données. |
| InsideBase | 5 | Spécifie qu’une étiquette de données doit être affichée à l’intérieur de la base d’un marqueur de données. |
| InsideEnd | 6 | Spécifie qu’une étiquette de données doit être affichée à l’intérieur de l’extrémité d’un marqueur de données. |
| OutsideEnd | 7 | Spécifie qu’une étiquette de données doit être affichée à l’extérieur de l’extrémité d’un repère de données. |
| BestFit | 8 | Spécifie qu’une étiquette de données doit être affichée à la position la plus appropriée. |


## Exemples



Montre comment définir la position de l’étiquette de données.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérer un graphique en colonnes.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();

// Supprimer la série générée par défaut.
seriesColl->Clear();

// Ajouter une série.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = seriesColl->Add(u"Series 1", System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"}), System::MakeArray<double>({4, 5, 6}));

// Afficher les étiquettes de données et définir la couleur de la police.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->get_Font()->set_Color(System::Drawing::Color::get_White());

// Définir la position de l’étiquette de données.
dataLabels->set_Position(Aspose::Words::Drawing::Charts::ChartDataLabelPosition::InsideBase);
dataLabels->idx_get(0)->set_Position(Aspose::Words::Drawing::Charts::ChartDataLabelPosition::OutsideEnd);
dataLabels->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_DarkRed());

doc->Save(get_ArtifactsDir() + u"Charts.LabelPosition.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
