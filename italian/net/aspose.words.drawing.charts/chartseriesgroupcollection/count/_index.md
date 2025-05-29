---
title: ChartSeriesGroupCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words per .NET
description: Scopri la proprietà Count di ChartSeriesGroupCollection, che rivela il numero totale di gruppi di serie per una visualizzazione avanzata dei dati.
type: docs
weight: 10
url: /it/net/aspose.words.drawing.charts/chartseriesgroupcollection/count/
---
## ChartSeriesGroupCollection.Count property

Restituisce il numero di gruppi di serie in questa raccolta.

```csharp
public int Count { get; }
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

* class [ChartSeriesGroupCollection](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
