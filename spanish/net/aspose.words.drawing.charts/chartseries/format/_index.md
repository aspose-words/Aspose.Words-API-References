---
title: ChartSeries.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words para .NET
description: Descubra la propiedad Formato ChartSeries para acceder sin esfuerzo a estilos de relleno y línea personalizables, mejorando su experiencia de visualización de datos.
type: docs
weight: 60
url: /es/net/aspose.words.drawing.charts/chartseries/format/
---
## ChartSeries.Format property

Proporciona acceso al relleno y formato de línea de la serie.

```csharp
public ChartFormat Format { get; }
```

## Ejemplos

Siembra cómo configurar el color de la serie.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

//Eliminar serie generada por defecto.
seriesColl.Clear();

// Crea una matriz de nombres de categorías.
string[] categories = new[] { "Category 1", "Category 2" };

// Añadiendo nueva serie. Las matrices de valores y categorías deben tener el mismo tamaño.
ChartSeries series1 = seriesColl.Add("Series 1", categories, new double[] { 1, 2 });
ChartSeries series2 = seriesColl.Add("Series 2", categories, new double[] { 3, 4 });
ChartSeries series3 = seriesColl.Add("Series 3", categories, new double[] { 5, 6 });

// Establecer el color de la serie.
series1.Format.Fill.ForeColor = Color.Red;
series2.Format.Fill.ForeColor = Color.Yellow;
series3.Format.Fill.ForeColor = Color.Blue;

doc.Save(ArtifactsDir + "Charts.SeriesColor.docx");
```

### Ver también

* class [ChartFormat](../../chartformat/)
* class [ChartSeries](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
