---
title: "Aspose::Words::Drawing::Charts::AxisScaleType énum"
linktitle: "AxisScaleType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::AxisScaleType énum. Spécifie les types d'échelle possibles pour un axe en C++."
type: docs
weight: 23000
url: /fr/cpp/aspose.words.drawing.charts/axisscaletype/
---
## AxisScaleType enum


Spécifie les types d'échelle possibles pour un axe.

```cpp
enum class AxisScaleType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Linéaire | 0 | Mise à l'échelle linéaire. |
| Logarithmique | 1 | Mise à l'échelle logarithmique. |


## Exemples



Montre comment appliquer une mise à l'échelle logarithmique à un axe de graphique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Effacez la série de données de démonstration du graphique pour commencer avec un graphique vierge.
chart->get_Series()->Clear();

// Insérez une série avec des coordonnées X/Y pour cinq points.
chart->get_Series()->Add(u"Series 1", System::MakeArray<double>({1.0, 2.0, 3.0, 4.0, 5.0}), System::MakeArray<double>({1.0, 20.0, 400.0, 8000.0, 160000.0}));

// Le réglage de l'axe X est linéaire par défaut,
// affichant des valeurs incrémentées uniformément qui couvrent notre plage de valeurs X (0, 1, 2, 3...).
// Un axe linéaire n'est pas idéal pour nos valeurs Y
// car les points avec des valeurs Y plus petites seront plus difficiles à lire.
// Une mise à l'échelle logarithmique avec une base de 20 (1, 20, 400, 8000...)
// répartira les points tracés, nous permettant de lire leurs valeurs sur le graphique plus facilement.
chart->get_AxisY()->get_Scaling()->set_Type(Aspose::Words::Drawing::Charts::AxisScaleType::Logarithmic);
chart->get_AxisY()->get_Scaling()->set_LogBase(20);

doc->Save(get_ArtifactsDir() + u"Charts.AxisScaling.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
