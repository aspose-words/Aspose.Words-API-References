---
title: FootnoteOptions.StartNumber
linktitle: StartNumber
articleTitle: StartNumber
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FootnoteOptions StartNumber för att anpassa fotnotsnumreringen och enkelt förbättra dokumentets tydlighet och organisation.
type: docs
weight: 50
url: /sv/net/aspose.words.notes/footnoteoptions/startnumber/
---
## FootnoteOptions.StartNumber property

Anger startnumret eller tecknet för de första automatiskt numrerade fotnoterna.

```csharp
public int StartNumber { get; set; }
```

## Anmärkningar

Denna egenskap har endast effekt när[`RestartRule`](../restartrule/)är inställd på Continuous.

## Exempel

Visar hur man anger ett nummer där dokumentet börjar fotnots-/slutnoträkningen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fotnoter och slutnoter är ett sätt att lägga till en referens eller en sidokommentar till text
 // som inte stör huvudtextens flöde.
// Om du infogar en fotnot/slutnot läggs en liten upphöjd referenssymbol till
// i huvudtexten där vi infogar fotnoten/slutnoten.
// Varje fotnot/slutnot skapar också en post, som består av en symbol
// som matchar referenssymbolen i huvudtexten.
// Referenstexten som vi skickar till dokumentbyggarens "InsertEndnote"-metod.
// Fotnoter visas som standard längst ner på varje sida som innehåller
// deras referenssymboler och slutnoter visas i slutet av dokumentet.
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.");

builder.InsertParagraph();

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.");

// Som standard är referenssymbolen för varje fotnot och slutnot dess index
// bland alla dokumentets fotnoter/slutnoter. Varje dokument har separata räkningar
// för fotnoter och slutnoter, som båda börjar på 1.
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// Vi kan använda egenskapen "StartNumber" för att få dokumentet att
// börjar en fotnots- eller slutnoträkning vid ett annat nummer.
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

### Se även

* class [FootnoteOptions](../)
* namnutrymme [Aspose.Words.Notes](../../../aspose.words.notes/)
* hopsättning [Aspose.Words](../../../)
