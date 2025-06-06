---
title: Document.Compare
linktitle: Compare
articleTitle: Compare
second_title: Aspose.Words para .NET
description: Compare documentos fácilmente con nuestra herramienta Comparar documentos. Identifique rápidamente ediciones y cambios de formato para optimizar las revisiones y mejorar la colaboración.
type: docs
weight: 600
url: /es/net/aspose.words/document/compare/
---
## Compare(*[Document](../), string, DateTime*) {#compare}

Compara este documento con otro documento produciendo cambios como número de revisiones de edición y formato[`Revision`](../../revision/) .

```csharp
public void Compare(Document document, string author, DateTime dateTime)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| document | Document | Documento para comparar. |
| author | String | Iniciales del autor a utilizar para las revisiones. |
| dateTime | DateTime | La fecha y hora que se utilizarán para las revisiones. |

## Observaciones

Los documentos no deben tener revisiones antes de la comparación.

## Ejemplos

Muestra cómo comparar documentos.

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// Comparar documentos con revisiones generará una excepción.
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

//Después de la comparación, el documento original obtendrá una nueva revisión
// para cada elemento que sea diferente en el documento editado.
foreach (Revision r in docOriginal.Revisions)
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

//Aceptar estas revisiones transformará el documento original en el documento editado.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## Compare(*[Document](../), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_1}

Compara este documento con otro documento produciendo cambios como una serie de revisiones de edición y formato.[`Revision`](../../revision/) . Permite especificar opciones de comparación utilizando[`CompareOptions`](../../../aspose.words.comparing/compareoptions/) .

```csharp
public void Compare(Document document, string author, DateTime dateTime, CompareOptions options)
```

## Ejemplos

Muestra cómo filtrar tipos específicos de elementos de documento al realizar una comparación.

```csharp
// Crea el documento original y rellénalo con varios tipos de elementos.
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);

// Texto de párrafo referenciado con una nota final:
builder.Writeln("Hello world! This is the first paragraph.");
builder.InsertFootnote(FootnoteType.Endnote, "Original endnote text.");

// Mesa:
builder.StartTable();
builder.InsertCell();
builder.Write("Original cell 1 text");
builder.InsertCell();
builder.Write("Original cell 2 text");
builder.EndTable();

//Cuadro de texto:
Shape textBox = builder.InsertShape(ShapeType.TextBox, 150, 20);
builder.MoveTo(textBox.FirstParagraph);
builder.Write("Original textbox contents");

// Campo FECHA:
builder.MoveTo(docOriginal.FirstSection.Body.AppendParagraph(""));
builder.InsertField(" DATE ");

// Comentario:
Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", DateTime.Now);
newComment.SetText("Original comment.");
builder.CurrentParagraph.AppendChild(newComment);

// Encabezado:
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Original header contents.");

// Cree un clon de nuestro documento y realice una edición rápida en cada uno de los elementos del documento clonado.
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
CompareOptions compareOptions = new CompareOptions
{
    CompareMoves = false,
    IgnoreFormatting = false,
    IgnoreCaseChanges = false,
    IgnoreComments = false,
    IgnoreTables = false,
    IgnoreFields = false,
    IgnoreFootnotes = false,
    IgnoreTextboxes = false,
    IgnoreHeadersAndFooters = false,
    Target = ComparisonTargetType.New
};

docOriginal.Compare(docEdited, "John Doe", DateTime.Now, compareOptions);
docOriginal.Save(ArtifactsDir + "Revision.CompareOptions.docx");
```

### Ver también

* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
