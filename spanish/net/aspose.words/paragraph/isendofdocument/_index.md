---
title: Paragraph.IsEndOfDocument
linktitle: IsEndOfDocument
articleTitle: IsEndOfDocument
second_title: Aspose.Words para .NET
description: Paragraph IsEndOfDocument propiedad. Verdadero si este párrafo es el último párrafo de la última sección del documento en C#.
type: docs
weight: 60
url: /es/net/aspose.words/paragraph/isendofdocument/
---
## Paragraph.IsEndOfDocument property

Verdadero si este párrafo es el último párrafo de la última sección del documento.

```csharp
public bool IsEndOfDocument { get; }
```

## Ejemplos

Muestra cómo insertar un párrafo en el documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Arial";
font.Underline = Underline.Dash;

ParagraphFormat paragraphFormat = builder.ParagraphFormat;
paragraphFormat.FirstLineIndent = 8;
paragraphFormat.Alignment = ParagraphAlignment.Justify;
paragraphFormat.AddSpaceBetweenFarEastAndAlpha = true;
paragraphFormat.AddSpaceBetweenFarEastAndDigit = true;
paragraphFormat.KeepTogether = true;

// El método "Writeln" finaliza el párrafo después de agregar texto
// y luego comienza una nueva línea, agregando un nuevo párrafo.
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### Ver también

* class [Paragraph](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
