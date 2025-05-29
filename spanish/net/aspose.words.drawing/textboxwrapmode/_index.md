---
title: TextBoxWrapMode Enum
linktitle: TextBoxWrapMode
articleTitle: TextBoxWrapMode
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Drawing.TextBoxWrapMode para controlar el ajuste de texto en formas, mejorando los diseños de los documentos y la flexibilidad del diseño.
type: docs
weight: 1750
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

Muestra cómo establecer un modo de ajuste para el contenido de un cuadro de texto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 300, 300);
TextBox textBox = textBoxShape.TextBox;

// Establezca la propiedad "TextBoxWrapMode" en "TextBoxWrapMode.None" para aumentar el ancho del cuadro de texto
// para acomodar el texto, si es lo suficientemente grande.
// Establezca la propiedad "TextBoxWrapMode" en "TextBoxWrapMode.Square" para
// envuelve todo el texto dentro del cuadro de texto, conservando sus dimensiones.
textBox.TextBoxWrapMode = textBoxWrapMode;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Font.Size = 32;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "Shape.TextBoxContentsWrapMode.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
