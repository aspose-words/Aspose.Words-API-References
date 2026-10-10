---
title: "Aspose::Words::Drawing::Charts::ChartYValue classe"
linktitle: "ChartYValue"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartYValue classe. Rappresenta un valore Y per una serie di grafico in C++."
type: docs
weight: 18600
url: /it/cpp/aspose.words.drawing.charts/chartyvalue/
---
## ChartYValue class


Rappresenta un valore Y per una serie di grafico.

```cpp
class ChartYValue : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Restituisce un flag che indica se l'oggetto specificato è uguale all'oggetto valore Y corrente. |
| static [FromDateTime](./fromdatetime/)(System::DateTime) | Crea un'istanza di [ChartYValue](./) del tipo [DateTime](../chartyvaluetype/). |
| static [FromDouble](./fromdouble/)(double) | Crea un'istanza di [ChartYValue](./) del tipo [Double](../chartyvaluetype/). |
| static [FromTimeSpan](./fromtimespan/)(System::TimeSpan) | Crea un'istanza di [ChartYValue](./) del tipo [Time](../chartyvaluetype/). |
| [get_DateTimeValue](./get_datetimevalue/)() const | Ottiene il valore datetime memorizzato. |
| [get_DoubleValue](./get_doublevalue/)() const | Ottiene il valore numerico memorizzato. |
| [get_TimeValue](./get_timevalue/)() const | Ottiene il valore time memorizzato. |
| [get_ValueType](./get_valuetype/)() const | Restituisce il tipo del valore Y memorizzato nell'oggetto. |
| [GetHashCode](./gethashcode/)() const override | Restituisce un codice hash per l'oggetto valore Y corrente. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Note


Questa classe contiene numerosi metodi statici per creare un valore Y di un tipo particolare. La proprietà [ValueType](./get_valuetype/) consente di determinare il tipo di un valore Y esistente.

Tutti i valori Y non nulli di una serie di grafico devono essere dello stesso tipo [ChartYValueType](../chartyvaluetype/).
## Vedi anche

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
