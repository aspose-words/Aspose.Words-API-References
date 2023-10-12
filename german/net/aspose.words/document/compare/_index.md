---
title: Document.Compare
second_title: Aspose.Words für .NET-API-Referenz
description: Document methode. Vergleicht dieses Dokument mit einem anderen Dokument und erzeugt Änderungen als Anzahl der Bearbeitungs und FormatrevisionenRevision .
type: docs
weight: 580
url: /de/net/aspose.words/document/compare/
---
## Compare(Document, string, DateTime) {#compare}

Vergleicht dieses Dokument mit einem anderen Dokument und erzeugt Änderungen als Anzahl der Bearbeitungs- und Formatrevisionen[`Revision`](../../revision/) .

```csharp
public void Compare(Document document, string author, DateTime dateTime)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| document | Document | Dokument zum Vergleichen. |
| author | String | Initialen des Autors zur Verwendung bei Überarbeitungen. |
| dateTime | DateTime | Das für Überarbeitungen zu verwendende Datum und die Uhrzeit. |

### Bemerkungen

Dokumente dürfen vor dem Vergleich nicht überarbeitet werden.

### Beispiele

Zeigt, wie Dokumente verglichen werden.

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// Beim Vergleich von Dokumenten mit Revisionen wird eine Ausnahme ausgelöst.
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// Nach dem Vergleich erhält das Originaldokument eine neue Revision
// für jedes Element, das im bearbeiteten Dokument anders ist.
foreach (Revision r in docOriginal.Revisions)
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// Durch das Akzeptieren dieser Überarbeitungen wird das Originaldokument in das bearbeitete Dokument umgewandelt.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)

---

## Compare(Document, string, DateTime, CompareOptions) {#compare_1}

Vergleicht dieses Dokument mit einem anderen Dokument und führt zu Änderungen in Form einer Reihe von Bearbeitungs- und Formatrevisionen[`Revision`](../../revision/) . Ermöglicht die Angabe von Vergleichsoptionen mit[`CompareOptions`](../../../aspose.words.comparing/compareoptions/) .

```csharp
public void Compare(Document document, string author, DateTime dateTime, CompareOptions options)
```

### Beispiele

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

* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)


