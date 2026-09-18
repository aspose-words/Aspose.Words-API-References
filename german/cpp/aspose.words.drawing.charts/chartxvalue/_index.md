---
title: "Aspose::Words::Drawing::Charts::ChartXValue Klasse"
linktitle: "ChartXValue"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartXValue Klasse. Stellt einen X‑Wert für eine Diagrammreihe in C++ dar."
type: docs
weight: 18200
url: /de/cpp/aspose.words.drawing.charts/chartxvalue/
---
## ChartXValue class


Stellt einen X‑Wert für eine Diagrammreihe dar.

```cpp
class ChartXValue : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Gibt ein Flag zurück, das angibt, ob das angegebene Objekt dem aktuellen X‑Wert‑Objekt gleich ist. |
| static [FromDateTime](./fromdatetime/)(System::DateTime) | Erstellt eine [ChartXValue](./) Instanz des Typs [DateTime](../chartxvaluetype/). |
| static [FromDouble](./fromdouble/)(double) | Erstellt eine [ChartXValue](./) Instanz des Typs [Double](../chartxvaluetype/). |
| static [FromMultilevelValue](./frommultilevelvalue/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartMultilevelValue\>\&) | Erstellt eine [ChartXValue](./)-Instanz des Typs [Multilevel](../chartxvaluetype/). |
| static [FromString](./fromstring/)(const System::String\&) | Erstellt eine [ChartXValue](./)-Instanz des Typs [String](../chartxvaluetype/). |
| static [FromTimeSpan](./fromtimespan/)(System::TimeSpan) | Erstellt eine [ChartXValue](./)-Instanz des Typs [Time](../chartxvaluetype/). |
| [get_DateTimeValue](./get_datetimevalue/)() const | Gibt den gespeicherten Datums‑Uhrzeitwert zurück. |
| [get_DoubleValue](./get_doublevalue/)() const | Gibt den gespeicherten numerischen Wert zurück. |
| [get_MultilevelValue](./get_multilevelvalue/)() const | Gibt den gespeicherten mehrstufigen Wert zurück. |
| [get_StringValue](./get_stringvalue/)() const | Gibt den gespeicherten Zeichenkettenwert zurück. |
| [get_TimeValue](./get_timevalue/)() const | Gibt den gespeicherten Zeitwert zurück. |
| [get_ValueType](./get_valuetype/)() const | Gibt den Typ des im Objekt gespeicherten X‑Werts zurück. |
| [GetHashCode](./gethashcode/)() const override | Gibt einen Hash‑Code für das aktuelle X‑Wert‑Objekt zurück. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Hinweise


Diese Klasse enthält mehrere statische Methoden zum Erstellen eines X‑Werts eines bestimmten Typs. Die Eigenschaft [ValueType](./get_valuetype/) ermöglicht es Ihnen, den Typ eines vorhandenen X‑Werts zu bestimmen.

Alle nicht‑null X‑Werte einer Diagrammreihe müssen vom selben Typ [ChartXValueType](../chartxvaluetype/) sein.

## Beispiele



Zeigt, wie Diagrammreihen mit Daten gefüllt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// Löscht X‑ und Y‑Werte der ersten Reihe.
series1->ClearValues();

// Füllen Sie die Reihe mit Daten.
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(5), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(5));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(7), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(11));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(9));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series2 = chart->get_Series()->idx_get(1);
// Löscht X‑ und Y‑Werte der zweiten Reihe.
series2->Clear();

// Füllen Sie die Reihe mit Daten.
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(2), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(4));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(4), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(6), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(14));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(8), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
