---
title: ControlChar
second_title: Referencia de API de Aspose.Words para .NET
description: Caracteres de control que se encuentran a menudo en los documentos.
type: docs
weight: 340
url: /es/net/aspose.words/controlchar/
---
## ControlChar class

Caracteres de control que se encuentran a menudo en los documentos.

```csharp
public static class ControlChar
```

## Campos

| Nombre | Descripción |
| --- | --- |
| static readonly [Cell](../../aspose.words/controlchar/cell/) | Final de una celda de tabla o final de un carácter de fila de tabla: "\x0007" o "\a". |
| const [CellChar](../../aspose.words/controlchar/cellchar/) | Final de una celda de tabla o final de un carácter de fila de tabla: (char)7 o "\a". |
| static readonly [ColumnBreak](../../aspose.words/controlchar/columnbreak/) | Carácter de fin de columna: "\x000e". |
| const [ColumnBreakChar](../../aspose.words/controlchar/columnbreakchar/) | Carácter de fin de columna: (char)14. |
| static readonly [Cr](../../aspose.words/controlchar/cr/) | Carácter de retorno de carro: "\x000d" o "\r". Igual que[`ParagraphBreak`](./paragraphbreak/) . |
| static readonly [CrLf](../../aspose.words/controlchar/crlf/) | Retorno de carro seguido de carácter de avance de línea: "\x000d\x000a" o "\r\n". No se usa como tal en documentos de Microsoft Word, pero se usa comúnmente en archivos de texto para saltos de párrafo. |
| const [DefaultTextInputChar](../../aspose.words/controlchar/defaulttextinputchar/) | Este es el carácter "o" utilizado como valor predeterminado en los campos de formulario de entrada de texto. |
| const [FieldEndChar](../../aspose.words/controlchar/fieldendchar/) | Carácter de fin de campo de MS Word: (char)21. |
| const [FieldSeparatorChar](../../aspose.words/controlchar/fieldseparatorchar/) | El carácter separador de campo separa el código de campo del valor del campo. Opcional en algunos campos. Valor: (char)20. |
| const [FieldStartChar](../../aspose.words/controlchar/fieldstartchar/) | Inicio del carácter de campo de MS Word: (char)19. |
| static readonly [Lf](../../aspose.words/controlchar/lf/) | Carácter de avance de línea: "\x000a" o "\n". Igual que[`LineFeed`](./linefeed/) . |
| static readonly [LineBreak](../../aspose.words/controlchar/linebreak/) | Carácter de salto de línea: "\x000b" o "\v". |
| const [LineBreakChar](../../aspose.words/controlchar/linebreakchar/) | Carácter de salto de línea: (char)11 o "\v". |
| static readonly [LineFeed](../../aspose.words/controlchar/linefeed/) | Carácter de avance de línea: "\x000a" o "\n". Igual que[`Lf`](./lf/) . |
| const [LineFeedChar](../../aspose.words/controlchar/linefeedchar/) | Carácter de avance de línea: (char)10 o "\n". |
| const [NonBreakingHyphenChar](../../aspose.words/controlchar/nonbreakinghyphenchar/) | Guión continuo en Microsoft Word es (char)30. |
| static readonly [NonBreakingSpace](../../aspose.words/controlchar/nonbreakingspace/) | Carácter de espacio de no separación: "\x00a0". |
| const [NonBreakingSpaceChar](../../aspose.words/controlchar/nonbreakingspacechar/) | Carácter de espacio de no separación: (char)160. |
| const [OptionalHyphenChar](../../aspose.words/controlchar/optionalhyphenchar/) | Guión opcional en Microsoft Word es (char)31. |
| static readonly [PageBreak](../../aspose.words/controlchar/pagebreak/) | Carácter de salto de página: "\x000c" o "\f". Tenga en cuenta que tiene el mismo valor que[`SectionBreak`](./sectionbreak/) . |
| const [PageBreakChar](../../aspose.words/controlchar/pagebreakchar/) | Carácter de salto de página: (char)12 o "\f". |
| static readonly [ParagraphBreak](../../aspose.words/controlchar/paragraphbreak/) | Carácter de fin de párrafo: "\x000d" o "\r". Igual que[`Cr`](./cr/) |
| const [ParagraphBreakChar](../../aspose.words/controlchar/paragraphbreakchar/) | Carácter de fin de párrafo: (char)13 o "\r". |
| static readonly [SectionBreak](../../aspose.words/controlchar/sectionbreak/) | Carácter de fin de sección: "\x000c" o "\f". Tenga en cuenta que tiene el mismo valor que[`PageBreak`](./pagebreak/) . |
| const [SectionBreakChar](../../aspose.words/controlchar/sectionbreakchar/) | Carácter de fin de sección: (char)12 o "\f". |
| const [SpaceChar](../../aspose.words/controlchar/spacechar/) | Carácter de espacio: (char)32. |
| static readonly [Tab](../../aspose.words/controlchar/tab/) | Carácter de tabulación: "\x0009" o "\t". |
| const [TabChar](../../aspose.words/controlchar/tabchar/) | Carácter de tabulación: (char)9 o "\t". |

### Observaciones

Proporciona versiones de caracteres y cadenas de las mismas constantes. Por ejemplo: string ControlChar.LineBreak y char ControlChar.LineBreakChar tienen el mismo valor.

### Ejemplos

Muestra cómo usar los caracteres de control.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar párrafos con texto con DocumentBuilder.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Convertir el documento a formato de texto revela que los caracteres de control
// representar algunos de los elementos estructurales del documento, como los saltos de página.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// Al convertir un documento a formato de cadena,
// podemos omitir algunos de los caracteres de control con el método Trim.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
