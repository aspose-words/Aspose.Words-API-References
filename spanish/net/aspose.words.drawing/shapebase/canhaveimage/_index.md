---
title: ShapeBase.CanHaveImage
linktitle: CanHaveImage
articleTitle: CanHaveImage
second_title: Aspose.Words para .NET
description: Descubra la propiedad CanHaveImage de ShapeBase: ¡aprenda a determinar si su tipo de forma admite imágenes para un atractivo visual mejorado!
type: docs
weight: 100
url: /es/net/aspose.words.drawing/shapebase/canhaveimage/
---
## ShapeBase.CanHaveImage property

Devuelve`verdadero` si el tipo de forma permite que la forma tenga una imagen.

```csharp
public bool CanHaveImage { get; }
```

## Observaciones

Aunque Microsoft Word tiene un tipo de forma especial para imágenes, parece que en los documentos de Microsoft Word cualquier forma excepto una forma de grupo puede tener una imagen, por lo tanto, esta propiedad devuelve`verdadero` para todas las formas excepto[`GroupShape`](../../groupshape/).

## Ejemplos

Muestra cómo insertar y rotar una imagen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar una forma con una imagen.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
Assert.True(shape.CanHaveImage);
Assert.True(shape.HasImage);

//Gira la imagen 45 grados en el sentido de las agujas del reloj.
shape.Rotation = 45;

doc.Save(ArtifactsDir + "Shape.Rotate.docx");
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
