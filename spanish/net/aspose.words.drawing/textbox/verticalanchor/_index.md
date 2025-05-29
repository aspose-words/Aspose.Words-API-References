---
title: TextBox.VerticalAnchor
linktitle: VerticalAnchor
articleTitle: VerticalAnchor
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad TextBox VerticalAnchor mejora la alineación del texto dentro de las formas para mejorar el diseño y la legibilidad en sus proyectos.
type: docs
weight: 120
url: /es/net/aspose.words.drawing/textbox/verticalanchor/
---
## TextBox.VerticalAnchor property

Especifica la alineación vertical del texto dentro de una forma.

```csharp
public TextBoxAnchor VerticalAnchor { get; set; }
```

## Observaciones

El valor predeterminado esTop.

## Ejemplos

Muestra cómo alinear verticalmente el contenido de texto de un cuadro de texto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// Establezca la propiedad "VerticalAnchor" en "TextBoxAnchor.Top" para
// alinea el texto en este cuadro de texto con el lado superior de la forma.
// Establezca la propiedad "VerticalAnchor" en "TextBoxAnchor.Middle" para
// alinea el texto en este cuadro de texto al centro de la forma.
// Establezca la propiedad "VerticalAnchor" en "TextBoxAnchor.Bottom" para
// alinea el texto en este cuadro de texto con la parte inferior de la forma.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// La alineación vertical del texto dentro de los cuadros de texto está disponible desde Microsoft Word 2007 en adelante.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

### Ver también

* enum [TextBoxAnchor](../../textboxanchor/)
* class [TextBox](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
