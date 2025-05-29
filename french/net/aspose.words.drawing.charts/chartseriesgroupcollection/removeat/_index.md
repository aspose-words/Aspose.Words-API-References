---
title: ChartSeriesGroupCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words pour .NET
description: Supprimez facilement un groupe de séries grâce à la méthode ChartSeriesGroupCollection RemoveAt. Simplifiez la gestion de vos graphiques en supprimant les données indésirables.
type: docs
weight: 50
url: /fr/net/aspose.words.drawing.charts/chartseriesgroupcollection/removeat/
---
## ChartSeriesGroupCollection.RemoveAt method

Supprime un groupe de séries à l'index spécifié. Toutes les séries enfants seront supprimées du graphique.

```csharp
public void RemoveAt(int index)
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
