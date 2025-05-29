---
title: AxisTickLabels.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words para .NET
description: Ajuste la rotación de AxisTickLabels para una legibilidad óptima. Personalice los ángulos de las etiquetas de marca en grados para mejorar la claridad y el atractivo visual de su gráfico.
type: docs
weight: 70
url: /es/net/aspose.words.drawing.charts/axisticklabels/rotation/
---
## AxisTickLabels.Rotation property

Obtiene o establece la rotación de las etiquetas de las marcas en grados.

```csharp
public int Rotation { get; set; }
```

## Observaciones

El rango de valores aceptables va de -180 a 180 inclusive. El valor predeterminado es 0.

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

* class [AxisTickLabels](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
