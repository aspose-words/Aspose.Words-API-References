---
title: ParagraphFormat.StyleIdentifier
second_title: Referencia de API de Aspose.Words para .NET
description: ParagraphFormat propiedad. Obtiene o establece el identificador de estilo independiente de la configuración regional del estilo de párrafo aplicado a este formato.
type: docs
weight: 340
url: /es/net/aspose.words/paragraphformat/styleidentifier/
---
## ParagraphFormat.StyleIdentifier property

Obtiene o establece el identificador de estilo independiente de la configuración regional del estilo de párrafo aplicado a este formato.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

### Ejemplos

Muestra cómo insertar una tabla de contenido (TOC) en un documento utilizando estilos de título como entradas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta una tabla de contenido para la primera página del documento.
// Configure la tabla para recoger párrafos con encabezados de niveles 1 a 3.
// Además, configure sus entradas para que sean hipervínculos que nos llevarán
// a la ubicación del encabezado cuando se hace clic con el botón izquierdo en Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Complete la tabla de contenido agregando párrafos con estilos de encabezado.
// Cada encabezado con un nivel entre 1 y 3 creará una entrada en la tabla.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// Una tabla de contenido es un campo de un tipo que debe actualizarse para mostrar un resultado actualizado.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Ver también

* enum [StyleIdentifier](../../styleidentifier/)
* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../paragraphformat/)
* asamblea [Aspose.Words](../../../)


