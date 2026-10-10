---
title: "Aspose::Words::Drawing::Charts::ChartXValue classe"
linktitle: "ChartXValue"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartXValue classe. Rappresenta un valore X per una serie di grafico in C++."
type: docs
weight: 18200
url: /it/cpp/aspose.words.drawing.charts/chartxvalue/
---
## ChartXValue class


Rappresenta un valore X per una serie del grafico.

```cpp
class ChartXValue : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Ottiene un flag che indica se l'oggetto specificato è uguale all'oggetto valore X corrente. |
| static [FromDateTime](./fromdatetime/)(System::DateTime) | Crea un'istanza di [ChartXValue](./) del tipo [DateTime](../chartxvaluetype/). |
| static [FromDouble](./fromdouble/)(double) | Crea un'istanza di [ChartXValue](./) del tipo [Double](../chartxvaluetype/). |
| static [FromMultilevelValue](./frommultilevelvalue/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartMultilevelValue\>\&) | Crea un'istanza di [ChartXValue](./) del tipo [Multilevel](../chartxvaluetype/). |
| static [FromString](./fromstring/)(const System::String\&) | Crea un'istanza di [ChartXValue](./) del tipo [String](../chartxvaluetype/). |
| static [FromTimeSpan](./fromtimespan/)(System::TimeSpan) | Crea un'istanza di [ChartXValue](./) del tipo [Time](../chartxvaluetype/). |
| [get_DateTimeValue](./get_datetimevalue/)() const | Ottiene il valore datetime memorizzato. |
| [get_DoubleValue](./get_doublevalue/)() const | Ottiene il valore numerico memorizzato. |
| [get_MultilevelValue](./get_multilevelvalue/)() const | Ottiene il valore multilevel memorizzato. |
| [get_StringValue](./get_stringvalue/)() const | Ottiene il valore stringa memorizzato. |
| [get_TimeValue](./get_timevalue/)() const | Ottiene il valore time memorizzato. |
| [get_ValueType](./get_valuetype/)() const | Ottiene il tipo del valore X memorizzato nell'oggetto. |
| [GetHashCode](./gethashcode/)() const override | Ottiene un codice hash per l'oggetto valore X corrente. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Note


Questa classe contiene numerosi metodi statici per creare un valore X di un tipo particolare. La proprietà [ValueType](./get_valuetype/) consente di determinare il tipo di un valore X esistente.

Tutti i valori X non nulli di una serie di grafico devono essere dello stesso tipo [ChartXValueType](../chartxvaluetype/).

## Esempi



Mostra come popolare le serie del grafico con i dati.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// Cancella i valori X e Y della prima serie.
series1->ClearValues();

// Popola la serie con i dati.
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(5), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(5));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(7), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(11));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(9));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series2 = chart->get_Series()->idx_get(1);
// Cancella i valori X e Y della seconda serie.
series2->Clear();

// Popola la serie con i dati.
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(2), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(4));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(4), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(6), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(14));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(8), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
