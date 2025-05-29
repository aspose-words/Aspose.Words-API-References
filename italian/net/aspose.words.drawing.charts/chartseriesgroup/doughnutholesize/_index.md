---
title: ChartSeriesGroup.DoughnutHoleSize
linktitle: DoughnutHoleSize
articleTitle: DoughnutHoleSize
second_title: Aspose.Words per .NET
description: Scopri la proprietà DoughnutHoleSize di ChartSeriesGroup per personalizzare facilmente la percentuale di dimensione del foro del tuo grafico a ciambella, per una migliore visualizzazione dei dati.
type: docs
weight: 50
url: /it/net/aspose.words.drawing.charts/chartseriesgroup/doughnutholesize/
---
## ChartSeriesGroup.DoughnutHoleSize property

Ottiene o imposta la dimensione del foro del grafico a ciambella padre come percentuale.

```csharp
public int DoughnutHoleSize { get; set; }
```

## Osservazioni

Si applica solo ai gruppi di serie diDoughnut tipo.

L'intervallo di valori accettabili è compreso tra 0 e 90 (inclusi). Il valore predefinito è 75.

## Esempi

Mostra come creare e formattare un grafico ad ciambella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Doughnut, 400, 400);
Chart chart = shape.Chart;
// Elimina la serie generata di default.
chart.Series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3" };
chart.Series.Add("Series 1", categories, new double[] { 4, 2, 5 });

// Formatta il grafico ad ciambella.
ChartSeriesGroup seriesGroup = chart.SeriesGroups[0];
seriesGroup.DoughnutHoleSize = 10;
seriesGroup.FirstSliceAngle = 270;

doc.Save(ArtifactsDir + "Charts.DoughnutChart.docx");
```

### Guarda anche

* class [ChartSeriesGroup](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
