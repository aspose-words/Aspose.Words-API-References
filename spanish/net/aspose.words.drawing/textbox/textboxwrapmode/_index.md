---
title: TextBox.TextBoxWrapMode
linktitle: TextBoxWrapMode
articleTitle: TextBoxWrapMode
second_title: Aspose.Words para .NET
description: TextBox TextBoxWrapMode propiedad. Determina cómo se ajusta el texto dentro de una forma en C#.
type: docs
weight: 110
url: /es/net/aspose.words.drawing/textbox/textboxwrapmode/
---
## TextBox.TextBoxWrapMode property

Determina cómo se ajusta el texto dentro de una forma.

```csharp
public TextBoxWrapMode TextBoxWrapMode { get; set; }
```

## Observaciones

El valor predeterminado esSquare.

## Ejemplos

Muestra cómo configurar un modo de ajuste para el contenido de un cuadro de texto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 300, 300);
TextBox textBox = textBoxShape.TextBox;

// Establece la propiedad "TextBoxWrapMode" en "TextBoxWrapMode.None" para aumentar el ancho del cuadro de texto
// para dar cabida al texto, en caso de que sea lo suficientemente grande.
// Establece la propiedad "TextBoxWrapMode" en "TextBoxWrapMode.Square" para
// ajusta todo el texto dentro del cuadro de texto, conservando sus dimensiones.
textBox.TextBoxWrapMode = textBoxWrapMode;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Font.Size = 32;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "Shape.TextBoxContentsWrapMode.docx");
```

### Ver también

* enum [TextBoxWrapMode](../../textboxwrapmode/)
* class [TextBox](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
