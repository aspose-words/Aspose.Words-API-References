---
title: BreakType
second_title: Referencia de API de Aspose.Words para .NET
description: Especifica el tipo de ruptura dentro de un documento.
type: docs
weight: 100
url: /es/net/aspose.words/breaktype/
---
## BreakType enumeration

Especifica el tipo de ruptura dentro de un documento.

```csharp
public enum BreakType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| ParagraphBreak | `0` | Salto entre párrafos. |
| PageBreak | `1` | Salto de página explícito. |
| ColumnBreak | `2` | Salto de columna explícito. |
| SectionBreakContinuous | `3` | Especifica el inicio de una nueva sección en la misma página que la sección anterior. |
| SectionBreakNewColumn | `4` | Especifica el inicio de una nueva sección en la nueva columna. |
| SectionBreakNewPage | `5` | Especifica el inicio de una nueva sección en una nueva página. |
| SectionBreakEvenPage | `6` | Especifica el inicio de una nueva sección en una nueva página par. |
| SectionBreakOddPage | `7` | Especifica el inicio de una nueva sección en una página impar. |
| LineBreak | `8` | Salto de línea explícito. |

### Ejemplos

Muestra cómo crear encabezados y pies de página en un documento usando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Especificar que queremos encabezados y pies de página diferentes para las primeras páginas, pares e impares.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Cree los encabezados, luego agregue tres páginas al documento para mostrar cada tipo de encabezado.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

Muestra cómo aplicar y revertir la configuración de configuración de página a las secciones de un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Modifique las propiedades de configuración de la página para la sección actual del constructor y agregue texto.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// Si comenzamos una nueva sección usando un generador de documentos,
// heredará las propiedades de configuración de la página actual del constructor.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// Podemos revertir sus propiedades de configuración de página a sus valores predeterminados usando el método "ClearFormatting".
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

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

* espacio de nombres [Aspose.Words](../../aspose.words)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
