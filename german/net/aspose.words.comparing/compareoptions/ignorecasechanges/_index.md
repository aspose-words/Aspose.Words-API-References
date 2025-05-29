---
title: CompareOptions.IgnoreCaseChanges
linktitle: IgnoreCaseChanges
articleTitle: IgnoreCaseChanges
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „CompareOptions IgnoreCaseChanges“ den Dokumentvergleich verbessert, indem sie eine Groß-/Kleinschreibung ignorierende Analyse für genaue Ergebnisse ermöglicht.
type: docs
weight: 50
url: /de/net/aspose.words.comparing/compareoptions/ignorecasechanges/
---
## CompareOptions.IgnoreCaseChanges property

„True“ bedeutet, dass beim Dokumentvergleich die Groß-/Kleinschreibung nicht beachtet wird.

```csharp
public bool IgnoreCaseChanges { get; set; }
```

## Bemerkungen

Standardmäßig wird beim Vergleich zwischen Groß- und Kleinschreibung unterschieden.

## Beispiele

Zeigt, wie beim Vergleichen bestimmte Typen von Dokumentelementen gefiltert werden.

```csharp
// Erstellen Sie das Originaldokument und füllen Sie es mit verschiedenen Arten von Elementen.
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);

// Absatztext, auf den mit einer Endnote verwiesen wird:
builder.Writeln("Hello world! This is the first paragraph.");
builder.InsertFootnote(FootnoteType.Endnote, "Original endnote text.");

// Tisch:
builder.StartTable();
builder.InsertCell();
builder.Write("Original cell 1 text");
builder.InsertCell();
builder.Write("Original cell 2 text");
builder.EndTable();

// Textfeld:
Shape textBox = builder.InsertShape(ShapeType.TextBox, 150, 20);
builder.MoveTo(textBox.FirstParagraph);
builder.Write("Original textbox contents");

// DATE-Feld:
builder.MoveTo(docOriginal.FirstSection.Body.AppendParagraph(""));
builder.InsertField(" DATE ");

// Kommentar:
Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", DateTime.Now);
newComment.SetText("Original comment.");
builder.CurrentParagraph.AppendChild(newComment);

// Kopfzeile:
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Original header contents.");

// Erstellen Sie einen Klon unseres Dokuments und führen Sie eine schnelle Bearbeitung an jedem Element des geklonten Dokuments durch.
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

// Beim Vergleichen von Dokumenten wird für jede Bearbeitung im bearbeiteten Dokument eine Revision erstellt.
// Ein CompareOptions-Objekt verfügt über eine Reihe von Flags, die Revisionen unterdrücken können
// auf jedem jeweiligen Elementtyp, wobei deren Änderung effektiv ignoriert wird.
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

### Siehe auch

* class [CompareOptions](../)
* namensraum [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* Montage [Aspose.Words](../../../)
