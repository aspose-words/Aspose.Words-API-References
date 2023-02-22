---
title: Class CompareOptions
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Comparing.CompareOptions classe. Consente di scegliere le opzioni avanzate per loperazione di confronto dei documenti.
type: docs
weight: 260
url: /it/net/aspose.words.comparing/compareoptions/
---
## CompareOptions class

Consente di scegliere le opzioni avanzate per l'operazione di confronto dei documenti.

```csharp
public class CompareOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [CompareOptions](compareoptions/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Granularity](../../aspose.words.comparing/compareoptions/granularity/) { get; set; } | Specifica se le modifiche vengono tracciate per carattere o per parola. Il valore predefinito èWordLevel . |
| [IgnoreCaseChanges](../../aspose.words.comparing/compareoptions/ignorecasechanges/) { get; set; } | True indica che il confronto dei documenti non fa distinzione tra maiuscole e minuscole. Per impostazione predefinita, il confronto fa distinzione tra maiuscole e minuscole. |
| [IgnoreComments](../../aspose.words.comparing/compareoptions/ignorecomments/) { get; set; } | Specifica se confrontare le differenze nei commenti. Per impostazione predefinita i commenti non vengono ignorati. |
| [IgnoreDmlUniqueId](../../aspose.words.comparing/compareoptions/ignoredmluniqueid/) { get; set; } | Specifica se ignorare la differenza nell'ID univoco di DrawingML. Il valore predefinito è **falso** . |
| [IgnoreFields](../../aspose.words.comparing/compareoptions/ignorefields/) { get; set; } | Specifica se confrontare le differenze nei campi. Per impostazione predefinita i campi non vengono ignorati. |
| [IgnoreFootnotes](../../aspose.words.comparing/compareoptions/ignorefootnotes/) { get; set; } | Specifica se confrontare le differenze nelle note a piè di pagina e nelle note di chiusura. Per impostazione predefinita, le note a piè di pagina non vengono ignorate. |
| [IgnoreFormatting](../../aspose.words.comparing/compareoptions/ignoreformatting/) { get; set; } | True indica che la formattazione viene ignorata. Per impostazione predefinita, la formattazione del documento non viene ignorata. |
| [IgnoreHeadersAndFooters](../../aspose.words.comparing/compareoptions/ignoreheadersandfooters/) { get; set; } | True indica che il contenuto di intestazioni e piè di pagina viene ignorato. Per impostazione predefinita, intestazioni e piè di pagina non vengono ignorati. |
| [IgnoreTables](../../aspose.words.comparing/compareoptions/ignoretables/) { get; set; } | Specifica se confrontare le differenze nei dati contenuti nelle tabelle. Per impostazione predefinita, le tabelle non vengono ignorate. |
| [IgnoreTextboxes](../../aspose.words.comparing/compareoptions/ignoretextboxes/) { get; set; } | Specifica se confrontare le differenze nei dati contenuti nelle caselle di testo. Per impostazione predefinita, le caselle di testo non vengono ignorate. |
| [Target](../../aspose.words.comparing/compareoptions/target/) { get; set; } | Specifica quale documento deve essere utilizzato come destinazione durante il confronto. |

### Esempi

Mostra come filtrare tipi specifici di elementi del documento quando si effettua un confronto.

```csharp
// Crea il documento originale e popolalo con vari tipi di elementi.
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);

// Testo del paragrafo a cui si fa riferimento con una nota di chiusura:
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
// Un oggetto CompareOptions ha una serie di flag che possono sopprimere le revisioni
// su ogni rispettivo tipo di elemento, ignorando di fatto la loro modifica.
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

* spazio dei nomi [Aspose.Words.Comparing](../../aspose.words.comparing/)
* assemblea [Aspose.Words](../../)


