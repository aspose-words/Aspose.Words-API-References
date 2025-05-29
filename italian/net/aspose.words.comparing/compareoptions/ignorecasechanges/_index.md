---
title: CompareOptions.IgnoreCaseChanges
linktitle: IgnoreCaseChanges
articleTitle: IgnoreCaseChanges
second_title: Aspose.Words per .NET
description: Scopri come la proprietà IgnoreCaseChanges di CompareOptions migliora il confronto dei documenti consentendo un'analisi senza distinzione tra maiuscole e minuscole per risultati accurati.
type: docs
weight: 50
url: /it/net/aspose.words.comparing/compareoptions/ignorecasechanges/
---
## CompareOptions.IgnoreCaseChanges property

Vero indica che il confronto dei documenti non distingue tra maiuscole e minuscole.

```csharp
public bool IgnoreCaseChanges { get; set; }
```

## Osservazioni

Per impostazione predefinita, il confronto è sensibile alle maiuscole e alle minuscole.

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

* class [CompareOptions](../)
* spazio dei nomi [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* assemblea [Aspose.Words](../../../)
