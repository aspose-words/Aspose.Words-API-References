---
title: ChartSeriesGroupCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words per .NET
description: Rimuovi senza sforzo un gruppo di serie con il metodo RemoveAt di ChartSeriesGroupCollection. Semplifica la gestione dei grafici eliminando i dati indesiderati.
type: docs
weight: 50
url: /it/net/aspose.words.drawing.charts/chartseriesgroupcollection/removeat/
---
## ChartSeriesGroupCollection.RemoveAt method

Rimuove un gruppo di serie all'indice specificato. Tutte le serie figlie verranno rimosse dal grafico.

```csharp
public void RemoveAt(int index)
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
