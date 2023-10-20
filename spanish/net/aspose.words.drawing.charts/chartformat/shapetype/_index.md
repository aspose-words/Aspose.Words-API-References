---
title: ChartFormat.ShapeType
linktitle: ShapeType
articleTitle: ShapeType
second_title: Aspose.Words para .NET
description: ChartFormat ShapeType propiedad. Obtiene o establece el tipo de forma del elemento del gráfico principal en C#.
type: docs
weight: 20
url: /es/net/aspose.words.drawing.charts/chartformat/shapetype/
---
## ChartFormat.ShapeType property

Obtiene o establece el tipo de forma del elemento del gráfico principal.

```csharp
public ChartShapeType ShapeType { get; set; }
```

## Observaciones

Actualmente, la propiedad solo se puede utilizar para etiquetas de datos.

## Ejemplos

Muestra cómo configurar el formato de relleno, trazo y llamada para las etiquetas de datos del gráfico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Eliminar la serie generada por defecto.
chart.Series.Clear();

// Agregar nueva serie.
ChartSeries series = chart.Series.Add("AW Series 1",
    new string[] { "AW Category 1", "AW Category 2", "AW Category 3", "AW Category 4" },
    new double[] { 100, 200, 300, 400 });

// Mostrar etiquetas de datos.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;

// Formatear etiquetas de datos como llamadas.
ChartFormat format = series.DataLabels.Format;
format.ShapeType = ChartShapeType.WedgeRectCallout;
format.Stroke.Color = Color.DarkGreen;
format.Fill.Solid(Color.Green);
series.DataLabels.Font.Color = Color.Yellow;

// Cambiar el relleno y el trazo de una etiqueta de datos individual.
ChartFormat labelFormat = series.DataLabels[0].Format;
labelFormat.Stroke.Color = Color.DarkBlue;
labelFormat.Fill.Solid(Color.Blue);

doc.Save(ArtifactsDir + "Charts.FormatDataLables.docx");
```

### Ver también

* enum [ChartShapeType](../../chartshapetype/)
* class [ChartFormat](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
