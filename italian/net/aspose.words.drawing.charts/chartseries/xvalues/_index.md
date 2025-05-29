---
title: ChartSeries.XValues
linktitle: XValues
articleTitle: XValues
second_title: Aspose.Words per .NET
description: Scopri la proprietà ChartSeries XValues per accedere a una potente raccolta di valori X, migliorando la visualizzazione e l'analisi dei dati.
type: docs
weight: 140
url: /it/net/aspose.words.drawing.charts/chartseries/xvalues/
---
## ChartSeries.XValues property

Ottiene una raccolta di valori X per questa serie di grafici.

```csharp
public ChartXValueCollection XValues { get; }
```

## Esempi

Mostra come lavorare con il codice di formato dei dati del grafico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un grafico a bolle.
Shape shape = builder.InsertChart(ChartType.Bubble, 432, 252);
Chart chart = shape.Chart;

// Elimina la serie generata di default.
chart.Series.Clear();

ChartSeries series = chart.Series.Add(
    "Series1",
    new double[] { 1, 1.9, 2.45, 3 },
    new double[] { 1, -0.9, 1.82, 0 },
    new double[] { 2, 1.1, 2.95, 2 });

// Mostra le etichette dei dati.
series.HasDataLabels = true;
series.DataLabels.ShowCategoryName = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowBubbleSize = true;

// Imposta i codici del formato dei dati.
series.XValues.FormatCode = "#,##0.0#";
series.YValues.FormatCode = "#,##0.0#;[Red]\\-#,##0.0#";
series.BubbleSizes.FormatCode = "#,##0.0#";

doc.Save(ArtifactsDir + "Charts.FormatCode.docx");
```

### Guarda anche

* class [ChartXValueCollection](../../chartxvaluecollection/)
* class [ChartSeries](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
