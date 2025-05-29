---
title: ChartSeries.SeriesType
linktitle: SeriesType
articleTitle: SeriesType
second_title: Aspose.Words per .NET
description: Scopri la proprietà SeriesType di ChartSeries per identificare facilmente il tipo di serie dei tuoi grafici e migliorare la visualizzazione dei dati. Ottieni insight preziosi oggi stesso!
type: docs
weight: 120
url: /it/net/aspose.words.drawing.charts/chartseries/seriestype/
---
## ChartSeries.SeriesType property

Ottiene il tipo di questa serie di grafici.

```csharp
public ChartSeriesType SeriesType { get; }
```

## Esempi

Mostra come rimuovere serie specifiche di grafici.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

// Rimuove tutte le serie di tipo Colonna.
for (int i = chart.Series.Count - 1; i >= 0; i--)
{
    if (chart.Series[i].SeriesType == ChartSeriesType.Column)
        chart.Series.RemoveAt(i);
}

chart.Series.Add(
    "Aspose Series",
    new string[] { "Category 1", "Category 2", "Category 3", "Category 4" },
    new double[] { 5.6, 7.1, 2.9, 8.9 });

doc.Save(ArtifactsDir + "Charts.RemoveSpecificChartSeries.docx");
```

### Guarda anche

* enum [ChartSeriesType](../../chartseriestype/)
* class [ChartSeries](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
