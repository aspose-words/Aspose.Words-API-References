---
title: InlineStory.Tables
linktitle: Tables
articleTitle: Tables
second_title: Aspose.Words för .NET
description: InlineStory Tables fast egendom. Får en samling tabeller som är omedelbara barn till berättelsen i C#.
type: docs
weight: 110
url: /sv/net/aspose.words/inlinestory/tables/
---
## InlineStory.Tables property

Får en samling tabeller som är omedelbara barn till berättelsen.

```csharp
public TableCollection Tables { get; }
```

## Exempel

Visar hur man infogar InlineStory-noder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, null);

// Tabellnoder har en "EnsureMinimum()"-metod som ser till att tabellen har minst en cell.
Table table = new Table(doc);
table.EnsureMinimum();

// Vi kan placera en tabell inuti en fotnot, vilket kommer att få den att visas i sidfoten på referenssidan.
Assert.That(footnote.Tables, Is.Empty);
footnote.AppendChild(table);
Assert.AreEqual(1, footnote.Tables.Count);
Assert.AreEqual(NodeType.Table, footnote.LastChild.NodeType);

// En InlineStory har också en "EnsureMinimum()"-metod, men i det här fallet,
// det ser till att det sista barnet i noden är ett stycke,
// för att vi enkelt ska kunna klicka och skriva text i Microsoft Word.
footnote.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, footnote.LastChild.NodeType);

// Redigera utseendet på ankaret, vilket är det lilla upphöjda numret
// i huvudtexten som pekar på fotnoten.
footnote.Font.Name = "Arial";
footnote.Font.Color = Color.Green;

// Alla inline-berättelsenoder har sina respektive berättelsetyper.
Assert.AreEqual(StoryType.Footnotes, footnote.StoryType);

// En kommentar är en annan typ av inline-berättelse.
Comment comment = (Comment)builder.CurrentParagraph.AppendChild(new Comment(doc, "John Doe", "J. D.", DateTime.Now));

// Det överordnade stycket i en inline-berättelsenod kommer att vara det från huvuddokumentet.
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, comment.ParentParagraph);

// Det sista stycket är dock det från kommentartextens innehåll,
// som kommer att vara utanför huvuddokumentet i en pratbubbla.
// En kommentar kommer inte att ha några underordnade noder som standard,
// så att vi kan använda metoden EnsureMinimum() för att placera ett stycke här också.
Assert.Null(comment.LastParagraph);
comment.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, comment.LastChild.NodeType);

// När vi har ett stycke kan vi flytta byggaren att göra det och skriva vår kommentar.
builder.MoveTo(comment.LastParagraph);
builder.Write("My comment.");

Assert.AreEqual(StoryType.Comments, comment.StoryType);

doc.Save(ArtifactsDir + "InlineStory.InsertInlineStoryNodes.docx");
```

### Se även

* class [TableCollection](../../../aspose.words.tables/tablecollection/)
* class [InlineStory](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
