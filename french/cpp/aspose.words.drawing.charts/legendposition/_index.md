---
title: "Aspose::Words::Drawing::Charts::LegendPosition enum"
linktitle: "LegendPosition"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::LegendPosition enum. Spécifie les positions possibles d'une légende de graphique en C++."
type: docs
weight: 29000
url: /fr/cpp/aspose.words.drawing.charts/legendposition/
---
## LegendPosition enum


Spécifie les positions possibles pour une légende de graphique.

```cpp
enum class LegendPosition
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 0 | Aucune légende ne sera affichée pour le graphique. |
| Bottom | 1 | Spécifie que la légende doit être dessinée en bas du graphique. |
| Gauche | 2 | Spécifie que la légende doit être dessinée à gauche du graphique. |
| Droite | 3 | Spécifie que la légende doit être dessinée à droite du graphique. |
| Top | 4 | Spécifie que la légende doit être dessinée en haut du graphique. |
| HautDroite | 5 | Spécifie que la légende doit être dessinée en haut à droite du graphique. |


## Exemples



Montre comment modifier l'apparence de la légende d'un graphique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(3, chart->get_Series()->get_Count());
ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

// Déplacez la légende du graphique vers le coin supérieur droit.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> legend = chart->get_Legend();
legend->set_Position(Aspose::Words::Drawing::Charts::LegendPosition::TopRight);

// Donnez plus d'espace aux autres éléments du graphique, comme le tracé, en leur permettant de chevaucher la légende.
legend->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartLegend.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
