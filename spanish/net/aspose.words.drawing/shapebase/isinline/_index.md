---
title: ShapeBase.IsInline
second_title: Referencia de API de Aspose.Words para .NET
description: ShapeBase propiedad. Una forma rápida de determinar si esta forma está colocada en línea con el texto.
type: docs
weight: 290
url: /es/net/aspose.words.drawing/shapebase/isinline/
---
## ShapeBase.IsInline property

Una forma rápida de determinar si esta forma está colocada en línea con el texto.

```csharp
public bool IsInline { get; }
```

### Observaciones

Tiene efecto sólo para formas de nivel superior.

### Ejemplos

Muestra cómo determinar si una forma está en línea o flotante.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// A continuación se muestran dos tipos de envoltura que pueden tener las formas.
// 1 - En línea:
builder.Write("Hello world! ");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.FillColor = Color.LightBlue;
builder.Write(" Hello again.");

// Una forma en línea se encuentra dentro de un párrafo, entre otros elementos del párrafo, como corridas de texto.
// En Microsoft Word, podemos hacer clic y arrastrar la forma a cualquier párrafo como si fuera un carácter.
// Si la forma es grande, afectará el espaciado vertical del párrafo.
// No podemos mover esta forma a un lugar sin párrafo.
Assert.AreEqual(WrapType.Inline, shape.WrapType);
Assert.True(shape.IsInline);

// 2 - Flotante:
shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin ,200, 
    RelativeVerticalPosition.TopMargin ,200, 100, 100, WrapType.None);
shape.FillColor = Color.Orange;

// Una forma flotante pertenece al párrafo en el que la insertamos,
// que podemos determinar mediante un símbolo de ancla que aparece cuando hacemos clic en la forma.
// Si la forma no tiene un símbolo de ancla visible a su izquierda,
// necesitaremos habilitar anclajes visibles a través de "Opciones" -> "Pantalla" -> "Anclajes de objetos".
// En Microsoft Word, podemos hacer clic izquierdo y arrastrar esta forma libremente a cualquier ubicación.
Assert.AreEqual(WrapType.None, shape.WrapType);
Assert.False(shape.IsInline);

doc.Save(ArtifactsDir + "Shape.IsInline.docx");
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../shapebase/)
* asamblea [Aspose.Words](../../../)


