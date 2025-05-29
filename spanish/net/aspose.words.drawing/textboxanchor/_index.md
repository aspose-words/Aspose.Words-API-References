---
title: TextBoxAnchor Enum
linktitle: TextBoxAnchor
articleTitle: TextBoxAnchor
second_title: Aspose.Words para .NET
description: Descubre la enumeración Aspose.Words.Drawing.TextBoxAnchor para una alineación vertical precisa del texto de las formas. ¡Mejora el formato de tus documentos sin esfuerzo!
type: docs
weight: 1740
url: /es/net/aspose.words.drawing/textboxanchor/
---
## TextBoxAnchor enumeration

Especifica los valores utilizados para la alineación vertical del texto de la forma.

```csharp
public enum TextBoxAnchor
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Top | `0` | El texto se alinea en la parte superior del cuadro de texto. |
| Middle | `1` | El texto se alinea en el centro del cuadro de texto. |
| Bottom | `2` | El texto se alinea en la parte inferior del cuadro de texto. |
| TopCentered | `3` | El texto se alinea en la parte superior centrada del cuadro de texto. |
| MiddleCentered | `4` | El texto se alinea en el centro del cuadro de texto. |
| BottomCentered | `5` | El texto se alinea en la parte inferior centrada del cuadro de texto. |
| TopBaseline | `6` | El texto se alinea con la línea base superior del cuadro de texto. |
| BottomBaseline | `7` | El texto se alinea con la línea base inferior del cuadro de texto. |
| TopCenteredBaseline | `8` | El texto se alinea con la línea base centrada superior del cuadro de texto. |
| BottomCenteredBaseline | `9` | El texto se alinea con la línea base centrada en la parte inferior del cuadro de texto. |

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

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
