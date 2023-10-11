---
title: Enum LayoutFlow
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Drawing.LayoutFlow enumeración. Determina el flujo del diseño del texto en un cuadro de texto.
type: docs
weight: 1100
url: /es/net/aspose.words.drawing/layoutflow/
---
## LayoutFlow enumeration

Determina el flujo del diseño del texto en un cuadro de texto.

```csharp
public enum LayoutFlow
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Horizontal | `0` | El texto se muestra horizontalmente. |
| TopToBottomIdeographic | `1` | El texto ideográfico se muestra verticalmente. |
| BottomToTop | `2` | El texto se muestra verticalmente. |
| TopToBottom | `3` | El texto se muestra verticalmente. |
| HorizontalIdeographic | `4` | El texto ideográfico se muestra horizontalmente. |
| Vertical | `5` | El texto se muestra verticalmente. |

### Ejemplos

Muestra cómo agregar texto a un cuadro de texto y cambiar su orientación.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textbox = new Shape(doc, ShapeType.TextBox)
{
    Width = 100, 
    Height = 100,
    TextBox = { LayoutFlow = LayoutFlow.BottomToTop }
};

textbox.AppendChild(new Paragraph(doc));
builder.InsertNode(textbox);

builder.MoveTo(textbox.FirstParagraph);
builder.Write("This text is flipped 90 degrees to the left.");

doc.Save(ArtifactsDir + "Drawing.TextBox.docx");
```

### Ver también

* property [LayoutFlow](../textbox/layoutflow/)
* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)


