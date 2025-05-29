---
title: ChartXValue Class
linktitle: ChartXValue
articleTitle: ChartXValue
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Drawing.Charts.ChartXValue, la soluzione per definire i valori X nelle serie di grafici, migliorando la visualizzazione dei dati senza sforzo.
type: docs
weight: 1160
url: /it/net/aspose.words.drawing.charts/chartxvalue/
---
## ChartXValue class

Rappresenta un valore X per una serie di grafici.

```csharp
public class ChartXValue
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DateTimeValue](../../aspose.words.drawing.charts/chartxvalue/datetimevalue/) { get; } | Ottiene il valore datetime memorizzato. |
| [DoubleValue](../../aspose.words.drawing.charts/chartxvalue/doublevalue/) { get; } | Ottiene il valore numerico memorizzato. |
| [MultilevelValue](../../aspose.words.drawing.charts/chartxvalue/multilevelvalue/) { get; } | Ottiene il valore multilivello memorizzato. |
| [StringValue](../../aspose.words.drawing.charts/chartxvalue/stringvalue/) { get; } | Ottiene il valore della stringa memorizzata. |
| [TimeValue](../../aspose.words.drawing.charts/chartxvalue/timevalue/) { get; } | Ottiene il valore temporale memorizzato. |
| [ValueType](../../aspose.words.drawing.charts/chartxvalue/valuetype/) { get; } | Ottiene il tipo del valore X memorizzato nell'oggetto. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| static [FromDateTime](../../aspose.words.drawing.charts/chartxvalue/fromdatetime/)(*DateTime*) | Crea un`ChartXValue` istanza delDateTime tipo. |
| static [FromDouble](../../aspose.words.drawing.charts/chartxvalue/fromdouble/)(*double*) | Crea un`ChartXValue` istanza delDouble tipo. |
| static [FromMultilevelValue](../../aspose.words.drawing.charts/chartxvalue/frommultilevelvalue/)(*[ChartMultilevelValue](../chartmultilevelvalue/)*) | Crea un`ChartXValue` istanza delMultilevel tipo. |
| static [FromString](../../aspose.words.drawing.charts/chartxvalue/fromstring/)(*string*) | Crea un`ChartXValue` istanza delString tipo. |
| static [FromTimeSpan](../../aspose.words.drawing.charts/chartxvalue/fromtimespan/)(*TimeSpan*) | Crea un`ChartXValue` istanza delTime tipo. |
| override [Equals](../../aspose.words.drawing.charts/chartxvalue/equals/)(*object*) | Ottiene un flag che indica se l'oggetto specificato è uguale al valore X corrente dell'oggetto. |
| override [GetHashCode](../../aspose.words.drawing.charts/chartxvalue/gethashcode/)() | Ottiene un codice hash per l'oggetto valore X corrente. |

## Osservazioni

Questa classe contiene diversi metodi statici per creare un valore X di un tipo particolare. The [`ValueType`](./valuetype/) La proprietà consente di determinare il tipo di un valore X esistente.

Tutti i valori X non nulli di una serie di grafici devono essere uguali[`ChartXValueType`](../chartxvaluetype/) tipo.

## Esempi

Mostra come popolare le serie di grafici con i dati.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Cancella i valori X e Y della prima serie.
series1.ClearValues();

// Popola la serie con i dati.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// Cancella i valori X e Y della seconda serie.
series2.Clear();

// Popola la serie con i dati.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)
