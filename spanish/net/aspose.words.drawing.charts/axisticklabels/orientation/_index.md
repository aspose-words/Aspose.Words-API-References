---
title: AxisTickLabels.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words para .NET
description: Personaliza la orientación de tus AxisTickLabels para una legibilidad óptima. Ajusta fácilmente la dirección del texto de las etiquetas de marca para mejorar la visualización de tus datos.
type: docs
weight: 50
url: /es/net/aspose.words.drawing.charts/axisticklabels/orientation/
---
## AxisTickLabels.Orientation property

Obtiene o establece la orientación del texto de la etiqueta de marca.

```csharp
public ShapeTextOrientation Orientation { get; set; }
```

## Observaciones

El valor predeterminado esHorizontal.

Tenga en cuenta que algunos[`ShapeTextOrientation`](../../../aspose.words.drawing/shapetextorientation/) Los valores no afectan la orientación de la etiqueta de marca text en los ejes de valores.

## Ejemplos

Muestra cómo cambiar la orientación y la rotación de las etiquetas de las marcas de los ejes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar un gráfico de columnas.
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
AxisTickLabels xTickLabels = shape.Chart.AxisX.TickLabels;
AxisTickLabels yTickLabels = shape.Chart.AxisY.TickLabels;

// Establecer la orientación y rotación de la etiqueta de la marca del eje.
xTickLabels.Orientation = ShapeTextOrientation.VerticalFarEast;
xTickLabels.Rotation = -30;
yTickLabels.Orientation = ShapeTextOrientation.Horizontal;
yTickLabels.Rotation = 45;

doc.Save(ArtifactsDir + "Charts.TickLabelsOrientationRotation.docx");
```

### Ver también

* enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* class [AxisTickLabels](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
