---
title: ChartSeriesGroupCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words para .NET
description: Elimine fácilmente un grupo de series con el método ChartSeriesGroupCollection RemoveAt. Simplifique la gestión de gráficos eliminando datos no deseados.
type: docs
weight: 50
url: /es/net/aspose.words.drawing.charts/chartseriesgroupcollection/removeat/
---
## ChartSeriesGroupCollection.RemoveAt method

Elimina un grupo de series en el índice especificado. Se eliminarán todas las series secundarias del gráfico.

```csharp
public void RemoveAt(int index)
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

* class [ChartSeriesGroupCollection](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
