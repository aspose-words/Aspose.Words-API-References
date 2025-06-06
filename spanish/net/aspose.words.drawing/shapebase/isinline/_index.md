---
title: ShapeBase.IsInline
linktitle: IsInline
articleTitle: IsInline
second_title: Aspose.Words para .NET
description: Descubra la propiedad ShapeBase IsInline para comprobar fácilmente si su forma se alinea con el texto, mejorando su diseño y optimizando la eficiencia del diseño.
type: docs
weight: 310
url: /es/net/aspose.words.drawing/shapebase/isinline/
---
## ShapeBase.IsInline property

Una forma rápida de determinar si esta forma está posicionada en línea con el texto.

```csharp
public bool IsInline { get; }
```

## Observaciones

Tiene efecto sólo para formas de nivel superior.

## Ejemplos

Muestra cómo determinar si una forma está en línea o es flotante.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//A continuación se muestran dos tipos de envoltura que pueden tener las formas.
// 1 - En línea:
builder.Write("Hello world! ");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.FillColor = Color.LightBlue;
builder.Write(" Hello again.");

// Una forma en línea se ubica dentro de un párrafo entre otros elementos del párrafo, como por ejemplo líneas de texto.
// En Microsoft Word, podemos hacer clic y arrastrar la forma a cualquier párrafo como si fuera un carácter.
// Si la forma es grande, afectará el espaciado vertical del párrafo.
//No podemos mover esta forma a un lugar sin párrafo.
Assert.AreEqual(WrapType.Inline, shape.WrapType);
Assert.True(shape.IsInline);

// 2 - Flotante:
shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 200,
    RelativeVerticalPosition.TopMargin, 200, 100, 100, WrapType.None);
shape.FillColor = Color.Orange;

// Una forma flotante pertenece al párrafo en el que la insertamos,
// lo cual podemos determinar mediante un símbolo de ancla que aparece cuando hacemos clic en la forma.
// Si la forma no tiene un símbolo de ancla visible a su izquierda,
// necesitaremos habilitar los anclajes visibles a través de "Opciones" -> "Mostrar" -> "Anclajes de objeto".
// En Microsoft Word, podemos hacer clic izquierdo y arrastrar esta forma libremente a cualquier ubicación.
Assert.AreEqual(WrapType.None, shape.WrapType);
Assert.False(shape.IsInline);

doc.Save(ArtifactsDir + "Shape.IsInline.docx");
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
