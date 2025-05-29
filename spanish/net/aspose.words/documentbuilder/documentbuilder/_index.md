---
title: DocumentBuilder
linktitle: DocumentBuilder
articleTitle: DocumentBuilder
second_title: Aspose.Words para .NET
description: Crea documentos potentes sin esfuerzo con DocumentBuilder. ¡Crea una nueva instancia y optimiza tu gestión documental hoy mismo!
type: docs
weight: 10
url: /es/net/aspose.words/documentbuilder/documentbuilder/
---
## DocumentBuilder() {#constructor}

Inicializa una nueva instancia de esta clase.

```csharp
public DocumentBuilder()
```

## Observaciones

Crea un nuevo[`DocumentBuilder`](../)objeto y lo adjunta a un nuevo[`Document`](../../document/) objeto.

## Ejemplos

Muestra cómo insertar texto formateado utilizando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Especifique el formato de fuente y luego agregue texto.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

### Ver también

* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## DocumentBuilder(*[DocumentBuilderOptions](../../documentbuilderoptions/)*) {#constructor_3}

Inicializa una nueva instancia de esta clase.

```csharp
public DocumentBuilder(DocumentBuilderOptions options)
```

## Observaciones

Crea un nuevo[`DocumentBuilder`](../)objeto y lo adjunta a un nuevo[`Document`](../../document/) object. Se pueden especificar opciones adicionales de creación de documentos.

## Ejemplos

Muestra cómo ignorar el formato de tabla para el contenido posterior.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// Agrega contenido antes de la tabla.
// El tamaño de fuente predeterminado es 12.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// Cambia el tamaño de fuente dentro de la tabla.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// Si ContextTableFormatting es verdadero, entonces el formato de tabla no se aplica al contenido posterior.
// Si ContextTableFormatting es falso, entonces el formato de tabla se aplica al contenido después.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### Ver también

* class [DocumentBuilderOptions](../../documentbuilderoptions/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## DocumentBuilder(*[Document](../../document/)*) {#constructor_1}

Inicializa una nueva instancia de esta clase.

```csharp
public DocumentBuilder(Document doc)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| doc | Document | El[`Document`](../../document/) objeto al que adjuntar. |

## Observaciones

Crea un nuevo[`DocumentBuilder`](../) objeto, se adjunta al especificado[`Document`](../../document/) objeto. El cursor se posiciona al principio del documento.

## Ejemplos

Muestra cómo crear encabezados y pies de página en un documento utilizando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Especificamos que queremos encabezados y pies de página diferentes para la primera página, páginas pares e impares.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Cree los encabezados y luego agregue tres páginas al documento para mostrar cada tipo de encabezado.
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

* class [Document](../../document/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## DocumentBuilder(*[Document](../../document/), [DocumentBuilderOptions](../../documentbuilderoptions/)*) {#constructor_2}

Inicializa una nueva instancia de esta clase.

```csharp
public DocumentBuilder(Document doc, DocumentBuilderOptions options)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| doc | Document | El[`Document`](../../document/) objeto al que adjuntar. |
| options | DocumentBuilderOptions | Opciones adicionales para el proceso de construcción de documentos. |

## Observaciones

Crea un nuevo[`DocumentBuilder`](../) objeto, se adjunta al especificado[`Document`](../../document/) objeto. El cursor se posiciona al principio del documento.

## Ejemplos

Muestra cómo ignorar el formato de tabla para el contenido posterior.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// Agrega contenido antes de la tabla.
// El tamaño de fuente predeterminado es 12.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// Cambia el tamaño de fuente dentro de la tabla.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// Si ContextTableFormatting es verdadero, entonces el formato de tabla no se aplica al contenido posterior.
// Si ContextTableFormatting es falso, entonces el formato de tabla se aplica al contenido después.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### Ver también

* class [Document](../../document/)
* class [DocumentBuilderOptions](../../documentbuilderoptions/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
