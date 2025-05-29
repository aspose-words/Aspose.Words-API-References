---
title: ChartFormat Class
linktitle: ChartFormat
articleTitle: ChartFormat
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.ChartFormat para crear estilos avanzados de elementos gráficos. Mejore sus documentos con diseños de gráficos profesionales y personalizables.
type: docs
weight: 1000
url: /es/net/aspose.words.drawing.charts/chartformat/
---
## ChartFormat class

Representa el formato de un elemento del gráfico.

Para obtener más información, visite el[Trabajar con gráficos](https://docs.aspose.com/words/net/working-with-charts/) Artículo de documentación.

```csharp
public class ChartFormat
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Fill](../../aspose.words.drawing.charts/chartformat/fill/) { get; } | Obtiene el formato de relleno para el elemento del gráfico principal. |
| [IsDefined](../../aspose.words.drawing.charts/chartformat/isdefined/) { get; } | Obtiene una bandera que indica si hay algún formato definido. |
| [ShapeType](../../aspose.words.drawing.charts/chartformat/shapetype/) { get; set; } | Obtiene o establece el tipo de forma del elemento del gráfico principal. |
| [Stroke](../../aspose.words.drawing.charts/chartformat/stroke/) { get; } | Obtiene el formato de línea para el elemento del gráfico principal. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [SetDefaultFill](../../aspose.words.drawing.charts/chartformat/setdefaultfill/)() | Restablece el relleno del elemento del gráfico para que tenga el valor predeterminado. |

## Ejemplos

Muestra cómo utilizar el formato de gráficos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

//Eliminar serie generada por defecto.
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2" };
series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });

// Formatear el fondo del gráfico.
chart.Format.Fill.Solid(Color.DarkSlateGray);

// Ocultar las etiquetas de las marcas de los ejes.
chart.AxisX.TickLabels.Position = AxisTickLabelPosition.None;
chart.AxisY.TickLabels.Position = AxisTickLabelPosition.None;

// Formatear el título del gráfico.
chart.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

//Formatear título del eje.
chart.AxisX.Title.Show = true;
chart.AxisX.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Formato de leyenda.
chart.Legend.Format.Fill.Solid(Color.LightGoldenrodYellow);

doc.Save(ArtifactsDir + "Charts.ChartFormat.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
