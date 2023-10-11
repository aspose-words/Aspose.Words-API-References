---
title: Enum FootnotePosition
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Notes.FootnotePosition uppräkning. Definierar fotnotspositionen.
type: docs
weight: 4290
url: /sv/net/aspose.words.notes/footnoteposition/
---
## FootnotePosition enumeration

Definierar fotnotspositionen.

```csharp
public enum FootnotePosition
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| BottomOfPage | `1` | Fotnoter matas ut längst ner på varje sida. |
| BeneathText | `2` | Fotnoter matas ut under texten på varje sida. |

### Exempel

Visar hur du väljer en annan plats där dokumentet samlas in och visar dess fotnoter.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// En fotnot är ett sätt att bifoga en referens eller en sidokommentar till text
 // som inte stör flödet i huvudtexten.
// Att infoga en fotnot lägger till en liten upphöjd referenssymbol
// vid huvudtexten där vi infogar fotnoten.
// Varje fotnot skapar också en post längst ner på sidan, bestående av en symbol
// som matchar referenssymbolen i huvudtexten.
// Referenstexten som vi skickar till dokumentbyggarens "InsertFootnote"-metod.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// Vi kan använda egenskapen "Position" för att bestämma var dokumentet ska placera alla dess fotnoter.
// Om vi ställer in värdet för egenskapen "Position" till "FootnotePosition.BottomOfPage",
// varje fotnot kommer att dyka upp längst ner på sidan som innehåller dess referensmärke. Detta är standardvärdet.
// Om vi ställer in värdet på egenskapen "Position" till "FootnotePosition.BeneathText",
// varje fotnot kommer att dyka upp i slutet av sidans text som innehåller dess referensmärke.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

### Se även

* class [FootnoteOptions](../footnoteoptions/)
* namnutrymme [Aspose.Words.Notes](../../aspose.words.notes/)
* hopsättning [Aspose.Words](../../)


