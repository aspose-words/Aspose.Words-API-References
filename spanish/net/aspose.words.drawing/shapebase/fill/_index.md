---
title: Fill
second_title: Referencia de API de Aspose.Words para .NET
description: Obtiene el formato de relleno para la forma.
type: docs
weight: 170
url: /es/net/aspose.words.drawing/shapebase/fill/
---
## ShapeBase.Fill property

Obtiene el formato de relleno para la forma.

```csharp
public Fill Fill { get; }
```

### Ejemplos

Muestra cómo rellenar una forma con un color sólido.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Escribe algo de texto y luego cúbrelo con una forma flotante.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Usa la propiedad "StrokeColor" para establecer el color del contorno de la forma.
shape.StrokeColor = Color.CadetBlue;

// Use la propiedad "FillColor" para establecer el color del área interior de la forma.
shape.FillColor = Color.LightBlue;

// La propiedad "Opacidad" determina qué tan transparente es el color en una escala de 0-1,
// siendo 1 totalmente opaco y 0 invisible.
// El relleno de forma predeterminado es totalmente opaco, por lo que no podemos ver el texto sobre el que se encuentra esta forma.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Establezca la opacidad del color de relleno de la forma en un valor más bajo para que podamos ver el texto debajo.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Ver también

* class [Fill](../../fill)
* class [ShapeBase](../../shapebase)
* espacio de nombres [Aspose.Words.Drawing](../../shapebase)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
