---
title: ChartXValue.FromDouble
linktitle: FromDouble
articleTitle: FromDouble
second_title: Aspose.Words per .NET
description: Scopri il metodo ChartXValue FromDouble per creare senza sforzo istanze di ChartXValue di tipo Double, migliorando le tue capacità di visualizzazione dei dati.
type: docs
weight: 20
url: /it/net/aspose.words.drawing.charts/chartxvalue/fromdouble/
---
## ChartXValue.FromDouble method

Crea un[`ChartXValue`](../) istanza delDouble tipo.

```csharp
public static ChartXValue FromDouble(double value)
```

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

* class [ChartXValue](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
