---
title: FlipOrientation Enum
linktitle: FlipOrientation
articleTitle: FlipOrientation
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Drawing.FlipOrientation para opciones versátiles de orientación de formas. ¡Mejore el diseño de sus documentos con personalización flexible!
type: docs
weight: 1290
url: /es/net/aspose.words.drawing/fliporientation/
---
## FlipOrientation enumeration

Valores posibles para la orientación de una forma.

```csharp
[Flags]
public enum FlipOrientation
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | Las coordenadas no están invertidas. |
| Horizontal | `1` | Gira a lo largo del eje y, invirtiendo las coordenadas x. |
| Vertical | `2` | Gira a lo largo del eje x, invirtiendo las coordenadas y. |
| Both | `3` | Gira a lo largo de los ejes y y x. |

## Ejemplos

Muestra cómo voltear una forma sobre un eje.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta una forma de imagen y deja su orientación en su estado predeterminado.
Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

Assert.AreEqual(FlipOrientation.None, shape.FlipOrientation);

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Establezca la propiedad "FlipOrientation" en "FlipOrientation.Horizontal" para voltear la segunda forma en el eje y,
// convirtiéndolo en una imagen reflejada horizontalmente de la primera forma.
shape.FlipOrientation = FlipOrientation.Horizontal;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Establezca la propiedad "FlipOrientation" en "FlipOrientation.Horizontal" para voltear la tercera forma en el eje x,
// convirtiéndolo en una imagen reflejada verticalmente de la primera forma.
shape.FlipOrientation = FlipOrientation.Vertical;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Establezca la propiedad "FlipOrientation" en "FlipOrientation.Horizontal" para voltear la cuarta forma en los ejes x e y,
// convirtiéndolo en una imagen reflejada horizontal y vertical de la primera forma.
shape.FlipOrientation = FlipOrientation.Both;

doc.Save(ArtifactsDir + "Shape.FlipShapeOrientation.docx");
```

### Ver también

* property [FlipOrientation](../shapebase/fliporientation/)
* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
