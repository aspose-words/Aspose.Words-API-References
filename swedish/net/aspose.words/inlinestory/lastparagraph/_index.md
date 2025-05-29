---
title: InlineStory.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words för .NET
description: Upptäck egenskapen InlineStory LastParagraph för att enkelt komma åt det sista stycket i din berättelse och förbättra din innehållshantering.
type: docs
weight: 70
url: /sv/net/aspose.words/inlinestory/lastparagraph/
---
## InlineStory.LastParagraph property

Hämtar det sista stycket i berättelsen.

```csharp
public Paragraph LastParagraph { get; }
```

## Exempel

Visar hur man infogar InlineStory-noder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, null);

// Tabellnoder har en "EnsureMinimum()"-metod som säkerställer att tabellen har minst en cell.
Table table = new Table(doc);
table.EnsureMinimum();

// Vi kan placera en tabell inuti en fotnot, vilket gör att den visas i sidfoten på den refererande sidan.
Assert.AreEqual(0, footnote.Tables.Count);
footnote.AppendChild(table);
Assert.AreEqual(1, footnote.Tables.Count);
Assert.AreEqual(NodeType.Table, footnote.LastChild.NodeType);

// En InlineStory har också en "EnsureMinimum()"-metod, men i det här fallet,
// det säkerställer att nodens sista barn är ett stycke,
// för att vi enkelt ska kunna klicka och skriva text i Microsoft Word.
footnote.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, footnote.LastChild.NodeType);

// Redigera utseendet på ankaret, vilket är det lilla upphöjda numret
// i huvudtexten som pekar till fotnoten.
footnote.Font.Name = "Arial";
footnote.Font.Color = Color.Green;

// Alla inline-berättelsenoder har sina respektive berättelsetyper.
Assert.AreEqual(StoryType.Footnotes, footnote.StoryType);

// En kommentar är en annan typ av inbäddad berättelse.
Comment comment = (Comment)builder.CurrentParagraph.AppendChild(new Comment(doc, "John Doe", "J. D.", DateTime.Now));

// Det överordnade stycket till en inline-artikelnod kommer att vara det från dokumentets huvudsakliga brödtext.
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, comment.ParentParagraph);

// Det sista stycket är dock det från kommentartextens innehåll,
// som kommer att finnas utanför dokumentets huvudtext i en pratbubbla.
// En kommentar kommer som standard inte att ha några underordnade noder,
// så vi kan använda EnsureMinimum()-metoden för att placera ett stycke här också.
Assert.Null(comment.LastParagraph);
comment.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, comment.LastChild.NodeType);

// När vi har ett stycke kan vi flytta verktyget för att göra det och skriva vår kommentar.
builder.MoveTo(comment.LastParagraph);
builder.Write("My comment.");

Assert.AreEqual(StoryType.Comments, comment.StoryType);

doc.Save(ArtifactsDir + "InlineStory.InsertInlineStoryNodes.docx");
```

### Se även

* class [Paragraph](../../paragraph/)
* class [InlineStory](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
