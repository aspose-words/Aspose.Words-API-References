---
title: FindReplaceOptions.ApplyParagraphFormat
linktitle: ApplyParagraphFormat
articleTitle: ApplyParagraphFormat
second_title: Aspose.Words para .NET
description: Descubre la propiedad ApplyParagraphFormat en FindReplaceOptions para un formato de párrafo perfecto en tus documentos. ¡Mejora tu contenido sin esfuerzo!
type: docs
weight: 30
url: /es/net/aspose.words.replacing/findreplaceoptions/applyparagraphformat/
---
## FindReplaceOptions.ApplyParagraphFormat property

Formato de párrafo aplicado al nuevo contenido.

```csharp
public ParagraphFormat ApplyParagraphFormat { get; }
```

## Ejemplos

Muestra cómo agregar formato a los párrafos en los que una operación de búsqueda y reemplazo encontró coincidencias.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Every paragraph that ends with a full stop like this one will be right aligned.");
builder.Writeln("This one will not!");
builder.Write("This one also will.");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(ParagraphAlignment.Left, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[2].ParagraphFormat.Alignment);

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de búsqueda y reemplazo.
FindReplaceOptions options = new FindReplaceOptions();

// Establezca la propiedad "Alineación" en "ParagraphAlignment.Right" para alinear a la derecha cada párrafo
// que contiene una coincidencia que la operación de buscar y reemplazar encuentra.
options.ApplyParagraphFormat.Alignment = ParagraphAlignment.Right;

// Reemplace cada punto que esté justo antes de un salto de párrafo con un signo de exclamación.
int count = doc.Range.Replace(".&p", "!&p", options);

Assert.AreEqual(2, count);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[2].ParagraphFormat.Alignment);
Assert.AreEqual("Every paragraph that ends with a full stop like this one will be right aligned!\r" +
                "This one will not!\r" +
                "This one also will!", doc.GetText().Trim());
```

### Ver también

* class [ParagraphFormat](../../../aspose.words/paragraphformat/)
* class [FindReplaceOptions](../)
* espacio de nombres [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* asamblea [Aspose.Words](../../../)
