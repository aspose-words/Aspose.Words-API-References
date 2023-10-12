---
title: Enum EndnotePosition
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Notes.EndnotePosition uppräkning. Definierar slutnotens position.
type: docs
weight: 4250
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
| EndOfDocument | `3` | Slutanteckningar matas ut i slutet av dokumentet. |

### Exempel

Visar hur du väljer en annan plats där dokumentet samlas in och visar dess slutanteckningar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// En slutnot är ett sätt att bifoga en referens eller en sidokommentar till text
 // som inte stör flödet i huvudtexten.
// Att infoga en slutnot lägger till en liten upphöjd referenssymbol
// vid huvudtexten där vi infogar slutnoten.
// Varje slutnot skapar också en post i slutet av dokumentet, bestående av en symbol
// som matchar referenssymbolen i huvudtexten.
// Referenstexten som vi skickar till dokumentbyggarens "InsertEndnote"-metod.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote contents.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("This is the second section.");

// Vi kan använda egenskapen "Position" för att bestämma var dokumentet ska placera alla sina slutnoter.
// Om vi ställer in värdet på egenskapen "Position" till "EndnotePosition.EndOfDocument",
// varje fotnot kommer att dyka upp i en samling i slutet av dokumentet. Detta är standardvärdet.
// Om vi ställer in värdet på egenskapen "Position" till "EndnotePosition.EndOfSection",
// varje fotnot kommer att dyka upp i en samling i slutet av avsnittet vars text innehåller slutnotens referensmärke.
doc.EndnoteOptions.Position = endnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionEndnote.docx");
```

### Se även

* class [EndnoteOptions](../endnoteoptions/)
* namnutrymme [Aspose.Words.Notes](../../aspose.words.notes/)
* hopsättning [Aspose.Words](../../)


