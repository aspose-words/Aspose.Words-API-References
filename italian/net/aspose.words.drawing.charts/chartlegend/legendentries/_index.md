---
title: ChartLegend.LegendEntries
linktitle: LegendEntries
articleTitle: LegendEntries
second_title: Aspose.Words per .NET
description: Esplora la proprietà ChartLegend LegendEntries per accedere a una raccolta completa di voci di legenda per tutte le serie e le linee di tendenza nel tuo grafico.
type: docs
weight: 30
url: /it/net/aspose.words.drawing.charts/chartlegend/legendentries/
---
## ChartLegend.LegendEntries property

Restituisce una raccolta di voci della legenda per tutte le serie e le linee di tendenza del grafico padre.

```csharp
public ChartLegendEntryCollection LegendEntries { get; }
```

## Esempi

Mostra come lavorare con una voce di legenda per le serie di grafici.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "AW Category 1", "AW Category 2" };

ChartSeries series1 = series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });
series.Add("Series 3", categories, new double[] { 5, 6 });
series.Add("Series 4", categories, new double[] { 0, 0 });

ChartLegendEntryCollection legendEntries = chart.Legend.LegendEntries;
legendEntries[3].IsHidden = true;

doc.Save(ArtifactsDir + "Charts.LegendEntries.docx");
```

### Guarda anche

* class [ChartLegendEntryCollection](../../chartlegendentrycollection/)
* class [ChartLegend](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
