---
title: DocumentBuilder.InsertTableOfContents
second_title: Referencia de API de Aspose.Words para .NET
description: DocumentBuilder método. Inserta un campo TOC tabla de contenido en el documento.
type: docs
weight: 440
url: /es/net/aspose.words/documentbuilder/inserttableofcontents/
---
## DocumentBuilder.InsertTableOfContents method

Inserta un campo TOC (tabla de contenido) en el documento.

```csharp
public Field InsertTableOfContents(string switches)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| switches | String | El campo TOC cambia. |

### Observaciones

Este método inserta un campo TOC (tabla de contenido) en el documento en la posición actual.

Una tabla de contenido en un documento de Word puede construirse de varias maneras y formatearse usando una variedad de opciones. La forma en que se crea la tabla y se muestra en Microsoft Word se controla mediante los interruptores de campo.

La forma más fácil de especificar los interruptores es insertar y configurar una tabla de contenido en un documento de Word utilizando el menú Insertar-&gt;Referencia-&gt;Índice y tablas, y luego activar la visualización de códigos de campo para ver los interruptores. Puede presionar Alt+F9 en Microsoft Word para activar o desactivar la visualización de códigos de campo.

Por ejemplo, después de crear una tabla de contenido, se inserta el siguiente campo en el documento: **{ TOC \o "1-3" \h \z \u }** . Puedes copiar **\o "1-3" \h\z\u** y utilícelo como el parámetro de interruptores.

Tenga en cuenta que **InsertTableOfContents** solo insertará un campo TOC, pero en realidad no construirá la tabla de contenido. La tabla de contenido se crea con Microsoft Word cuando se actualiza el campo.

Si inserta una tabla de contenido con este método y luego abre el archivo en Microsoft Word, no verá la tabla de contenido porque el campo TOC aún no se ha actualizado.

En Microsoft Word, los campos no se actualizan automáticamente cuando se abre un documento, pero puede actualizar los campos en un documento en cualquier momento presionando F9.

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

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)


