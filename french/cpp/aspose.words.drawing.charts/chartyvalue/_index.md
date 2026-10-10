---
title: "Aspose::Words::Drawing::Charts::ChartYValue classe"
linktitle: "ChartYValue"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartYValue classe. Représente une valeur Y pour une série de graphique en C++."
type: docs
weight: 18600
url: /fr/cpp/aspose.words.drawing.charts/chartyvalue/
---
## ChartYValue class


Représente une valeur Y pour une série de graphique.

```cpp
class ChartYValue : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Obtient un indicateur indiquant si l'objet spécifié est égal à l'objet valeur Y actuel. |
| static [FromDateTime](./fromdatetime/)(System::DateTime) | Crée une instance de [ChartYValue](./) du type [DateTime](../chartyvaluetype/). |
| static [FromDouble](./fromdouble/)(double) | Crée une instance de [ChartYValue](./) du type [Double](../chartyvaluetype/). |
| static [FromTimeSpan](./fromtimespan/)(System::TimeSpan) | Crée une instance de [ChartYValue](./) du type [Time](../chartyvaluetype/). |
| [get_DateTimeValue](./get_datetimevalue/)() const | Obtient la valeur datetime stockée. |
| [get_DoubleValue](./get_doublevalue/)() const | Obtient la valeur numérique stockée. |
| [get_TimeValue](./get_timevalue/)() const | Obtient la valeur temps stockée. |
| [get_ValueType](./get_valuetype/)() const | Obtient le type de la valeur Y stockée dans l'objet. |
| [GetHashCode](./gethashcode/)() const override | Obtient un code de hachage pour l'objet valeur Y actuel. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Remarques


Cette classe contient un certain nombre de méthodes statiques pour créer une valeur Y d'un type particulier. La propriété [ValueType](./get_valuetype/) vous permet de déterminer le type d'une valeur Y existante.

Toutes les valeurs Y non nulles d'une série de graphique doivent être du même type [ChartYValueType](../chartyvaluetype/).
## Voir aussi

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
