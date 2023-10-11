---
title: Document.Compare
second_title: Aspose.Words per .NET API Reference
description: Document metodo. Confronta questo documento con un altro documento producendo modifiche come numero di modifiche e revisioni del formatoRevision .
type: docs
weight: 580
url: /it/net/aspose.words/document/compare/
---
## Compare(Document, string, DateTime) {#compare}

Confronta questo documento con un altro documento producendo modifiche come numero di modifiche e revisioni del formato[`Revision`](../../revision/) .

```csharp
public void Compare(Document document, string author, DateTime dateTime)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| document | Document | Documento da confrontare. |
| author | String | Iniziali dell'autore da utilizzare per le revisioni. |
| dateTime | DateTime | La data e l'ora da utilizzare per le revisioni. |

### Osservazioni

I documenti non devono avere revisioni prima del confronto.

### Esempi

Mostra come confrontare i documenti.

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// Il confronto dei documenti con le revisioni genererà un'eccezione.
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// Dopo il confronto, il documento originale riceverà una nuova revisione
// per ogni elemento diverso nel documento modificato.
foreach (Revision r in docOriginal.Revisions)
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// Accettare queste revisioni trasformerà il documento originale nel documento modificato.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)

---

## Compare(Document, string, DateTime, CompareOptions) {#compare_1}

Confronta questo documento con un altro documento producendo modifiche come una serie di modifiche e revisioni del formato[`Revision`](../../revision/) . Permette di specificare le opzioni di confronto utilizzando[`CompareOptions`](../../../aspose.words.comparing/compareoptions/) .

```csharp
public void Compare(Document document, string author, DateTime dateTime, CompareOptions options)
```

### Esempi

Mostra come filtrare tipi specifici di elementi del documento quando si effettua un confronto.

```csharp
// Crea il documento originale e popolalo con vari tipi di elementi.
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);

// Testo del paragrafo referenziato con una nota finale:
builder.Writeln("Hello world! This is the first paragraph.");
builder.InsertFootnote(FootnoteType.Endnote, "Original endnote text.");

// Tavolo:
builder.StartTable();
builder.InsertCell();
builder.Write("Original cell 1 text");
builder.InsertCell();
builder.Write("Original cell 2 text");
builder.EndTable();

// Casella di testo:
Shape textBox = builder.InsertShape(ShapeType.TextBox, 150, 20);
builder.MoveTo(textBox.FirstParagraph);
builder.Write("Original textbox contents");

// Campo DATA:
builder.MoveTo(docOriginal.FirstSection.Body.AppendParagraph(""));
builder.InsertField(" DATE ");

// Commento:
Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", DateTime.Now);
newComment.SetText("Original comment.");
builder.CurrentParagraph.AppendChild(newComment);

// Intestazione:
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Original header contents.");

// Crea un clone del nostro documento ed esegui una rapida modifica su ciascuno degli elementi del documento clonato.
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

// Il confronto dei documenti crea una revisione per ogni modifica nel documento modificato.
// Un oggetto CompareOptions dispone di una serie di flag che possono eliminare le revisioni
// su ciascun rispettivo tipo di elemento, ignorando di fatto la loro modifica.
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

### Guarda anche

* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)


