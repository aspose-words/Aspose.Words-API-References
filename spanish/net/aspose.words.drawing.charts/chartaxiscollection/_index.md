---
title: ChartAxisCollection Class
linktitle: ChartAxisCollection
articleTitle: ChartAxisCollection
second_title: Aspose.Words para .NET
description: Aspose.Words.Drawing.Charts.ChartAxisCollection clase. Representa una colección de ejes del gráfico en C#.
type: docs
weight: 640
url: /es/net/aspose.words.drawing.charts/chartaxiscollection/
---
## ChartAxisCollection class

Representa una colección de ejes del gráfico.

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

// Ocultar las líneas principales de la cuadrícula en los ejes Y primario y secundario.
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
