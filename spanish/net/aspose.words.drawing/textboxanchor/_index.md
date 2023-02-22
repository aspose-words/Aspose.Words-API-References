---
title: Enum TextBoxAnchor
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Drawing.TextBoxAnchor enumeración. Especifica los valores utilizados para la alineación vertical del texto de forma.
type: docs
weight: 1180
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
| Top | `0` | El texto se alinea con la parte superior del cuadro de texto. |
| Middle | `1` | El texto se alinea a la mitad del cuadro de texto. |
| Bottom | `2` | El texto se alinea con la parte inferior del cuadro de texto. |
| TopCentered | `3` | El texto se alinea con la parte superior centrada del cuadro de texto. |
| MiddleCentered | `4` | El texto se alinea en el centro del cuadro de texto. |
| BottomCentered | `5` | El texto se alinea con la parte inferior centrada del cuadro de texto. |
| TopBaseline | `6` | El texto se alinea con la línea base superior del cuadro de texto. |
| BottomBaseline | `7` | El texto se alinea con la línea base inferior del cuadro de texto. |
| TopCenteredBaseline | `8` | El texto se alinea con la línea base superior centrada del cuadro de texto. |
| BottomCenteredBaseline | `9` | El texto se alinea con la línea de base centrada en la parte inferior del cuadro de texto. |

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

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)


