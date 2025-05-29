---
title: ChartAxisTitle.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words para .NET
description: Descubra la propiedad ChartAxisTitle Format para personalizar fácilmente el relleno del título del eje y los estilos de línea, mejorando la visualización de sus datos.
type: docs
weight: 20
url: /es/net/aspose.words.drawing.charts/chartaxistitle/format/
---
## ChartAxisTitle.Format property

Proporciona acceso al relleno y formato de línea del título del eje.

```csharp
public ChartFormat Format { get; }
```

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

* class [ChartFormat](../../chartformat/)
* class [ChartAxisTitle](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
