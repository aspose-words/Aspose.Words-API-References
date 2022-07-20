---
title: CompareOptions
second_title: Referencia de API de Aspose.Words para .NET
description: Permite elegir opciones avanzadas para la operación de comparación de documentos.
type: docs
weight: 260
url: /es/net/aspose.words.comparing/compareoptions/
---
## CompareOptions class

Permite elegir opciones avanzadas para la operación de comparación de documentos.

```csharp
public class CompareOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [CompareOptions](compareoptions)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Granularity](../../aspose.words.comparing/compareoptions/granularity) { get; set; } | Especifica si los cambios se rastrean por carácter o por palabra. El valor predeterminado esWordLevel . |
| [IgnoreCaseChanges](../../aspose.words.comparing/compareoptions/ignorecasechanges) { get; set; } | True indica que la comparación de documentos no distingue entre mayúsculas y minúsculas. Por defecto, la comparación distingue entre mayúsculas y minúsculas. |
| [IgnoreComments](../../aspose.words.comparing/compareoptions/ignorecomments) { get; set; } | Especifica si comparar las diferencias en los comentarios. Por defecto no se ignoran los comentarios. |
| [IgnoreDmlUniqueId](../../aspose.words.comparing/compareoptions/ignoredmluniqueid) { get; set; } | Especifica si se ignorará la diferencia en el ID único de DrawingML. El valor predeterminado es **falso** . |
| [IgnoreFields](../../aspose.words.comparing/compareoptions/ignorefields) { get; set; } | Especifica si comparar las diferencias en los campos. Por defecto los campos no se ignoran. |
| [IgnoreFootnotes](../../aspose.words.comparing/compareoptions/ignorefootnotes) { get; set; } | Especifica si se comparan las diferencias en las notas al pie y al final. Por defecto no se ignoran las notas al pie. |
| [IgnoreFormatting](../../aspose.words.comparing/compareoptions/ignoreformatting) { get; set; } | True indica que se ignora el formato. Por defecto, no se ignora el formato del documento. |
| [IgnoreHeadersAndFooters](../../aspose.words.comparing/compareoptions/ignoreheadersandfooters) { get; set; } | True indica que se ignora el contenido de los encabezados y pies de página. Por defecto, los encabezados y pies de página no se ignoran. |
| [IgnoreTables](../../aspose.words.comparing/compareoptions/ignoretables) { get; set; } | Especifica si comparar las diferencias en los datos contenidos en las tablas. Por defecto no se ignoran las tablas. |
| [IgnoreTextboxes](../../aspose.words.comparing/compareoptions/ignoretextboxes) { get; set; } | Especifica si se comparan las diferencias en los datos contenidos en los cuadros de texto. Por defecto, los cuadros de texto no se ignoran. |
| [Target](../../aspose.words.comparing/compareoptions/target) { get; set; } | Especifica qué documento se utilizará como destino durante la comparación. |

### Ejemplos

Muestra cómo filtrar tipos específicos de elementos del documento al realizar una comparación.

```csharp
// Cree el documento original y rellénelo con varios tipos de elementos.
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);

// Texto de párrafo referenciado con una nota al final:
builder.Writeln("Hello world! This is the first paragraph.");
builder.InsertFootnote(FootnoteType.Endnote, "Original endnote text.");

// Mesa:
builder.StartTable();
builder.InsertCell();
builder.Write("Original cell 1 text");
builder.InsertCell();
builder.Write("Original cell 2 text");
builder.EndTable();

// Caja de texto:
Shape textBox = builder.InsertShape(ShapeType.TextBox, 150, 20);
builder.MoveTo(textBox.FirstParagraph);
builder.Write("Original textbox contents");

// campo FECHA:
builder.MoveTo(docOriginal.FirstSection.Body.AppendParagraph(""));
builder.InsertField(" DATE ");

// Comentario:
Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", DateTime.Now);
newComment.SetText("Original comment.");
builder.CurrentParagraph.AppendChild(newComment);

// Encabezado:
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Original header contents.");

// Crea un clon de nuestro documento y realiza una edición rápida en cada uno de los elementos del documento clonado.
Document docEdited = (Document)docOriginal.Clone(true);
Paragraph firstParagraph = docEdited.FirstSection.Body.FirstParagraph;

firstParagraph.Runs[0].Text = "hello world! this is the first paragraph, after editing.";
firstParagraph.ParagraphFormat.Style = docEdited.Styles[StyleIdentifier.Heading1];
((Footnote)docEdited.GetChild(NodeType.Footnote, 0, true)).FirstParagraph.Runs[1].Text = "Edited endnote text.";
((Table)docEdited.GetChild(NodeType.Table, 0, true)).FirstRow.Cells[1].FirstParagraph.Runs[0].Text = "Edited Cell 2 contents";
((Shape)docEdited.GetChild(NodeType.Shape, 0, true)).FirstParagraph.Runs[0].Text = "Edited textbox contents";
((FieldDate)docEdited.Range.Fields[0]).UseLunarCalendar = true; 
((Comment)docEdited.GetChild(NodeType.Comment, 0, true)).FirstParagraph.Runs[0].Text = "Edited comment.";
docEdited.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].FirstParagraph.Runs[0].Text =
    "Edited header contents.";

// La comparación de documentos crea una revisión para cada edición en el documento editado.
// Un objeto CompareOptions tiene una serie de banderas que pueden suprimir las revisiones
// en cada tipo respectivo de elemento, ignorando efectivamente su cambio.
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.IgnoreFormatting = false;
compareOptions.IgnoreCaseChanges = false;
compareOptions.IgnoreComments = false;
compareOptions.IgnoreTables = false;
compareOptions.IgnoreFields = false;
compareOptions.IgnoreFootnotes = false;
compareOptions.IgnoreTextboxes = false;
compareOptions.IgnoreHeadersAndFooters = false;
compareOptions.Target = ComparisonTargetType.New;

docOriginal.Compare(docEdited, "John Doe", DateTime.Now, compareOptions);
docOriginal.Save(ArtifactsDir + "Document.CompareOptions.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Comparing](../../aspose.words.comparing)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
