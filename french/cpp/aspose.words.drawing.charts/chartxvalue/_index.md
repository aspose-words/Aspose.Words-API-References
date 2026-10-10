---
title: "Aspose::Words::Drawing::Charts::ChartXValue classe"
linktitle: "ChartXValue"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartXValue classe. Représente une valeur X pour une série de graphique en C++."
type: docs
weight: 18200
url: /fr/cpp/aspose.words.drawing.charts/chartxvalue/
---
## ChartXValue class


Représente une valeur X pour une série de graphique.

```cpp
class ChartXValue : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Obtient un indicateur indiquant si l'objet spécifié est égal à l'objet valeur X actuel. |
| static [FromDateTime](./fromdatetime/)(System::DateTime) | Crée une instance de [ChartXValue](./) du type [DateTime](../chartxvaluetype/). |
| static [FromDouble](./fromdouble/)(double) | Crée une instance de [ChartXValue](./) du type [Double](../chartxvaluetype/). |
| static [FromMultilevelValue](./frommultilevelvalue/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartMultilevelValue\>\&) | Crée une instance de [ChartXValue](./) du type [Multilevel](../chartxvaluetype/). |
| static [FromString](./fromstring/)(const System::String\&) | Crée une instance de [ChartXValue](./) du type [String](../chartxvaluetype/). |
| static [FromTimeSpan](./fromtimespan/)(System::TimeSpan) | Crée une instance de [ChartXValue](./) du type [Time](../chartxvaluetype/). |
| [get_DateTimeValue](./get_datetimevalue/)() const | Obtient la valeur datetime stockée. |
| [get_DoubleValue](./get_doublevalue/)() const | Obtient la valeur numérique stockée. |
| [get_MultilevelValue](./get_multilevelvalue/)() const | Obtient la valeur multilevel stockée. |
| [get_StringValue](./get_stringvalue/)() const | Obtient la valeur chaîne stockée. |
| [get_TimeValue](./get_timevalue/)() const | Obtient la valeur temps stockée. |
| [get_ValueType](./get_valuetype/)() const | Obtient le type de la valeur X stockée dans l'objet. |
| [GetHashCode](./gethashcode/)() const override | Obtient un code de hachage pour l'objet de valeur X actuel. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Remarques


Cette classe contient un certain nombre de méthodes statiques pour créer une valeur X d'un type particulier. La propriété [ValueType](./get_valuetype/) vous permet de déterminer le type d'une valeur X existante.

Toutes les valeurs X non nulles d'une série de graphique doivent être du même type [ChartXValueType](../chartxvaluetype/).

## Exemples



Montre comment remplir les séries de graphique avec des données.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// Efface les valeurs X et Y de la première série.
series1->ClearValues();

// Remplissez la série avec des données.
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(5), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(5));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(7), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(11));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(9));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series2 = chart->get_Series()->idx_get(1);
// Efface les valeurs X et Y de la deuxième série.
series2->Clear();

// Remplissez la série avec des données.
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(2), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(4));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(4), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(6), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(14));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(8), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
