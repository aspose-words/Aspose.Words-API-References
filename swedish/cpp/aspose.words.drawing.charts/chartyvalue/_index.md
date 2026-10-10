---
title: "Aspose::Words::Drawing::Charts::ChartYValue klass"
linktitle: "ChartYValue"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartYValue klass. Representerar ett Y‑värde för en diagramserie i C++."
type: docs
weight: 18600
url: /sv/cpp/aspose.words.drawing.charts/chartyvalue/
---
## ChartYValue class


Representerar ett Y‑värde för en diagramserie.

```cpp
class ChartYValue : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Hämtar en flagga som indikerar om det angivna objektet är lika med det aktuella Y‑värdeobjektet. |
| static [FromDateTime](./fromdatetime/)(System::DateTime) | Skapar en [ChartYValue](./) instans av typen [DateTime](../chartyvaluetype/). |
| static [FromDouble](./fromdouble/)(double) | Skapar en [ChartYValue](./) instans av typen [Double](../chartyvaluetype/). |
| static [FromTimeSpan](./fromtimespan/)(System::TimeSpan) | Skapar en [ChartYValue](./) instans av typen [Time](../chartyvaluetype/). |
| [get_DateTimeValue](./get_datetimevalue/)() const | Hämtar det lagrade datum/tid‑värdet. |
| [get_DoubleValue](./get_doublevalue/)() const | Hämtar det lagrade numeriska värdet. |
| [get_TimeValue](./get_timevalue/)() const | Hämtar det lagrade tidsvärdet. |
| [get_ValueType](./get_valuetype/)() const | Hämtar typen av Y‑värdet som lagras i objektet. |
| [GetHashCode](./gethashcode/)() const override | Hämtar en hash‑kod för det aktuella Y‑värdeobjektet. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Anmärkningar


Denna klass innehåller ett antal statiska metoder för att skapa ett Y‑värde av en viss typ. Egenskapen [ValueType](./get_valuetype/) låter dig bestämma typen av ett befintligt Y‑värde.

Alla icke‑null Y‑värden i en diagramserie måste vara av samma [ChartYValueType](../chartyvaluetype/) typ.
## Se även

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
