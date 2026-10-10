---
title: "Aspose::Words::Drawing::Charts::ChartStyle enum"
linktitle: "ChartStyle"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartStyle enum. Spécifie les styles prédéfinis d'un graphique en C++."
type: docs
weight: 27875
url: /fr/cpp/aspose.words.drawing.charts/chartstyle/
---
## ChartStyle enum


Spécifie les styles prédéfinis d'un graphique.

```cpp
enum class ChartStyle
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Normal | 0 | Représente le style de graphique par défaut. |
| Muted | 1 | Un style avec des couleurs atténuées. |
| Saturated | 2 | Un style avec des couleurs plus saturées. |
| Shaded | 3 | Un style avec des points de données ombrés. |
| Flat | 4 | Un style avec des points de données plats sans dégradé. |
| Shadowed | 5 | Un style avec des points de données ayant une ombre. |
| Dégradé | 6 | Un style avec un remplissage en dégradé des points de données. |
| Original | 7 | Un style avec une apparence originale d'un graphique. |
| Transparent1 | 8 | Un style avec des points de données transparents. |
| Transparent2 | 9 | Un style avec des points de données transparents. |
| Outline | 10 | Un style avec des points de données sans remplissage, mais seulement un contour. |
| OutlineBlack | 11 | Un style avec un arrière-plan de graphique noir, dans lequel les points de données n'ont pas de remplissage, mais seulement un contour. |
| Noir | 12 | Un style avec un arrière-plan de graphique noir. |
| Grey | 13 | Un style avec un arrière-plan de graphique à dégradé gris. |
| Bleu | 14 | Un style avec un arrière-plan de graphique bleu. |
| ShadedPlot | 15 | Un style dans lequel la zone du tracé est ombrée. |


## Exemples



Montre comment définir et obtenir le style du graphique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérer un graphique avec le style Noir.
builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 250, Aspose::Words::Drawing::Charts::ChartStyle::Black);

doc->Save(get_ArtifactsDir() + u"Charts.SetChartStyle.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Charts.SetChartStyle.docx");

// Obtenir un graphique à mettre à jour.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Obtenir le style du graphique.
ASSERT_EQ(Aspose::Words::Drawing::Charts::ChartStyle::Black, chart->get_Style());
```

## Voir aussi

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
