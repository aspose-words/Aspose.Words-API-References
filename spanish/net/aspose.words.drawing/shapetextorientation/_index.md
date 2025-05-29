---
title: ShapeTextOrientation Enum
linktitle: ShapeTextOrientation
articleTitle: ShapeTextOrientation
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Drawing.ShapeTextOrientation para controlar fácilmente la orientación del texto en formas, mejorando el diseño y la legibilidad de su documento.
type: docs
weight: 1680
url: /es/net/aspose.words.drawing/shapetextorientation/
---
## ShapeTextOrientation enumeration

Especifica la orientación del texto en las formas.

```csharp
public enum ShapeTextOrientation
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Horizontal | `0` | El texto está dispuesto horizontalmente (lr-tb). |
| Downward | `1` | El texto se gira 90 grados hacia la derecha para aparecer de arriba a abajo (tb-rl). |
| Upward | `2` | El texto se gira 90 grados hacia la izquierda para aparecer de abajo hacia arriba (bt-lr). |
| VerticalFarEast | `3` | Los caracteres del Lejano Oriente aparecen en vertical, el resto del texto se gira 90 grados hacia la derecha para aparecer de arriba a abajo (tb-rl-v). |
| VerticalRotatedFarEast | `4` | Los caracteres del Lejano Oriente aparecen en vertical, el resto del texto se gira 90 grados hacia la derecha para aparecer de arriba a abajo verticalmente y luego de izquierda a derecha horizontalmente (tb-lr-v). |
| WordArtVertical | `5` | El texto es vertical, con una letra encima de la otra. |
| WordArtVerticalRightToLeft | `6` | El texto es vertical, con una letra encima de la otra, y luego de derecha a izquierda horizontalmente. |

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

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
