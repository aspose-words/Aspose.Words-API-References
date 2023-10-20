---
title: CompareOptions Class
linktitle: CompareOptions
articleTitle: CompareOptions
second_title: Aspose.Words für .NET
description: Aspose.Words.Comparing.CompareOptions klas. Ermöglicht die Auswahl erweiterter Optionen für den Dokumentvergleichsvorgang in C#.
type: docs
weight: 270
url: /de/net/aspose.words.comparing/compareoptions/
---
## CompareOptions class

Ermöglicht die Auswahl erweiterter Optionen für den Dokumentvergleichsvorgang.

Um mehr zu erfahren, besuchen Sie die[Dokumente vergleichen](https://docs.aspose.com/words/net/compare-documents/) Dokumentationsartikel.

```csharp
public class CompareOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [CompareOptions](compareoptions/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CompareMoves](../../aspose.words.comparing/compareoptions/comparemoves/) { get; set; } | Gibt an, ob Unterschiede verglichen werden sollenMoveRevision zwischen den beiden Dokumenten. Standardmäßig werden keine Revisionen beim Verschieben erstellt. |
| [Granularity](../../aspose.words.comparing/compareoptions/granularity/) { get; set; } | Gibt an, ob Änderungen nach Zeichen oder Wort verfolgt werden. Der Standardwert istWordLevel . |
| [IgnoreCaseChanges](../../aspose.words.comparing/compareoptions/ignorecasechanges/) { get; set; } | True gibt an, dass beim Dokumentenvergleich die Groß-/Kleinschreibung nicht beachtet wird. Standardmäßig wird beim Vergleich die Groß-/Kleinschreibung beachtet. |
| [IgnoreComments](../../aspose.words.comparing/compareoptions/ignorecomments/) { get; set; } | Gibt an, ob Unterschiede in Kommentaren verglichen werden sollen. Standardmäßig werden Kommentare nicht ignoriert. |
| [IgnoreDmlUniqueId](../../aspose.words.comparing/compareoptions/ignoredmluniqueid/) { get; set; } | Gibt an, ob Unterschiede in der eindeutigen DrawingML-ID ignoriert werden sollen. Der Standardwert ist`FALSCH` . |
| [IgnoreFields](../../aspose.words.comparing/compareoptions/ignorefields/) { get; set; } | Gibt an, ob Unterschiede in Feldern verglichen werden sollen. Standardmäßig werden Felder nicht ignoriert. |
| [IgnoreFootnotes](../../aspose.words.comparing/compareoptions/ignorefootnotes/) { get; set; } | Gibt an, ob Unterschiede in Fußnoten und Endnoten verglichen werden sollen. Standardmäßig werden Fußnoten nicht ignoriert. |
| [IgnoreFormatting](../../aspose.words.comparing/compareoptions/ignoreformatting/) { get; set; } | True gibt an, dass die Formatierung ignoriert wird. Standardmäßig wird die Dokumentformatierung nicht ignoriert. |
| [IgnoreHeadersAndFooters](../../aspose.words.comparing/compareoptions/ignoreheadersandfooters/) { get; set; } | True gibt an, dass der Inhalt von Kopf- und Fußzeilen ignoriert wird. Standardmäßig werden Kopf- und Fußzeilen nicht ignoriert. |
| [IgnoreTables](../../aspose.words.comparing/compareoptions/ignoretables/) { get; set; } | Gibt an, ob die Unterschiede in den in Tabellen enthaltenen Daten verglichen werden sollen. Standardmäßig werden Tabellen nicht ignoriert. |
| [IgnoreTextboxes](../../aspose.words.comparing/compareoptions/ignoretextboxes/) { get; set; } | Gibt an, ob Unterschiede in den in Textfeldern enthaltenen Daten verglichen werden sollen. Standardmäßig werden Textfelder nicht ignoriert. |
| [Target](../../aspose.words.comparing/compareoptions/target/) { get; set; } | Gibt an, welches Dokument beim Vergleich als Ziel verwendet werden soll. |

## Beispiele

Zeigt, wie bei einem Vergleich bestimmte Arten von Dokumentelementen gefiltert werden.

```csharp
// Das Originaldokument erstellen und es mit verschiedenen Arten von Elementen füllen.
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

// Header:
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
// für jeden jeweiligen Elementtyp, wobei deren Änderung effektiv ignoriert wird.
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

### Siehe auch

* namensraum [Aspose.Words.Comparing](../../aspose.words.comparing/)
* Montage [Aspose.Words](../../)
