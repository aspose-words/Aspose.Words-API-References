---
title: ChartAxisCollection Class
linktitle: ChartAxisCollection
articleTitle: ChartAxisCollection
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.ChartAxisCollection, su solución ideal para administrar los ejes de los gráficos de manera eficiente y mejorar la visualización de datos de sus documentos.
type: docs
weight: 900
url: /es/net/aspose.words.drawing.charts/chartaxiscollection/
---
## ChartAxisCollection class

Representa una colección de ejes de gráfico.

```csharp
public class ChartAxisCollection : IEnumerable<ChartAxis>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartaxiscollection/count/) { get; } | Obtiene el número de ejes en esta colección. |
| [Item](../../aspose.words.drawing.charts/chartaxiscollection/item/) { get; } | Obtiene el eje en el índice especificado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartaxiscollection/getenumerator/)() | Devuelve un objeto enumerador. |

## Ejemplos

Muestra cómo trabajar con la colección de ejes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Ocultar las líneas de cuadrícula principales en los ejes Y primario y secundario.
foreach (ChartAxis axis in chart.Axes)
{
    if (axis.Type == ChartAxisType.Value)
        axis.HasMajorGridlines = false;
}

doc.Save(ArtifactsDir + "Charts.AxisCollection.docx");
```

### Ver también

* class [ChartAxis](../chartaxis/)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
