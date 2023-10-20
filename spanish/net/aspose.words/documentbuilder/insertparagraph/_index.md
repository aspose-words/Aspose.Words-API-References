---
title: DocumentBuilder.InsertParagraph
linktitle: InsertParagraph
articleTitle: InsertParagraph
second_title: Aspose.Words para .NET
description: DocumentBuilder InsertParagraph método. Inserta un salto de párrafo en el documento en C#.
type: docs
weight: 420
url: /es/net/aspose.words/documentbuilder/insertparagraph/
---
## DocumentBuilder.InsertParagraph method

Inserta un salto de párrafo en el documento.

```csharp
public Paragraph InsertParagraph()
```

### Valor_devuelto

El nodo de párrafo que se acaba de insertar. Es el mismo nodo que[`CurrentParagraph`](../currentparagraph/).

## Observaciones

Formato de párrafo actual especificado por el[`ParagraphFormat`](../paragraphformat/) Se utiliza la propiedad.

Divide el párrafo actual en dos. Después de insertar el párrafo, el cursor se coloca al principio del nuevo párrafo.

Se produce una excepción si no es posible insertar un salto de párrafo en la posición actual del cursor.

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

* class [Paragraph](../../paragraph/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
