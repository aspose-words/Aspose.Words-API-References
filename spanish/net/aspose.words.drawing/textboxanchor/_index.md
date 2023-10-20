---
title: TextBoxAnchor Enum
linktitle: TextBoxAnchor
articleTitle: TextBoxAnchor
second_title: Aspose.Words para .NET
description: Aspose.Words.Drawing.TextBoxAnchor enumeración. Especifica los valores utilizados para la alineación vertical del texto de forma en C#.
type: docs
weight: 1330
url: /es/net/aspose.words.drawing/textboxanchor/
---
## TextBoxAnchor enumeration

Especifica los valores utilizados para la alineación vertical del texto de forma.

```csharp
public enum TextBoxAnchor
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Top | `0` | El texto está alineado con la parte superior del cuadro de texto. |
| Middle | `1` | El texto está alineado con el centro del cuadro de texto. |
| Bottom | `2` | El texto está alineado con la parte inferior del cuadro de texto. |
| TopCentered | `3` | El texto está alineado con la parte superior centrada del cuadro de texto. |
| MiddleCentered | `4` | El texto está alineado con el centro del cuadro de texto. |
| BottomCentered | `5` | El texto está alineado con la parte inferior centrada del cuadro de texto. |
| TopBaseline | `6` | El texto está alineado con la línea base superior del cuadro de texto. |
| BottomBaseline | `7` | El texto está alineado con la línea base inferior del cuadro de texto. |
| TopCenteredBaseline | `8` | El texto está alineado con la línea base centrada superior del cuadro de texto. |
| BottomCenteredBaseline | `9` | El texto está alineado con la línea base inferior centrada del cuadro de texto. |

## Ejemplos

Muestra cómo alinear verticalmente el contenido de texto de un cuadro de texto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// Establece la propiedad "VerticalAnchor" en "TextBoxAnchor.Top" para
// alinea el texto en este cuadro de texto con el lado superior de la forma.
// Establece la propiedad "VerticalAnchor" en "TextBoxAnchor.Middle" para
// alinea el texto en este cuadro de texto con el centro de la forma.
// Establece la propiedad "VerticalAnchor" en "TextBoxAnchor.Bottom" para
// alinea el texto de este cuadro de texto con la parte inferior de la forma.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// La alineación vertical del texto dentro de los cuadros de texto está disponible desde Microsoft Word 2007 en adelante.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
