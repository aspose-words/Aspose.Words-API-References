---
title: TextBoxWrapMode Enum
linktitle: TextBoxWrapMode
articleTitle: TextBoxWrapMode
second_title: Aspose.Words para .NET
description: Aspose.Words.Drawing.TextBoxWrapMode enumeración. Especifica cómo se ajusta el texto dentro de una forma en C#.
type: docs
weight: 1340
url: /es/net/aspose.words.drawing/textboxwrapmode/
---
## TextBoxWrapMode enumeration

Especifica cómo se ajusta el texto dentro de una forma.

```csharp
public enum TextBoxWrapMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Square | `0` | El texto se ajusta dentro de una forma. |
| None | `2` | El texto no se ajusta dentro de una forma. |

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

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
