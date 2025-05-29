---
title: ChartSeries.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words per .NET
description: Ottimizza i tuoi grafici con il metodo ChartSeries Clear! Rimuovi facilmente i valori dei dati e ripristina la formattazione per un aspetto più pulito e professionale.
type: docs
weight: 170
url: /it/net/aspose.words.drawing.charts/chartseries/clear/
---
## ChartSeries.Clear method

Rimuove tutti i valori dei dati dalla serie del grafico. Il formato di tutti i singoli punti dati e delle etichette dati viene cancellato.

```csharp
public void Clear()
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

* class [ChartSeries](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
