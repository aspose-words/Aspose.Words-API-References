---
title: Document.Compare
linktitle: Compare
articleTitle: Compare
second_title: Aspose.Words per .NET
description: Confronta i documenti senza sforzo con il nostro strumento di confronto documenti. Individua rapidamente modifiche e cambiamenti di formato per revisioni semplificate e una collaborazione migliorata.
type: docs
weight: 600
url: /it/net/aspose.words/document/compare/
---
## Compare(*[Document](../), string, DateTime*) {#compare}

Confronta questo documento con un altro documento che produce modifiche come numero di revisioni di modifica e formato[`Revision`](../../revision/) .

```csharp
public void Compare(Document document, string author, DateTime dateTime)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| document | Document | Documento da confrontare. |
| author | String | Iniziali dell'autore da utilizzare per le revisioni. |
| dateTime | DateTime | Data e ora da utilizzare per le revisioni. |

## Osservazioni

I documenti non devono avere revisioni prima del confronto.

## Esempi

Mostra come confrontare i documenti.

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// Il confronto tra documenti e revisioni genererà un'eccezione.
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// Dopo il confronto, il documento originale otterrà una nuova revisione
// per ogni elemento diverso nel documento modificato.
foreach (Revision r in docOriginal.Revisions)
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// L'accettazione di queste revisioni trasformerà il documento originale nel documento modificato.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## Compare(*[Document](../), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_1}

Confronta questo documento con un altro documento che produce modifiche come un numero di revisioni di modifica e formato[`Revision`](../../revision/) . Consente di specificare le opzioni di confronto utilizzando[`CompareOptions`](../../../aspose.words.comparing/compareoptions/) .

```csharp
public void Compare(Document document, string author, DateTime dateTime, CompareOptions options)
```

## Esempi

Mostra come filtrare tipi specifici di elementi del documento quando si effettua un confronto.

```csharp
// Crea il documento originale e popolalo con vari tipi di elementi.
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);

// Testo del paragrafo a cui si fa riferimento con una nota finale:
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

// Creiamo un clone del nostro documento ed eseguiamo una modifica rapida su ciascuno degli elementi del documento clonato.
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

// Il confronto dei documenti crea una revisione per ogni modifica apportata al documento modificato.
// Un oggetto CompareOptions ha una serie di flag che possono sopprimere le revisioni
// su ogni rispettivo tipo di elemento, ignorando di fatto la loro modifica.
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

### Guarda anche

* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
