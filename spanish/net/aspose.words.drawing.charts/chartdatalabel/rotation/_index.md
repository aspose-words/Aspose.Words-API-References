---
title: ChartDataLabel.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words para .NET
description: Descubra la propiedad Rotación de ChartDataLabel para personalizar fácilmente los ángulos de las etiquetas en sus gráficos. ¡Mejore la visualización de datos con un control preciso!
type: docs
weight: 110
url: /es/net/aspose.words.drawing.charts/chartdatalabel/rotation/
---
## ChartDataLabel.Rotation property

Obtiene o establece la rotación de la etiqueta en grados.

```csharp
public int Rotation { get; set; }
```

## Observaciones

El rango de valores aceptables va de -180 a 180 inclusive. El valor predeterminado es 0.

Si el[`Orientation`](../orientation/) El valor esHorizontalLa forma de la etiqueta , si existe, se rota junto con el texto de la etiqueta. De lo contrario, solo se rota el texto de la etiqueta.

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

* class [ChartDataLabel](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
