---
title: "Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden méthode"
linktitle: "get_Hidden"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden méthode. Obtient ou définit un indicateur indiquant si cet axe est masqué ou non en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words.drawing.charts/chartaxis/get_hidden/
---
## ChartAxis::get_Hidden method


Obtient ou définit un indicateur indiquant si cet axe est masqué ou non.

```cpp
bool Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden()
```


## Exemples



Montre comment masquer les axes du graphique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Effacez la série de données de démonstration du graphique pour commencer avec un graphique vierge.
chart->get_Series()->Clear();

// Ajoutez une série personnalisée avec des catégories pour l'axe X, et les valeurs décimales correspondantes pour l'axe Y.
chart->get_Series()->Add(u"AW Series 1", System::MakeArray<System::String>({u"Item 1", u"Item 2", u"Item 3", u"Item 4", u"Item 5"}), System::MakeArray<double>({1.2, 0.3, 2.1, 2.9, 4.2}));

// Masquez les axes du graphique pour simplifier l'apparence du graphique.
chart->get_AxisX()->set_Hidden(true);
chart->get_AxisY()->set_Hidden(true);

doc->Save(get_ArtifactsDir() + u"Charts.HideChartAxis.docx");
```

## Voir aussi

* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
