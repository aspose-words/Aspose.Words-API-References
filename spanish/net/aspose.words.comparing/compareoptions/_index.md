---
title: CompareOptions Class
linktitle: CompareOptions
articleTitle: CompareOptions
second_title: Aspose.Words para .NET
description: Aspose.Words.Comparing.CompareOptions clase. Permite elegir opciones avanzadas para la operación de comparación de documentos en C#.
type: docs
weight: 270
url: /es/net/aspose.words.comparing/compareoptions/
---
## CompareOptions class

Permite elegir opciones avanzadas para la operación de comparación de documentos.

Para obtener más información, visite el[Comparar documentos](https://docs.aspose.com/words/net/compare-documents/) artículo de documentación.

```csharp
public class CompareOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [CompareOptions](compareoptions/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CompareMoves](../../aspose.words.comparing/compareoptions/comparemoves/) { get; set; } | Especifica si se comparan las diferencias enMoveRevision entre los dos documentos. Por defecto, no se producen revisiones de movimiento. |
| [Granularity](../../aspose.words.comparing/compareoptions/granularity/) { get; set; } | Especifica si los cambios se rastrean por carácter o por palabra. El valor predeterminado esWordLevel . |
| [IgnoreCaseChanges](../../aspose.words.comparing/compareoptions/ignorecasechanges/) { get; set; } | Verdadero indica que la comparación de documentos no distingue entre mayúsculas y minúsculas. De forma predeterminada, la comparación distingue entre mayúsculas y minúsculas. |
| [IgnoreComments](../../aspose.words.comparing/compareoptions/ignorecomments/) { get; set; } | Especifica si se comparan las diferencias en los comentarios. De forma predeterminada, los comentarios no se ignoran. |
| [IgnoreDmlUniqueId](../../aspose.words.comparing/compareoptions/ignoredmluniqueid/) { get; set; } | Especifica si se ignora la diferencia en el ID único de DrawingML. El valor predeterminado es`FALSO` . |
| [IgnoreFields](../../aspose.words.comparing/compareoptions/ignorefields/) { get; set; } | Especifica si se comparan las diferencias en los campos. De forma predeterminada, los campos no se ignoran. |
| [IgnoreFootnotes](../../aspose.words.comparing/compareoptions/ignorefootnotes/) { get; set; } | Especifica si se comparan las diferencias en las notas al pie y al final. De forma predeterminada, las notas al pie no se ignoran. |
| [IgnoreFormatting](../../aspose.words.comparing/compareoptions/ignoreformatting/) { get; set; } | Verdadero indica que se ignora el formato. De forma predeterminada, el formato del documento no se ignora. |
| [IgnoreHeadersAndFooters](../../aspose.words.comparing/compareoptions/ignoreheadersandfooters/) { get; set; } | Verdadero indica que el contenido de los encabezados y pies de página se ignora. De forma predeterminada, los encabezados y pies de página no se ignoran. |
| [IgnoreTables](../../aspose.words.comparing/compareoptions/ignoretables/) { get; set; } | Especifica si se comparan las diferencias en los datos contenidos en las tablas. De forma predeterminada, las tablas no se ignoran. |
| [IgnoreTextboxes](../../aspose.words.comparing/compareoptions/ignoretextboxes/) { get; set; } | Especifica si se comparan las diferencias en los datos contenidos en los cuadros de texto. De forma predeterminada, los cuadros de texto no se ignoran. |
| [Target](../../aspose.words.comparing/compareoptions/target/) { get; set; } | Especifica qué documento se utilizará como objetivo durante la comparación. |

## Ejemplos

Muestra cómo filtrar tipos específicos de elementos del documento al realizar una comparación.

```csharp
// Crea el documento original y complétalo con varios tipos de elementos.
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);

// Texto del párrafo al que se hace referencia con una nota al final:
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

// encabezado:
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
// Un objeto CompareOptions tiene una serie de indicadores que pueden suprimir revisiones
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

* espacio de nombres [Aspose.Words.Comparing](../../aspose.words.comparing/)
* asamblea [Aspose.Words](../../)
