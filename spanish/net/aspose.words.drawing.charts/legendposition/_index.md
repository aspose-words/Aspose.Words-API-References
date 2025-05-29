---
title: LegendPosition Enum
linktitle: LegendPosition
articleTitle: LegendPosition
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Drawing.Charts.LegendPosition para personalizar fácilmente la posición de la leyenda de su gráfico para una mejor visualización de datos.
type: docs
weight: 1230
url: /es/net/aspose.words.drawing.charts/legendposition/
---
## LegendPosition enumeration

Especifica las posibles posiciones para una leyenda de gráfico.

```csharp
public enum LegendPosition
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | No se mostrará ninguna leyenda para el gráfico. |
| Bottom | `1` | Especifica que la leyenda se dibujará en la parte inferior del gráfico. |
| Left | `2` | Especifica que la leyenda se dibujará a la izquierda del gráfico. |
| Right | `3` | Especifica que la leyenda se dibujará a la derecha del gráfico. |
| Top | `4` | Especifica que la leyenda se dibujará en la parte superior del gráfico. |
| TopRight | `5` | Especifica que la leyenda se dibujará en la parte superior derecha del gráfico. |

## Ejemplos

Muestra cómo editar la apariencia de la leyenda de un gráfico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 300);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Mueve la leyenda del gráfico a la esquina superior derecha.
ChartLegend legend = chart.Legend;
legend.Position = LegendPosition.TopRight;

// Dale más espacio a otros elementos del gráfico, como el gráfico, permitiéndoles superponerse a la leyenda.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
