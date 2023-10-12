---
title: ShapeBase.BoundsInPoints
second_title: Referencia de API de Aspose.Words para .NET
description: ShapeBase propiedad. Obtiene la ubicación y el tamaño del bloque contenedor de la forma en puntos en relación con el ancla de la forma superior.
type: docs
weight: 80
url: /es/net/aspose.words.drawing/shapebase/boundsinpoints/
---
## ShapeBase.BoundsInPoints property

Obtiene la ubicación y el tamaño del bloque contenedor de la forma en puntos, en relación con el ancla de la forma superior.

```csharp
public RectangleF BoundsInPoints { get; }
```

### Ejemplos

Muestra cómo verificar la forma que contiene límites de bloque.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Line, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 50, 100, 100, WrapType.None);
shape.StrokeColor = Color.Orange;

// Aunque la línea en sí ocupa poco espacio en la página del documento,
// ocupa un bloque contenedor rectangular, cuyo tamaño podemos determinar usando las propiedades "Límites".
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.Bounds);
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.BoundsInPoints);

// Crea una forma de grupo y luego establece el tamaño del bloque que lo contiene usando la propiedad "Límites".
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(0, 100, 250, 250);

Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);

// Crea un rectángulo, verifica el tamaño de su bloque delimitador y luego agrégalo a la forma del grupo.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

Assert.AreEqual(new RectangleF(700, 700, 100, 100), shape.BoundsInPoints);

group.AppendChild(shape);

// El plano de coordenadas de la forma del grupo tiene su origen en la esquina superior izquierda del bloque que lo contiene,
// y las coordenadas xey de (1000, 1000) en la esquina inferior derecha.
// La forma de nuestro grupo tiene un tamaño de 250x250 puntos, por lo que cada 4 puntos en el plano de coordenadas de la forma del grupo
// se traduce en 1 punto en el plano de coordenadas del cuerpo del documento.
// Cada forma que insertemos también reducirá su tamaño en un factor de 4.
// El cambio en la propiedad "BoundsInPoints" de la forma reflejará esto.
Assert.AreEqual(new RectangleF(175, 275, 25, 25), shape.BoundsInPoints);

doc.FirstSection.Body.FirstParagraph.AppendChild(group);

// Inserta una forma y colócala fuera de los límites del bloque contenedor de la forma del grupo.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 1000,
    Top = 1000
};

group.AppendChild(shape);

// La huella de la forma del grupo en el cuerpo del documento ha aumentado, pero el bloque contenedor sigue siendo el mismo.
Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);
Assert.AreEqual(new RectangleF(250, 350, 25, 25), shape.BoundsInPoints);

doc.Save(ArtifactsDir + "Shape.Bounds.docx");
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../shapebase/)
* asamblea [Aspose.Words](../../../)


