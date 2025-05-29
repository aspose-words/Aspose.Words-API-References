---
title: CompareOptions.IgnoreComments
linktitle: IgnoreComments
articleTitle: IgnoreComments
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen CompareOptions IgnoreComments förbättrar din jämförelse genom att exkludera kommentarskillnader för tydligare resultat.
type: docs
weight: 60
url: /sv/net/aspose.words.comparing/compareoptions/ignorecomments/
---
## CompareOptions.IgnoreComments property

Anger om skillnader i kommentarer ska jämföras.

```csharp
public bool IgnoreComments { get; set; }
```

## Anmärkningar

Som standard ignoreras inte kommentarer.

## Exempel

Visar hur man filtrerar specifika typer av dokumentelement vid en jämförelse.

```csharp
// Skapa originaldokumentet och fyll det med olika typer av element.
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

// DATUM-fält:
builder.MoveTo(docOriginal.FirstSection.Body.AppendParagraph(""));
builder.InsertField(" DATE ");

// Kommentar:
Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", DateTime.Now);
newComment.SetText("Original comment.");
builder.CurrentParagraph.AppendChild(newComment);

// Rubrik:
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Original header contents.");

// Skapa en klon av vårt dokument och utför en snabb redigering på vart och ett av det klonade dokumentets element.
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
// på varje respektive typ av element, vilket effektivt ignorerar deras förändring.
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

### Se även

* class [CompareOptions](../)
* namnutrymme [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* hopsättning [Aspose.Words](../../../)
