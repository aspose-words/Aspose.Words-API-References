---
title: ChartDataLabelCollection.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words para .NET
description: Descubra la propiedad Posición de ChartDataLabelCollection para personalizar fácilmente las posiciones de las etiquetas de datos para una mejor visualización y claridad de los datos.
type: docs
weight: 70
url: /es/net/aspose.words.drawing.charts/chartdatalabelcollection/position/
---
## ChartDataLabelCollection.Position property

Obtiene o establece la posición de las etiquetas de datos.

```csharp
public ChartDataLabelPosition Position { get; set; }
```

## Observaciones

Se puede configurar la posición para las etiquetas de datos de los siguientes tipos de series de gráficos:

-Bar ,Column , Histogram ,Pareto , Waterfall ; valores permitidos:Center , InsideBase ,InsideEnd y OutsideEnd;

-BarStacked ,BarPercentStacked , ColumnStacked ,ColumnPercentStacked ; valores permitidos :Center ,InsideBase yInsideEnd;

-Bubble ,Bubble3D , Line ,LineStacked , LinePercentStacked ,Scatter , Stock ; valores permitidos:Center , Left ,Right , Above yBelow;

-Pie ,Pie3D , PieOfBar ,PieOfPie ; valores permitidos: Center ,InsideEnd , OutsideEnd yBestFit;

-BoxAndWhisker ; valores permitidos: Left ,Right , Above yBelow.

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

* enum [ChartDataLabelPosition](../../chartdatalabelposition/)
* class [ChartDataLabelCollection](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
