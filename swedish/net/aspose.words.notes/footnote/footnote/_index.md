---
title: Footnote.Footnote
second_title: Aspose.Words för .NET API Referens
description: Footnote byggare. Initierar en instans avFootnote class.
type: docs
weight: 10
url: /sv/net/aspose.words.notes/footnote/footnote/
---
## Footnote constructor

Initierar en instans av[`Footnote`](../) class.

```csharp
public Footnote(DocumentBase doc, FootnoteType footnoteType)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | DocumentBase | Ägardokumentet. |
| footnoteType | FootnoteType | A[`FootnoteType`](../footnotetype/) värde som anger om detta är en fotnot eller slutnot. |

### Anmärkningar

När[`Footnote`](../) skapas, det tillhör det angivna dokumentet, men är inte ännu en del av dokumentet och[`ParentNode`](../../../aspose.words/node/parentnode/) är`null`.

Att lägga till[`Footnote`](../) till dokumentanvändningenNode) ellerNode) på stycket där du vill infoga fotnoten.

### Exempel

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

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [FootnoteType](../../footnotetype/)
* class [Footnote](../)
* namnutrymme [Aspose.Words.Notes](../../footnote/)
* hopsättning [Aspose.Words](../../../)


