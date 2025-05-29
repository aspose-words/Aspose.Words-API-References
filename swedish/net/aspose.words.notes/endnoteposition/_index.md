---
title: EndnotePosition Enum
linktitle: EndnotePosition
articleTitle: EndnotePosition
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words EndnotePosition-enum för exakt kontroll över placeringen av slutnoter i dokument, vilket förbättrar dina textformateringsmöjligheter.
type: docs
weight: 4940
url: /sv/net/aspose.words.notes/endnoteposition/
---
## EndnotePosition enumeration

Definierar slutnotens position.

```csharp
public enum EndnotePosition
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| EndOfSection | `0` | Slutnoter matas ut i slutet av avsnittet. |
| EndOfDocument | `3` | Slutnoter matas ut i slutet av dokumentet. |

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

* class [EndnoteOptions](../endnoteoptions/)
* namnutrymme [Aspose.Words.Notes](../../aspose.words.notes/)
* hopsättning [Aspose.Words](../../)
