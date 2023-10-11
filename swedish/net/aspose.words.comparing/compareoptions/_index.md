---
title: Class CompareOptions
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Comparing.CompareOptions klass. Gör det möjligt att välja avancerade alternativ för dokumentjämförelse.
type: docs
weight: 270
url: /sv/net/aspose.words.comparing/compareoptions/
---
## CompareOptions class

Gör det möjligt att välja avancerade alternativ för dokumentjämförelse.

För att lära dig mer, besök[Jämför dokument](https://docs.aspose.com/words/net/compare-documents/) dokumentationsartikel.

```csharp
public class CompareOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [CompareOptions](compareoptions/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CompareMoves](../../aspose.words.comparing/compareoptions/comparemoves/) { get; set; } | Anger om skillnader iMoveRevision mellan de två dokumenten. Som standard produceras inga flyttversioner. |
| [Granularity](../../aspose.words.comparing/compareoptions/granularity/) { get; set; } | Anger om ändringar spåras med tecken eller ord. Standardvärdet ärWordLevel . |
| [IgnoreCaseChanges](../../aspose.words.comparing/compareoptions/ignorecasechanges/) { get; set; } | True indikerar att dokumentjämförelse är skiftlägesokänslig. Som standard är jämförelse skiftlägeskänslig. |
| [IgnoreComments](../../aspose.words.comparing/compareoptions/ignorecomments/) { get; set; } | Anger om skillnader i kommentarer ska jämföras. Som standard ignoreras inte kommentarer. |
| [IgnoreDmlUniqueId](../../aspose.words.comparing/compareoptions/ignoredmluniqueid/) { get; set; } | Anger om skillnaden i DrawingML unika Id. ska ignoreras. Standardvärdet är`falsk` . |
| [IgnoreFields](../../aspose.words.comparing/compareoptions/ignorefields/) { get; set; } | Anger om skillnader i fält ska jämföras. Som standard ignoreras inte fält. |
| [IgnoreFootnotes](../../aspose.words.comparing/compareoptions/ignorefootnotes/) { get; set; } | Anger om skillnader i fotnoter och slutnoter ska jämföras. Som standard ignoreras inte fotnoter. |
| [IgnoreFormatting](../../aspose.words.comparing/compareoptions/ignoreformatting/) { get; set; } | True indikerar att formatering ignoreras. Som standard ignoreras inte dokumentformatering. |
| [IgnoreHeadersAndFooters](../../aspose.words.comparing/compareoptions/ignoreheadersandfooters/) { get; set; } | True indikerar att innehållet i sidhuvuden och sidfötter ignoreras. Som standard ignoreras inte sidhuvuden och sidfötter. |
| [IgnoreTables](../../aspose.words.comparing/compareoptions/ignoretables/) { get; set; } | Anger om skillnaderna i data i tabeller ska jämföras. Som standard ignoreras inte tabeller. |
| [IgnoreTextboxes](../../aspose.words.comparing/compareoptions/ignoretextboxes/) { get; set; } | Anger om skillnader i data i textrutor ska jämföras. Som standard ignoreras inte textrutor. |
| [Target](../../aspose.words.comparing/compareoptions/target/) { get; set; } | Anger vilket dokument som ska användas som mål vid jämförelse. |

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

// DATUMfält:
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

* namnutrymme [Aspose.Words.Comparing](../../aspose.words.comparing/)
* hopsättning [Aspose.Words](../../)


