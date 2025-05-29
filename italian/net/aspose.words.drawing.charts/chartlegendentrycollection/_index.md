---
title: ChartLegendEntryCollection Class
linktitle: ChartLegendEntryCollection
articleTitle: ChartLegendEntryCollection
second_title: Aspose.Words per .NET
description: Esplora Aspose.Words.ChartLegendEntryCollection per gestire in modo efficiente le voci della legenda dei grafici e migliorare facilmente l'aspetto visivo dei tuoi documenti.
type: docs
weight: 1030
url: /it/net/aspose.words.drawing.charts/chartlegendentrycollection/
---
## ChartLegendEntryCollection class

Rappresenta una raccolta di voci della legenda del grafico.

Per saperne di più, visita il[Lavorare con i grafici](https://docs.aspose.com/words/net/working-with-charts/) articolo di documentazione.

```csharp
public class ChartLegendEntryCollection : IEnumerable<ChartLegendEntry>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartlegendentrycollection/count/) { get; } | Restituisce il numero di[`ChartLegendEntry`](../chartlegendentry/) in questa raccolta. |
| [Item](../../aspose.words.drawing.charts/chartlegendentrycollection/item/) { get; } | Restituisce[`ChartLegendEntry`](../chartlegendentry/) per l'indice specificato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartlegendentrycollection/getenumerator/)() | Restituisce un oggetto enumeratore. |

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

* class [ChartLegendEntry](../chartlegendentry/)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)
