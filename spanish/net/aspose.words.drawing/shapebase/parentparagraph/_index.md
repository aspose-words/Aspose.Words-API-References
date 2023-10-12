---
title: ShapeBase.ParentParagraph
second_title: Referencia de API de Aspose.Words para .NET
description: ShapeBase propiedad. Devuelve el párrafo padre inmediato.
type: docs
weight: 410
url: /es/net/aspose.words.drawing/shapebase/parentparagraph/
---
## ShapeBase.ParentParagraph property

Devuelve el párrafo padre inmediato.

```csharp
public Paragraph ParentParagraph { get; }
```

### Observaciones

Para formas secundarias de una forma de grupo y formas secundarias de un objeto de Office Math siempre devuelve`nulo`.

### Ejemplos

Muestra cómo insertar un cuadro de texto y configurar la fuente de su contenido.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.TextBox, 300, 50);
builder.MoveTo(shape.LastParagraph);
builder.Write("This text is inside the text box.");

// Establece la propiedad "Oculta" del objeto "Fuente" de la forma en "verdadero" para ocultar el cuadro de texto a la vista
// y colapsar el espacio que normalmente ocuparía.
// Establece la propiedad "Oculta" del objeto "Fuente" de la forma en "falso" para dejar el cuadro de texto visible.
shape.Font.Hidden = hideShape;

// Si la forma es visible, modificaremos su apariencia mediante el objeto de fuente.
if (!hideShape)
{
    shape.Font.HighlightColor = Color.LightGray;
    shape.Font.Color = Color.Red;
    shape.Font.Underline = Underline.Dash;
}

// Saca el constructor del cuadro de texto y vuelve al documento principal.
builder.MoveTo(shape.ParentParagraph);

builder.Writeln("\nThis text is outside the text box.");

doc.Save(ArtifactsDir + "Shape.Font.docx");
```

### Ver también

* class [Paragraph](../../../aspose.words/paragraph/)
* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../shapebase/)
* asamblea [Aspose.Words](../../../)


