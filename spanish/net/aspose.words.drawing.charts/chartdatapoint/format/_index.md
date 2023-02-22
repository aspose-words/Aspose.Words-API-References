---
title: ChartDataPoint.Format
second_title: Referencia de API de Aspose.Words para .NET
description: ChartDataPoint propiedad. Proporciona acceso al formato de relleno y línea de este punto de datos.
type: docs
weight: 30
url: /es/net/aspose.words.drawing.charts/chartdatapoint/format/
---
## ChartDataPoint.Format property

Proporciona acceso al formato de relleno y línea de este punto de datos.

```csharp
public ChartFormat Format { get; }
```

### Ejemplos

Muestra cómo configurar el formato individual para las categorías de un gráfico de columnas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Elimina la serie generada por defecto.
chart.Series.Clear();

// Agregando nueva serie.
ChartSeries series = chart.Series.Add("Series 1",
    new[] { "Category 1", "Category 2", "Category 3", "Category 4" },
    new double[] { 1, 2, 3, 4 });

// Establecer formato de columna.
ChartDataPointCollection dataPoints = series.DataPoints;
dataPoints[0].Format.Fill.PresetTextured(PresetTexture.Denim);
dataPoints[1].Format.Fill.ForeColor = Color.Red;
dataPoints[2].Format.Fill.ForeColor = Color.Yellow;
dataPoints[3].Format.Fill.ForeColor = Color.Blue;

doc.Save(ArtifactsDir + "Charts.DataPointsFormatting.docx");
```

### Ver también

* class [ChartFormat](../../chartformat/)
* class [ChartDataPoint](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../chartdatapoint/)
* asamblea [Aspose.Words](../../../)


