---
title: ChartSeries.YValues
linktitle: YValues
articleTitle: YValues
second_title: Aspose.Words per .NET
description: Scopri la proprietà ChartSeries YValues per accedere a una potente raccolta di valori Y, migliorando le tue capacità di visualizzazione e analisi dei dati.
type: docs
weight: 150
url: /it/net/aspose.words.drawing.charts/chartseries/yvalues/
---
## ChartSeries.YValues property

Ottiene una raccolta di valori Y per questa serie di grafici.

```csharp
public ChartYValueCollection YValues { get; }
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

* class [ChartYValueCollection](../../chartyvaluecollection/)
* class [ChartSeries](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
