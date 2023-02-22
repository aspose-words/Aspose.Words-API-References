---
title: Paragraph.BreakIsStyleSeparator
second_title: Referencia de API de Aspose.Words para .NET
description: Paragraph propiedad. Verdadero si este salto de párrafo es un separador de estilo. Un separador de estilo permite que un párrafo conste de partes que tienen diferentes estilos de párrafo.
type: docs
weight: 20
url: /es/net/aspose.words/paragraph/breakisstyleseparator/
---
## Paragraph.BreakIsStyleSeparator property

Verdadero si este salto de párrafo es un separador de estilo. Un separador de estilo permite que un párrafo conste de partes que tienen diferentes estilos de párrafo.

```csharp
public bool BreakIsStyleSeparator { get; }
```

### Ejemplos

Muestra cómo escribir texto en la misma línea que un encabezado de TOC y hacer que no aparezca en la TOC.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertTableOfContents("\\o \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Inserta un párrafo con un estilo que el TOC tomará como una entrada.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

// Ambas cadenas están en el mismo párrafo y, por lo tanto, aparecerán en la misma entrada de TOC.
builder.Write("Heading 1. ");
builder.Write("Will appear in the TOC. ");

// Si insertamos un separador de estilo, podemos escribir más texto en el mismo párrafo
// y use un estilo diferente sin aparecer en el TOC.
// Si usamos un estilo de tipo de encabezado después del separador, podemos dibujar múltiples entradas de TOC desde una línea de texto del documento.
builder.InsertStyleSeparator();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Quote;
builder.Write("Won't appear in the TOC. ");

Assert.True(doc.FirstSection.Body.FirstParagraph.BreakIsStyleSeparator);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Paragraph.BreakIsStyleSeparator.docx");
```

### Ver también

* class [Paragraph](../)
* espacio de nombres [Aspose.Words](../../paragraph/)
* asamblea [Aspose.Words](../../../)


