---
title: ChartDataLabelCollection.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words para .NET
description: Descubra la propiedad Orientación de ChartDataLabelCollection para personalizar fácilmente la orientación del texto de sus etiquetas de datos, mejorando la claridad y el impacto de su gráfico.
type: docs
weight: 60
url: /es/net/aspose.words.drawing.charts/chartdatalabelcollection/orientation/
---
## ChartDataLabelCollection.Orientation property

Obtiene o establece la orientación del texto de las etiquetas de datos de toda la serie.

```csharp
public ShapeTextOrientation Orientation { get; set; }
```

## Observaciones

El valor predeterminado esHorizontal .

## Ejemplos

Muestra cómo cambiar la orientación y la rotación de las etiquetas de datos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
ChartSeries series = shape.Chart.Series[0];
ChartDataLabelCollection dataLabels = series.DataLabels;

// Mostrar etiquetas de datos.
series.HasDataLabels = true;
dataLabels.ShowValue = true;
dataLabels.ShowCategoryName = true;

// Define la forma de la etiqueta de datos.
dataLabels.Format.ShapeType = ChartShapeType.UpArrow;
dataLabels.Format.Stroke.Fill.Solid(Color.DarkBlue);

// Establezca la orientación y rotación de la etiqueta de datos para toda la serie.
dataLabels.Orientation = ShapeTextOrientation.VerticalFarEast;
dataLabels.Rotation = -45;

// Cambiar la orientación y rotación de la primera etiqueta de datos.
dataLabels[0].Orientation = ShapeTextOrientation.Horizontal;
dataLabels[0].Rotation = 45;

doc.Save(ArtifactsDir + "Charts.LabelOrientationRotation.docx");
```

### Ver también

* enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* class [ChartDataLabelCollection](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
