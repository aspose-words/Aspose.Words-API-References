---
title: ChartDataLabelPosition Enum
linktitle: ChartDataLabelPosition
articleTitle: ChartDataLabelPosition
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.ChartDataLabelPosition para personalizar fácilmente las etiquetas de datos de sus gráficos para mejorar la claridad y la presentación.
type: docs
weight: 960
url: /es/net/aspose.words.drawing.charts/chartdatalabelposition/
---
## ChartDataLabelPosition enumeration

Especifica la posición de una etiqueta de datos de gráfico.

```csharp
public enum ChartDataLabelPosition
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Center | `0` | Especifica que una etiqueta de datos debe mostrarse centrada en un marcador de datos. |
| Left | `1` | Especifica que se debe mostrar una etiqueta de datos a la izquierda de un marcador de datos. |
| Right | `2` | Especifica que se debe mostrar una etiqueta de datos a la derecha de un marcador de datos. |
| Above | `3` | Especifica que se debe mostrar una etiqueta de datos encima de un marcador de datos. |
| Below | `4` | Especifica que se debe mostrar una etiqueta de datos debajo de un marcador de datos. |
| InsideBase | `5` | Especifica que se debe mostrar una etiqueta de datos dentro de la base de un marcador de datos. |
| InsideEnd | `6` | Especifica que se debe mostrar una etiqueta de datos dentro del final de un marcador de datos. |
| OutsideEnd | `7` | Especifica que una etiqueta de datos debe mostrarse fuera del final de un marcador de datos. |
| BestFit | `8` | Especifica que una etiqueta de datos debe mostrarse en la posición más adecuada. |

## Observaciones

No todos los tipos de series permiten especificar la posición de las etiquetas. Y las que sí lo permiten no admiten todos los valores.

## Ejemplos

Muestra cómo establecer la posición de la etiqueta de datos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar gráfico de columnas.
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

//Eliminar serie generada por defecto.
seriesColl.Clear();

//Añadir serie.
ChartSeries series = seriesColl.Add(
    "Series 1",
    new string[] { "Category 1", "Category 2", "Category 3" },
    new double[] { 4, 5, 6 });

// Mostrar etiquetas de datos y establecer el color de fuente.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.Font.Color = Color.White;

// Establecer la posición de la etiqueta de datos.
dataLabels.Position = ChartDataLabelPosition.InsideBase;
dataLabels[0].Position = ChartDataLabelPosition.OutsideEnd;
dataLabels[0].Font.Color = Color.DarkRed;

doc.Save(ArtifactsDir + "Charts.LabelPosition.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
