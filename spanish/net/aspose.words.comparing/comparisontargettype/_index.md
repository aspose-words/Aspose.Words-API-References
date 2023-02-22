---
title: Enum ComparisonTargetType
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Comparing.ComparisonTargetType enumeración. Permite especificar el documento base que se utilizará durante la comparación. El valor predeterminado esCurrent .
type: docs
weight: 270
url: /es/net/aspose.words.comparing/comparisontargettype/
---
## ComparisonTargetType enumeration

Permite especificar el documento base que se utilizará durante la comparación. El valor predeterminado esCurrent .

```csharp
public enum ComparisonTargetType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Current | `0` | Este documento se utiliza como base durante la comparación. |
| New | `1` | Se utiliza otro documento como base durante la comparación. |

### Observaciones

Se relaciona con la opción "Mostrar cambios en" de Microsoft Word en el cuadro de diálogo "Comparar documentos".

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

* espacio de nombres [Aspose.Words.Comparing](../../aspose.words.comparing/)
* asamblea [Aspose.Words](../../)


