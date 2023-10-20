---
title: ComparisonTargetType Enum
linktitle: ComparisonTargetType
articleTitle: ComparisonTargetType
second_title: Aspose.Words für .NET
description: Aspose.Words.Comparing.ComparisonTargetType opsomming. Ermöglicht die Angabe des Basisdokuments das beim Vergleich verwendet wird. Der Standardwert istCurrent  in C#.
type: docs
weight: 280
url: /de/net/aspose.words.comparing/comparisontargettype/
---
## ComparisonTargetType enumeration

Ermöglicht die Angabe des Basisdokuments, das beim Vergleich verwendet wird. Der Standardwert istCurrent .

```csharp
public enum ComparisonTargetType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Current | `0` | Dieses Dokument dient als Grundlage für den Vergleich. |
| New | `1` | Anderes Dokument wird beim Vergleich als Basis verwendet. |

## Bemerkungen

Bezieht sich auf die Microsoft Word-Option „Änderungen anzeigen in“ im Dialogfeld „Dokumente vergleichen“.

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
