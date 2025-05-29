---
title: EndnoteOptions.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen EndnoteOptions Position förbättrar ditt dokuments layout genom att ange den ideala placeringen för slutnoter. Optimera ditt skrivande idag!
type: docs
weight: 20
url: /sv/net/aspose.words.notes/endnoteoptions/position/
---
## EndnoteOptions.Position property

Anger slutnoternas position.

```csharp
public EndnotePosition Position { get; set; }
```

## Exempel

Visar hur man väljer en annan plats där dokumentet samlar in och visar sina slutnoter.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// En slutnot är ett sätt att lägga till en referens eller en sidokommentar till text
 // som inte stör huvudtextens flöde.
// Om du infogar en slutnot läggs en liten upphöjd referenssymbol till
// i huvudtexten där vi infogar slutnoten.
// Varje slutnot skapar också en post i slutet av dokumentet, bestående av en symbol
// som matchar referenssymbolen i huvudtexten.
// Referenstexten som vi skickar till dokumentbyggarens "InsertEndnote"-metod.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote contents.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("This is the second section.");

// Vi kan använda egenskapen "Position" för att avgöra var dokumentet ska placera alla sina slutnoter.
// Om vi ställer in värdet för egenskapen "Position" till "EndnotePosition.EndOfDocument",
// varje fotnot kommer att visas i en samling i slutet av dokumentet. Detta är standardvärdet.
// Om vi ställer in värdet för egenskapen "Position" till "EndnotePosition.EndOfSection",
// varje fotnot kommer att visas i en samling i slutet av det avsnitt vars text innehåller slutnotens referensmarkering.
doc.EndnoteOptions.Position = endnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionEndnote.docx");
```

### Se även

* enum [EndnotePosition](../../endnoteposition/)
* class [EndnoteOptions](../)
* namnutrymme [Aspose.Words.Notes](../../../aspose.words.notes/)
* hopsättning [Aspose.Words](../../../)
