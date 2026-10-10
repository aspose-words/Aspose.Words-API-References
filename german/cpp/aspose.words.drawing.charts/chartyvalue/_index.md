---
title: "Aspose::Words::Drawing::Charts::ChartYValue Klasse"
linktitle: "ChartYValue"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartYValue Klasse. Stellt einen Y‑Wert für eine Diagrammreihe in C++ dar."
type: docs
weight: 18600
url: /de/cpp/aspose.words.drawing.charts/chartyvalue/
---
## ChartYValue class


Stellt einen Y‑Wert für eine Diagrammreihe dar.

```cpp
class ChartYValue : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Gibt ein Flag zurück, das angibt, ob das angegebene Objekt dem aktuellen Y‑Wert‑Objekt gleich ist. |
| static [FromDateTime](./fromdatetime/)(System::DateTime) | Erstellt eine [ChartYValue](./)-Instanz des Typs [DateTime](../chartyvaluetype/). |
| static [FromDouble](./fromdouble/)(double) | Erstellt eine [ChartYValue](./)-Instanz des Typs [Double](../chartyvaluetype/). |
| static [FromTimeSpan](./fromtimespan/)(System::TimeSpan) | Erstellt eine [ChartYValue](./)-Instanz des Typs [Time](../chartyvaluetype/). |
| [get_DateTimeValue](./get_datetimevalue/)() const | Gibt den gespeicherten Datums‑Uhrzeitwert zurück. |
| [get_DoubleValue](./get_doublevalue/)() const | Gibt den gespeicherten numerischen Wert zurück. |
| [get_TimeValue](./get_timevalue/)() const | Gibt den gespeicherten Zeitwert zurück. |
| [get_ValueType](./get_valuetype/)() const | Gibt den Typ des im Objekt gespeicherten Y‑Werts zurück. |
| [GetHashCode](./gethashcode/)() const override | Gibt einen Hashcode für das aktuelle Y‑Wert‑Objekt zurück. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Hinweise


Diese Klasse enthält eine Reihe von statischen Methoden zum Erstellen eines Y‑Werts eines bestimmten Typs. Die Eigenschaft [ValueType](./get_valuetype/) ermöglicht es Ihnen, den Typ eines vorhandenen Y‑Werts zu bestimmen.

Alle nicht‑null Y‑Werte einer Diagrammreihe müssen vom selben Typ [ChartYValueType](../chartyvaluetype/) sein.
## Siehe auch

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
