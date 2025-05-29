---
title: ChartSeriesGroupCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words per .NET
description: Accedi a ChartSeriesGroup per indice con la proprietà Item. Semplifica la visualizzazione dei dati e migliora la tua esperienza di creazione di grafici senza sforzo!
type: docs
weight: 20
url: /it/net/aspose.words.drawing.charts/chartseriesgroupcollection/item/
---
## ChartSeriesGroupCollection indexer

Restituisce un[`ChartSeriesGroup`](../../chartseriesgroup/) all'indice specificato.

```csharp
public ChartSeriesGroup this[int index] { get; }
```

## Esempi

Mostra come rimuovere l'asse secondario.

```csharp
Document doc = new Document(MyDir + "Combo chart.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Chart chart = shape.Chart;
ChartSeriesGroupCollection seriesGroups = chart.SeriesGroups;

// Trova l'asse secondario e rimuovilo dalla raccolta.
for (int i = 0; i < seriesGroups.Count; i++)
    if (seriesGroups[i].AxisGroup == AxisGroup.Secondary)
        seriesGroups.RemoveAt(i);
```

### Guarda anche

* class [ChartSeriesGroup](../../chartseriesgroup/)
* class [ChartSeriesGroupCollection](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
