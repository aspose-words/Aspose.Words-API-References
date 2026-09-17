---
title: "Aspose::Words::Drawing::Charts::ChartAxis::get_Scaling méthode"
linktitle: "get_Scaling"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartAxis::get_Scaling méthode. Fournit l'accès aux options de mise à l'échelle de l'axe en C++."
type: docs
weight: 22000
url: /fr/cpp/aspose.words.drawing.charts/chartaxis/get_scaling/
---
## ChartAxis::get_Scaling method


Fournit l'accès aux options de mise à l'échelle de l'axe.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::AxisScaling> Aspose::Words::Drawing::Charts::ChartAxis::get_Scaling()
```


## Exemples



Montre comment insérer un graphique avec des valeurs date/heure.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Effacez la série de données de démonstration du graphique pour commencer avec un graphique vierge.
chart->get_Series()->Clear();

// Ajoutez une série personnalisée contenant des valeurs date/heure pour l'axe X, ainsi que les valeurs décimales correspondantes pour l'axe Y.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::DateTime>({System::DateTime(2017, 11, 6), System::DateTime(2017, 11, 9), System::DateTime(2017, 11, 15), System::DateTime(2017, 11, 21), System::DateTime(2017, 11, 25), System::DateTime(2017, 11, 29)}), System::MakeArray<double>({1.2, 0.3, 2.1, 2.9, 4.2, 5.3}));

// Définissez les limites inférieure et supérieure pour l'axe X.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> xAxis = chart->get_AxisX();
xAxis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(2017, 11, 5).ToOADate()));
xAxis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(2017, 12, 3)));

// Définissez les unités majeures de l'axe X à une semaine, et les unités mineures à un jour.
xAxis->set_BaseTimeUnit(Aspose::Words::Drawing::Charts::AxisTimeUnit::Days);
xAxis->set_MajorUnit(7.0);
xAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
xAxis->set_MinorUnit(1.0);
xAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Outside);
xAxis->set_HasMajorGridlines(true);
xAxis->set_HasMinorGridlines(true);

// Définissez les propriétés de l'axe Y pour les valeurs décimales.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> yAxis = chart->get_AxisY();
yAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::High);
yAxis->set_MajorUnit(100.0);
yAxis->set_MinorUnit(50.0);
yAxis->get_DisplayUnit()->set_Unit(Aspose::Words::Drawing::Charts::AxisBuiltInUnit::Hundreds);
yAxis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(100.0));
yAxis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(700.0));
yAxis->set_HasMajorGridlines(true);
yAxis->set_HasMinorGridlines(true);

doc->Save(get_ArtifactsDir() + u"Charts.DateTimeValues.docx");
```

## Voir aussi

* Class [AxisScaling](../../axisscaling/)
* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
