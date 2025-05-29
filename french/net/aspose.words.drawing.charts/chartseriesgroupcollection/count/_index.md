---
title: ChartSeriesGroupCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Count de ChartSeriesGroupCollection, qui révèle le nombre total de groupes de séries pour une visualisation améliorée des données.
type: docs
weight: 10
url: /fr/net/aspose.words.drawing.charts/chartseriesgroupcollection/count/
---
## ChartSeriesGroupCollection.Count property

Renvoie le nombre de groupes de séries dans cette collection.

```csharp
public int Count { get; }
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

* class [ChartSeriesGroupCollection](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
