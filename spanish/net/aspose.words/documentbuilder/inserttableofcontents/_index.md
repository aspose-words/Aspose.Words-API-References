---
title: DocumentBuilder.InsertTableOfContents
linktitle: InsertTableOfContents
articleTitle: InsertTableOfContents
second_title: Aspose.Words para .NET
description: Mejore sin esfuerzo sus documentos con el método InsertTableOfContents de DocumentBuilder, agregando una tabla de contenido dinámica para una navegación sencilla y una mejor organización.
type: docs
weight: 500
url: /es/net/aspose.words/documentbuilder/inserttableofcontents/
---
## DocumentBuilder.InsertTableOfContents method

Inserta un campo TOC (tabla de contenidos) en el documento.

```csharp
public Field InsertTableOfContents(string switches)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| switches | String | El campo TOC cambia. |

## Observaciones

Este método inserta un campo TOC (tabla de contenidos) en el documento en la posición actual.

Una tabla de contenido en un documento de Word se puede crear de diversas maneras y formatear con diversas opciones. La forma en que Microsoft Word crea y muestra la tabla se controla mediante los parámetros de campo.

La forma más sencilla de especificar los parámetros es insertar y configurar una tabla de contenido en un documento de Word mediante el menú Insertar-&gt;Referencia-&gt;Índice y tablas. A continuación, active la visualización de códigos de campo para verlos. Puede presionar Alt+F9 en Microsoft Word para activar o desactivar la visualización de códigos de campo.

Por ejemplo, después de crear una tabla de contenidos, se inserta el siguiente campo en el documento:**{ TOC \o "1-3" \h \z \u }** . Puedes copiar**\o "1-3" \h \z \u** y usarlo como parámetro de interruptores.

Tenga en cuenta que`InsertTableOfContents` Solo insertará un campo de índice, pero no generará la tabla de contenido. Microsoft Word la genera al actualizar el campo.

Si inserta una tabla de contenido utilizando este método y luego abre el archivo en Microsoft Word, no verá la tabla de contenido porque el campo TOC aún no se ha actualizado.

En Microsoft Word, los campos no se actualizan automáticamente cuando se abre un documento, pero puede actualizar los campos de un documento en cualquier momento presionando F9.

## Ejemplos

Muestra cómo insertar una tabla de contenido (TOC) en un documento utilizando estilos de encabezado como entradas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar una tabla de contenidos para la primera página del documento.
// Configurar la tabla para seleccionar párrafos con encabezados de niveles 1 a 3.
// Además, configure sus entradas para que sean hipervínculos que nos llevarán
// a la ubicación del encabezado cuando se hace clic izquierdo en Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Rellene la tabla de contenidos agregando párrafos con estilos de encabezado.
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

// Una tabla de contenidos es un campo de un tipo que necesita actualizarse para mostrar un resultado actualizado.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Ver también

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
