---
title: Enum FootnoteType
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Notes.FootnoteType uppräkning. Anger om detta är en fotnot eller en slutnot.
type: docs
weight: 4300
url: /sv/net/aspose.words.notes/footnotetype/
---
## FootnoteType enumeration

Anger om detta är en fotnot eller en slutnot.

```csharp
public enum FootnoteType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Footnote | `0` | Objektet är en fotnot. |
| Endnote | `1` | Objektet är en slutnot. |

### Anmärkningar

Både fotnoter och slutnoter representeras av objekt avFootnote klass. Använda sig av[`FootnoteType`](../footnote/footnotetype/) för att skilja mellan fotnoter och slutnoter.

### Exempel

Visar hur man refererar till text med en fotnot och en slutnot.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga lite text och markera den med en fotnot med egenskapen IsAuto inställd på "true" som standard,
// så markören som syns i brödtexten kommer att automatiskt numreras vid "1",
// och fotnoten kommer att visas längst ner på sidan.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Infoga mer text och markera den med en slutnot med ett anpassat referensmärke,
// som kommer att användas i stället för siffran "2" och ställ in "IsAuto" till false.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Fotnoter visas alltid längst ner i den refererade texten,
// så denna sidbrytning kommer inte att påverka fotnoten.
// Å andra sidan är slutnoter alltid i slutet av dokumentet
// så att denna sidbrytning kommer att trycka ner slutnoten till nästa sida.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

Visar hur man infogar och anpassar fotnoter.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Lägg till text och referera till den med en fotnot. Denna fotnot kommer att placera en liten upphöjd referens
// markera efter texten som den refererar till och skapa en post under huvudtexten längst ner på sidan.
// Denna post kommer att innehålla fotnotens referensmärke och referenstexten,
// som vi kommer att skicka till dokumentbyggarens "InsertFootnote"-metod.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Om den här egenskapen är inställd på "true", är vår fotnots referensmärke
// kommer att vara dess index bland alla avsnittets fotnoter.
// Detta är den första fotnoten, så referensmärket blir "1".
Assert.True(footnote.IsAuto);

 // Vi kan flytta dokumentbyggaren inuti fotnoten för att redigera dess referenstext.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Vi kan ställa in ett anpassat referensmärke som fotnoten kommer att använda istället för dess indexnummer.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// Ett bokmärke med flaggan "IsAuto" inställd på sant kommer fortfarande att visa sitt verkliga index
// även om tidigare bokmärken visar anpassade referensmärken, så kommer detta bokmärkes referensmärke att vara en "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Se även

* namnutrymme [Aspose.Words.Notes](../../aspose.words.notes/)
* hopsättning [Aspose.Words](../../)


