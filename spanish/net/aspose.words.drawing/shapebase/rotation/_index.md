---
title: ShapeBase.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words para .NET
description: Descubra la propiedad Rotación ShapeBase, defina y personalice fácilmente los ángulos de rotación de sus formas, mejorando la precisión y la creatividad de su diseño.
type: docs
weight: 500
url: /es/net/aspose.words.drawing/shapebase/rotation/
---
## ShapeBase.Rotation property

Define el ángulo (en grados) en que se gira una forma. El valor positivo corresponde al ángulo de rotación en el sentido de las agujas del reloj.

```csharp
public double Rotation { get; set; }
```

## Observaciones

El valor predeterminado es 0.

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
