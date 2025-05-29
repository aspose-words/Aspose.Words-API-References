---
title: Shape.FillColor
linktitle: FillColor
articleTitle: FillColor
second_title: Aspose.Words para .NET
description: Descubra la propiedad Shape FillColor para personalizar sus diseños con colores de pincel vibrantes que realzan sus formas y elevan sus proyectos.
type: docs
weight: 50
url: /es/net/aspose.words.drawing/shape/fillcolor/
---
## Shape.FillColor property

Define el color del pincel que rellena la ruta cerrada de la forma.

```csharp
public Color FillColor { get; set; }
```

## Observaciones

Este es un acceso directo a la[`Color`](../../fill/color/) propiedad.

El valor predeterminado es White .

## Ejemplos

Muestra cómo rellenar una forma con un color sólido.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Escribe un texto y luego cúbrelo con una forma flotante.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Utilice la propiedad "StrokeColor" para establecer el color del contorno de la forma.
shape.StrokeColor = Color.CadetBlue;

// Utilice la propiedad "FillColor" para establecer el color del área interior de la forma.
shape.FillColor = Color.LightBlue;

// La propiedad "Opacidad" determina qué tan transparente es el color en una escala de 0 a 1,
// siendo 1 completamente opaco y 0 invisible.
//El relleno de la forma por defecto es totalmente opaco, por lo que no podemos ver el texto sobre el que se encuentra esta forma.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Establezca la opacidad del color de relleno de la forma en un valor más bajo para que podamos ver el texto debajo de él.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Ver también

* class [Shape](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
