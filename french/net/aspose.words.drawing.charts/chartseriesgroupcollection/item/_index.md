---
title: ChartSeriesGroupCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words pour .NET
description: Accédez à ChartSeriesGroup par index avec la propriété Item. Simplifiez la visualisation de vos données et améliorez votre expérience graphique sans effort !
type: docs
weight: 20
url: /fr/net/aspose.words.drawing.charts/chartseriesgroupcollection/item/
---
## ChartSeriesGroupCollection indexer

Renvoie un[`ChartSeriesGroup`](../../chartseriesgroup/) à l'index spécifié.

```csharp
public ChartSeriesGroup this[int index] { get; }
```

## Exemples

Montrez comment supprimer l'axe secondaire.

```csharp
Document doc = new Document(MyDir + "Combo chart.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Chart chart = shape.Chart;
ChartSeriesGroupCollection seriesGroups = chart.SeriesGroups;

// Rechercher l'axe secondaire et le supprimer de la collection.
for (int i = 0; i < seriesGroups.Count; i++)
    if (seriesGroups[i].AxisGroup == AxisGroup.Secondary)
        seriesGroups.RemoveAt(i);
```

### Voir également

* class [ChartSeriesGroup](../../chartseriesgroup/)
* class [ChartSeriesGroupCollection](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
