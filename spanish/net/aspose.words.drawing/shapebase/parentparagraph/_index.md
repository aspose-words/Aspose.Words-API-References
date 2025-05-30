---
title: ShapeBase.ParentParagraph
linktitle: ParentParagraph
articleTitle: ParentParagraph
second_title: Aspose.Words para .NET
description: Descubra la propiedad ParentParagraph de ShapeBase acceda de manera eficiente al párrafo padre inmediato para una administración de contenido optimizada y una organización mejorada.
type: docs
weight: 430
url: /es/net/aspose.words.drawing/shapebase/parentparagraph/
---
## ShapeBase.ParentParagraph property

Devuelve el párrafo padre inmediato.

```csharp
public Paragraph ParentParagraph { get; }
```

## Observaciones

Para las formas secundarias de una forma de grupo y las formas secundarias de un objeto de Office Math siempre devuelve`nulo`.

## Ejemplos

Muestra cómo insertar un cuadro de texto y establecer la fuente de su contenido.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.TextBox, 300, 50);
builder.MoveTo(shape.LastParagraph);
builder.Write("This text is inside the text box.");

// Establezca la propiedad "Oculto" del objeto "Fuente" de la forma en "verdadero" para ocultar el cuadro de texto de la vista
// y colapsar el espacio que normalmente ocuparía.
// Establezca la propiedad "Oculto" del objeto "Fuente" de la forma en "falso" para dejar el cuadro de texto visible.
shape.Font.Hidden = hideShape;

// Si la forma es visible, modificaremos su apariencia a través del objeto de fuente.
if (!hideShape)
{
    shape.Font.HighlightColor = Color.LightGray;
    shape.Font.Color = Color.Red;
    shape.Font.Underline = Underline.Dash;
}

// Mueva el generador fuera del cuadro de texto y devuélvalo al documento principal.
builder.MoveTo(shape.ParentParagraph);

builder.Writeln("\nThis text is outside the text box.");

doc.Save(ArtifactsDir + "Shape.Font.docx");
```

### Ver también

* class [Paragraph](../../../aspose.words/paragraph/)
* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
