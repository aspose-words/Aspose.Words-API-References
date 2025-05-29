---
title: ChartSeriesGroupCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words para .NET
description: Acceda a ChartSeriesGroup por índice con la propiedad Item. ¡Simplifique la visualización de datos y mejore su experiencia de gráficos sin esfuerzo!
type: docs
weight: 20
url: /es/net/aspose.words.drawing.charts/chartseriesgroupcollection/item/
---
## ChartSeriesGroupCollection indexer

Devuelve un[`ChartSeriesGroup`](../../chartseriesgroup/) en el índice especificado.

```csharp
public ChartSeriesGroup this[int index] { get; }
```

## Ejemplos

Muestra cómo quitar el eje secundario.

```csharp
Document doc = new Document(MyDir + "Combo chart.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Chart chart = shape.Chart;
ChartSeriesGroupCollection seriesGroups = chart.SeriesGroups;

// Encuentra el eje secundario y elimínalo de la colección.
for (int i = 0; i < seriesGroups.Count; i++)
    if (seriesGroups[i].AxisGroup == AxisGroup.Secondary)
        seriesGroups.RemoveAt(i);
```

### Ver también

* class [ChartSeriesGroup](../../chartseriesgroup/)
* class [ChartSeriesGroupCollection](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
