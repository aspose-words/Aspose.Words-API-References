---
title: "Méthode Aspose::Words::Drawing::Charts::AxisBound::get_Value"
linktitle: "get_Value"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::Charts::AxisBound::get_Value. Retourne la valeur numérique de la limite d'axe en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.drawing.charts/axisbound/get_value/
---
## AxisBound::get_Value method


Renvoie la valeur numérique de la limite d'axe.

```cpp
double Aspose::Words::Drawing::Charts::AxisBound::get_Value() const
```


## Exemples



Montre comment définir des limites d'axe personnalisées.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Effacez la série de données de démonstration du graphique pour commencer avec un graphique vierge.
chart->get_Series()->Clear();

// Ajoutez une série avec deux tableaux décimaux. Le premier tableau contient les valeurs X,
// et le second contient les valeurs Y correspondantes pour les points du graphique en nuage de points.
chart->get_Series()->Add(u"Series 1", System::MakeArray<double>({1.1, 5.4, 7.9, 3.5, 2.1, 9.7}), System::MakeArray<double>({2.1, 0.3, 0.6, 3.3, 1.4, 1.9}));

// Par défaut, un redimensionnement par défaut est appliqué aux axes X et Y du graphique,
// de sorte que leurs plages soient suffisamment grandes pour englober chaque valeur X et Y de chaque série.
ASSERT_TRUE(chart->get_AxisX()->get_Scaling()->get_Minimum()->get_IsAuto());

// Nous pouvons définir nos propres limites d'axe.
// Dans ce cas, nous ferons en sorte que les règles des axes X et Y affichent une plage de 0 à 10.
chart->get_AxisX()->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(0.0));
chart->get_AxisX()->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(10.0));
chart->get_AxisY()->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(0.0));
chart->get_AxisY()->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(10.0));

ASSERT_FALSE(chart->get_AxisX()->get_Scaling()->get_Minimum()->get_IsAuto());
ASSERT_FALSE(chart->get_AxisY()->get_Scaling()->get_Minimum()->get_IsAuto());

// Créez un graphique en ligne avec une série nécessitant une plage de dates sur l'axe X et des valeurs décimales pour l'axe Y.
chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 300);
chart = chartShape->get_Chart();
chart->get_Series()->Clear();

System::ArrayPtr<System::DateTime> dates = System::MakeArray<System::DateTime>({System::DateTime(1973, 5, 11), System::DateTime(1981, 2, 4), System::DateTime(1985, 9, 23), System::DateTime(1989, 6, 28), System::DateTime(1994, 12, 15)});

chart->get_Series()->Add(u"Series 1", dates, System::MakeArray<double>({3.0, 4.7, 5.9, 7.1, 8.9}));

// Nous pouvons également définir les limites d'axe sous forme de dates, limitant le graphique à une période.
// Définir la plage à 1980-1990 omettra les deux valeurs de la série
// qui sont en dehors de la plage du graphique.
chart->get_AxisX()->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(1980, 1, 1)));
chart->get_AxisX()->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(1990, 1, 1)));

doc->Save(get_ArtifactsDir() + u"Charts.AxisBound.docx");
```

## Voir aussi

* Class [AxisBound](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
