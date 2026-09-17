---
title: "Classe Aspose::Words::Drawing::Charts::AxisBound"
linktitle: "AxisBound"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Drawing::Charts::AxisBound. Représente la limite minimale ou maximale des valeurs d'axe. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.drawing.charts/axisbound/
---
## AxisBound class


Représente la limite minimale ou maximale des valeurs d’axe. Pour en savoir plus, consultez l’article de documentation [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class AxisBound : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [AxisBound](./axisbound/)() | Crée une nouvelle instance indiquant que la limite d'axe doit être déterminée automatiquement par une application de traitement de texte. |
| [AxisBound](./axisbound/)(double) | Crée une limite d'axe représentée sous forme de nombre. |
| [AxisBound](./axisbound/)(System::DateTime) | Crée une limite d'axe représentée sous forme de valeur date‑heure. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |
| [get_IsAuto](./get_isauto/)() const | Renvoie un indicateur indiquant que la limite d'axe doit être déterminée automatiquement. |
| [get_Value](./get_value/)() const | Renvoie la valeur numérique de la limite d'axe. |
| [get_ValueAsDate](./get_valueasdate/)() | Renvoie la valeur de la limite d'axe représentée sous forme de date‑heure. |
| [GetHashCode](./gethashcode/)() const override | Servit de fonction de hachage pour ce type. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | Renvoie une chaîne conviviale qui affiche la valeur de cet objet. |
| static [Type](./type/)() |  |
## Remarques


La limite peut être spécifiée comme un nombre, une date‑heure ou une valeur spéciale "auto".

Les instances de cette classe sont immuables.

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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
