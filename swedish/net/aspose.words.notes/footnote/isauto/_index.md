---
title: Footnote.IsAuto
linktitle: IsAuto
articleTitle: IsAuto
second_title: Aspose.Words för .NET
description: Upptäck IsAuto-egenskapen för fotnoter, vilket möjliggör sömlös autonumrering eller anpassade referensmarkeringar för förbättrad dokumenttydlighet och organisation.
type: docs
weight: 40
url: /sv/net/aspose.words.notes/footnote/isauto/
---
## Footnote.IsAuto property

Innehåller ett värde som anger om detta är en automatiskt numrerad fotnot eller en fotnot med användardefinierat anpassat referensmärke.

```csharp
public bool IsAuto { get; set; }
```

## Anmärkningar

[`ReferenceMark`](../referencemark/) initierad med tom sträng om`IsAuto` inställd på`falsk` .

## Exempel

Visar hur man infogar och anpassar fotnoter.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Lägg till text och referera till den med en fotnot. Denna fotnot placerar en liten upphöjd referens
// markera efter texten som den refererar till och skapa en post under huvudtexten längst ner på sidan.
// Denna post kommer att innehålla fotnotens referensmärke och referenstexten,
// som vi skickar till dokumentbyggarens "InsertFootnote"-metod.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Om den här egenskapen är satt till "sant", så är vår fotnots referensmarkering
// kommer att vara dess index bland alla avsnittets fotnoter.
// Detta är den första fotnoten, så referenstecknet blir "1".
Assert.True(footnote.IsAuto);

 // Vi kan flytta dokumentbyggaren inuti fotnoten för att redigera dess referenstext.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Vi kan ange ett anpassat referensmärke som fotnoten kommer att använda istället för sitt indexnummer.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// Ett bokmärke med flaggan "IsAuto" satt till sant kommer fortfarande att visa sitt verkliga index
// även om tidigare bokmärken visar anpassade referensmarkeringar, så kommer detta bokmärkes referensmarkering att vara en "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Se även

* class [Footnote](../)
* namnutrymme [Aspose.Words.Notes](../../../aspose.words.notes/)
* hopsättning [Aspose.Words](../../../)
