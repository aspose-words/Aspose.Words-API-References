---
title: Compare
second_title: Aspose.Words för .NET API Referens
description: Jämför detta dokument med ett annat dokument som ger ändringar som antal redigeringar och formatrevisionerRevisionaspose.words/revision .
type: docs
weight: 540
url: /sv/net/aspose.words/document/compare/
---
## Compare(Document, string, DateTime) {#compare}

Jämför detta dokument med ett annat dokument som ger ändringar som antal redigeringar och formatrevisioner[`Revision`](../../revision) .

```csharp
public void Compare(Document document, string author, DateTime dateTime)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| document | Document | Dokument att jämföra. |
| author | String | Författarens initialer att använda för revisioner. |
| dateTime | DateTime | Datum och tid som ska användas för revisioner. |

### Anmärkningar

Följande dokumentnoder jämförs inte för tillfället:

* [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag)
* Artikel 3

Dokument får inte ha revideringar före jämförelse.

### Exempel

Visar hur man jämför dokument.

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// Att jämföra dokument med revisioner ger ett undantag.
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// Efter jämförelsen kommer originaldokumentet att få en ny version
// för varje element som är olika i det redigerade dokumentet.
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// Om du accepterar dessa ändringar förvandlas originaldokumentet till det redigerade dokumentet.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### Se även

* class [Document](../../document)
* namnutrymme [Aspose.Words](../../document)
* hopsättning [Aspose.Words](../../../)

---

## Compare(Document, string, DateTime, CompareOptions) {#compare_1}

Jämför detta dokument med ett annat dokument som ger ändringar som ett antal redigerings- och formatrevisioner[`Revision`](../../revision) . Gör det möjligt att ange jämförelsealternativ med hjälp av[`CompareOptions`](../../../aspose.words.comparing/compareoptions) .

```csharp
public void Compare(Document document, string author, DateTime dateTime, CompareOptions options)
```

### Exempel

Visar hur man filtrerar specifika typer av dokumentelement när man gör en jämförelse.

```csharp
// Skapa originaldokumentet och fyll i det med olika typer av element.
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);

// Stycketext refererad med en slutnot:
builder.Writeln("Hello world! This is the first paragraph.");
builder.InsertFootnote(FootnoteType.Endnote, "Original endnote text.");

// Tabell:
builder.StartTable();
builder.InsertCell();
builder.Write("Original cell 1 text");
builder.InsertCell();
builder.Write("Original cell 2 text");
builder.EndTable();

// Textruta:
Shape textBox = builder.InsertShape(ShapeType.TextBox, 150, 20);
builder.MoveTo(textBox.FirstParagraph);
builder.Write("Original textbox contents");

// DATE-fält:
builder.MoveTo(docOriginal.FirstSection.Body.AppendParagraph(""));
builder.InsertField(" DATE ");

// Kommentar:
Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", DateTime.Now);
newComment.SetText("Original comment.");
builder.CurrentParagraph.AppendChild(newComment);

// Header:
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Original header contents.");

// Skapa en klon av vårt dokument och utför en snabb redigering av vart och ett av det klonade dokumentets element.
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

// Att jämföra dokument skapar en revision för varje redigering i det redigerade dokumentet.
// Ett CompareOptions-objekt har en serie flaggor som kan undertrycka revisioner
// på varje respektive typ av element, i praktiken ignorerar deras förändring.
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

### Se även

* class [CompareOptions](../../../aspose.words.comparing/compareoptions)
* class [Document](../../document)
* namnutrymme [Aspose.Words](../../document)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
