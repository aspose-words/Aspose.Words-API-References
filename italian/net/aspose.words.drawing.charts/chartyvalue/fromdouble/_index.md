---
title: ChartYValue.FromDouble
linktitle: FromDouble
articleTitle: FromDouble
second_title: Aspose.Words per .NET
description: ChartYValue FromDouble metodo. Crea unChartYValue istanza delDouble tipo in C#.
type: docs
weight: 20
url: /it/net/aspose.words.drawing.charts/chartyvalue/fromdouble/
---
## ChartYValue.FromDouble method

Crea un[`ChartYValue`](../) istanza delDouble tipo.

```csharp
public static ChartYValue FromDouble(double value)
```

## Esempi

Mostra come popolare le serie di grafici con i dati.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Cancella i valori X e Y della prima serie.
series1.ClearValues();

// Compila la serie con i dati.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9), ChartYValue.FromDouble(17));

ChartSeries series2 = chart.Series[1];

// Cancella i valori X e Y della seconda serie.
series2.ClearValues();

// Compila la serie con i dati.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Guarda anche

* class [ChartYValue](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
