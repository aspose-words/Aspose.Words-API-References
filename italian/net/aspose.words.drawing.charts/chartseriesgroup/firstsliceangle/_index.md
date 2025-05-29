---
title: ChartSeriesGroup.FirstSliceAngle
linktitle: FirstSliceAngle
articleTitle: FirstSliceAngle
second_title: Aspose.Words per .NET
description: Scopri la proprietà FirstSliceAngle di ChartSeriesGroup per personalizzare in gradi l'angolo della prima fetta del tuo grafico a torta, per una migliore visualizzazione dei dati.
type: docs
weight: 60
url: /it/net/aspose.words.drawing.charts/chartseriesgroup/firstsliceangle/
---
## ChartSeriesGroup.FirstSliceAngle property

Ottiene o imposta l'angolo, in gradi, della prima fetta del grafico a torta padre.

```csharp
public int FirstSliceAngle { get; set; }
```

## Osservazioni

Si applica ai gruppi di serie diPie ,Pie3D eDoughnut tipi.

L'intervallo di valori accettabili è compreso tra 0 e 360 (inclusi). Il valore predefinito è 0.

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
