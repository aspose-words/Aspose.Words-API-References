---
title: DocumentBuilder.InsertTableOfContents
linktitle: InsertTableOfContents
articleTitle: InsertTableOfContents
second_title: Aspose.Words para .NET
description: DocumentBuilder InsertTableOfContents método. Inserta un campo TOC tabla de contenido en el documento en C#.
type: docs
weight: 460
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

## Observaciones

Este método inserta un campo TOC (tabla de contenido) en el documento en la posición actual.

Una tabla de contenido en un documento de Word se puede crear de varias maneras y formatear usando una variedad de opciones. La forma en que se construye la tabla y se muestra en Microsoft Word está controlada por los modificadores de campo.

La forma más sencilla de especificar los modificadores es insertar y configurar una tabla de contenido en un documento de Word usando el menú Insertar-&gt;Referencia-&gt;Índice y tablas, y luego activar la visualización de códigos de campo para ver los modificadores. Puede presionar Alt+F9 en Microsoft Word para activar o desactivar la visualización de códigos de campo.

Por ejemplo, después de crear una tabla de contenido, se inserta el siguiente campo en el documento:**{ TOC \o "1-3" \h \z \u }** . Puedes copiar**\o "1-3" \h \z \u** y utilícelo como parámetro de interruptores.

Tenga en cuenta que`InsertTableOfContents` solo insertará un campo TOC, pero en realidad no creará la tabla de contenido. La tabla de contenido la crea Microsoft Word cuando se actualiza el campo.

Si inserta una tabla de contenido usando este método y luego abre el archivo en Microsoft Word, no verá la tabla de contenido porque el campo TOC aún no se ha actualizado.

En Microsoft Word, los campos no se actualizan automáticamente cuando se abre un documento, pero puede actualizar los campos de un documento en cualquier momento presionando F9.

## Ejemplos

Muestra cómo insertar una tabla de contenido (TOC) en un documento utilizando estilos de encabezado como entradas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar una tabla de contenido para la primera página del documento.
// Configurar la tabla para recoger párrafos con títulos de niveles 1 a 3.
// Además, configura sus entradas para que sean hipervínculos que nos llevarán
// a la ubicación del encabezado cuando se hace clic izquierdo en Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Complete la tabla de contenido agregando párrafos con estilos de encabezado.
// Cada uno de estos encabezados con un nivel entre 1 y 3 creará una entrada en la tabla.
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
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
