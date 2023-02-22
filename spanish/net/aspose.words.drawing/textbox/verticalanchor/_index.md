---
title: TextBox.VerticalAnchor
second_title: Referencia de API de Aspose.Words para .NET
description: TextBox propiedad. Especifica la alineación vertical del texto dentro de una forma.
type: docs
weight: 110
url: /es/net/aspose.words.drawing/textbox/verticalanchor/
---
## TextBox.VerticalAnchor property

Especifica la alineación vertical del texto dentro de una forma.

```csharp
public TextBoxAnchor VerticalAnchor { get; set; }
```

### Observaciones

El valor predeterminado esTop.

### Ejemplos

Muestra cómo alinear verticalmente el contenido de texto de un cuadro de texto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// Establecer la propiedad "VerticalAnchor" en "TextBoxAnchor.Top" para
// alinear el texto en este cuadro de texto con el lado superior de la forma.
// Establecer la propiedad "VerticalAnchor" en "TextBoxAnchor.Middle" para
// alinear el texto en este cuadro de texto al centro de la forma.
// Establecer la propiedad "VerticalAnchor" en "TextBoxAnchor.Bottom" para
// alinea el texto de este cuadro de texto con la parte inferior de la forma.
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
* espacio de nombres [Aspose.Words.Drawing](../../textbox/)
* asamblea [Aspose.Words](../../../)


