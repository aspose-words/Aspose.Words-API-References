---
title: "Aspose::Words::Drawing::Charts::ChartXValue‑klass"
linktitle: "ChartXValue"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartXValue‑klass. Representerar ett X‑värde för en diagramserie i C++."
type: docs
weight: 18200
url: /sv/cpp/aspose.words.drawing.charts/chartxvalue/
---
## ChartXValue class


Representerar ett X‑värde för en diagramserie.

```cpp
class ChartXValue : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Hämtar en flagga som indikerar om det angivna objektet är lika med det aktuella X‑värdeobjektet. |
| static [FromDateTime](./fromdatetime/)(System::DateTime) | Skapar en [ChartXValue](./)-instans av typen [DateTime](../chartxvaluetype/). |
| static [FromDouble](./fromdouble/)(double) | Skapar en [ChartXValue](./)-instans av typen [Double](../chartxvaluetype/). |
| static [FromMultilevelValue](./frommultilevelvalue/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartMultilevelValue\>\&) | Skapar en [ChartXValue](./)-instans av typen [Multilevel](../chartxvaluetype/). |
| static [FromString](./fromstring/)(const System::String\&) | Skapar en [ChartXValue](./) instans av typen [String](../chartxvaluetype/). |
| static [FromTimeSpan](./fromtimespan/)(System::TimeSpan) | Skapar en [ChartXValue](./) instans av typen [Time](../chartxvaluetype/). |
| [get_DateTimeValue](./get_datetimevalue/)() const | Hämtar det lagrade datum/tid‑värdet. |
| [get_DoubleValue](./get_doublevalue/)() const | Hämtar det lagrade numeriska värdet. |
| [get_MultilevelValue](./get_multilevelvalue/)() const | Hämtar det lagrade flernivåvärdet. |
| [get_StringValue](./get_stringvalue/)() const | Hämtar det lagrade strängvärdet. |
| [get_TimeValue](./get_timevalue/)() const | Hämtar det lagrade tidsvärdet. |
| [get_ValueType](./get_valuetype/)() const | Hämtar typen av X‑värdet som är lagrat i objektet. |
| [GetHashCode](./gethashcode/)() const override | Hämtar en hashkod för det aktuella X‑värdeobjektet. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Anmärkningar


Denna klass innehåller ett antal statiska metoder för att skapa ett X‑värde av en viss typ. Egenskapen [ValueType](./get_valuetype/) låter dig bestämma typen av ett befintligt X‑värde.

Alla icke‑null X‑värden i en diagramserie måste vara av samma typ [ChartXValueType](../chartxvaluetype/).

## Exempel



Visar hur man fyller diagramserier med data.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// Rensa X‑ och Y‑värdena i den första serien.
series1->ClearValues();

// Fyll serien med data.
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(5), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(5));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(7), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(11));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(9));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series2 = chart->get_Series()->idx_get(1);
// Rensa X‑ och Y‑värdena i den andra serien.
series2->Clear();

// Fyll serien med data.
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(2), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(4));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(4), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(6), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(14));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(8), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## Se även

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
