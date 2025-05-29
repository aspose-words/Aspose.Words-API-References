---
title: ChartStyle Enum
linktitle: ChartStyle
articleTitle: ChartStyle
second_title: Aspose.Words para .NET
description: Aplique estilos de gráficos predefinidos en Aspose.Words. Mejore las imágenes con la enumeración ChartStyle para un formato profesional de documentos.
type: docs
weight: 1130
url: /es/net/aspose.words.drawing.charts/chartstyle/
---
## ChartStyle enumeration

Especifica estilos predefinidos de un gráfico.

```csharp
public enum ChartStyle
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Normal | `0` | Representa el estilo de gráfico predeterminado. |
| Muted | `1` | Un estilo con colores apagados. |
| Saturated | `2` | Un estilo con colores más saturados. |
| Shaded | `3` | Un estilo con puntos de datos sombreados. |
| Flat | `4` | Un estilo con puntos de datos planos sin degradado. |
| Shadowed | `5` | Un estilo con puntos de datos que tienen una sombra. |
| Gradient | `6` | Un estilo con relleno degradado de puntos de datos. |
| Original | `7` | Un estilo con la apariencia original de un gráfico. |
| Transparent1 | `8` | Un estilo con puntos de datos transparentes. |
| Transparent2 | `9` | Un estilo con puntos de datos transparentes. |
| Outline | `10` | Un estilo con puntos de datos que no tienen relleno, sino solo un contorno. |
| OutlineBlack | `11` | Un estilo con fondo de gráfico negro, en el que los puntos de datos no tienen relleno, sino solo un contorno. |
| Black | `12` | Un estilo con fondo de gráfico negro. |
| Grey | `13` | Un estilo con fondo de gráfico degradado gris. |
| Blue | `14` | Un estilo con fondo de gráfico azul. |
| ShadedPlot | `15` | Un estilo en el que el área del gráfico está sombreada. |

## Ejemplos

Muestra cómo establecer y obtener el estilo del gráfico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar un gráfico en el estilo Negro.
builder.InsertChart(ChartType.Column, 400, 250, ChartStyle.Black);

doc.Save(ArtifactsDir + "Charts.SetChartStyle.docx");

doc = new Document(ArtifactsDir + "Charts.SetChartStyle.docx");

// Obtener un gráfico para actualizar.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Chart chart = shape.Chart;

// Obtener el estilo del gráfico.
Assert.AreEqual(ChartStyle.Black, chart.Style);
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
