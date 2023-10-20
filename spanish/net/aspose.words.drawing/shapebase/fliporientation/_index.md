---
title: ShapeBase.FlipOrientation
linktitle: FlipOrientation
articleTitle: FlipOrientation
second_title: Aspose.Words para .NET
description: ShapeBase FlipOrientation propiedad. Cambia la orientación de una forma en C#.
type: docs
weight: 180
url: /es/net/aspose.words.drawing/shapebase/fliporientation/
---
## ShapeBase.FlipOrientation property

Cambia la orientación de una forma.

```csharp
public FlipOrientation FlipOrientation { get; set; }
```

## Observaciones

El valor predeterminado esNone.

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

// Establece la propiedad "FlipOrientation" en "FlipOrientation.Horizontal" para voltear la segunda forma en el eje y,
// convirtiéndolo en una imagen especular horizontal de la primera forma.
shape.FlipOrientation = FlipOrientation.Horizontal;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Establece la propiedad "FlipOrientation" en "FlipOrientation.Horizontal" para voltear la tercera forma en el eje x,
// convirtiéndolo en una imagen especular vertical de la primera forma.
shape.FlipOrientation = FlipOrientation.Vertical;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Establece la propiedad "FlipOrientation" en "FlipOrientation.Horizontal" para voltear la cuarta forma en los ejes x e y,
// convirtiéndolo en una imagen especular horizontal y vertical de la primera forma.
shape.FlipOrientation = FlipOrientation.Both;

doc.Save(ArtifactsDir + "Shape.FlipShapeOrientation.docx");
```

### Ver también

* enum [FlipOrientation](../../fliporientation/)
* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
