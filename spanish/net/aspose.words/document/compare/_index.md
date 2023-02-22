---
title: Document.Compare
second_title: Referencia de API de Aspose.Words para .NET
description: Document método. Compara este documento con otro documento produciendo cambios como número de ediciones y revisiones de formatoRevision .
type: docs
weight: 540
url: /es/net/aspose.words/document/compare/
---
## Compare(Document, string, DateTime) {#compare}

Compara este documento con otro documento produciendo cambios como número de ediciones y revisiones de formato[`Revision`](../../revision/) .

```csharp
public void Compare(Document document, string author, DateTime dateTime)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| document | Document | Documento para comparar. |
| author | String | Iniciales del autor a utilizar para las revisiones. |
| dateTime | DateTime | La fecha y la hora que se usarán para las revisiones. |

### Observaciones

Los siguientes nodos de documentos no se comparan en este momento:

* [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/)
* artículo3

Los documentos no deben tener revisiones antes de la comparación.

### Ejemplos

Muestra cómo comparar documentos.

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// La comparación de documentos con revisiones generará una excepción.
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// Después de la comparación, el documento original obtendrá una nueva revisión
// por cada elemento que sea diferente en el documento editado.
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// Aceptar estas revisiones transformará el documento original en el documento editado.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)

---

## Compare(Document, string, DateTime, CompareOptions) {#compare_1}

Compara este documento con otro documento produciendo cambios como una serie de revisiones de edición y formato[`Revision`](../../revision/) . Permite especificar opciones de comparación mediante[`CompareOptions`](../../../aspose.words.comparing/compareoptions/) .

```csharp
public void Compare(Document document, string author, DateTime dateTime, CompareOptions options)
```

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

* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)


