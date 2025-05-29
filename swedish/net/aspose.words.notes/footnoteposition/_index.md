---
title: FootnotePosition Enum
linktitle: FootnotePosition
articleTitle: FootnotePosition
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Notes.FootnotePosition-uppräkningen för anpassningsbar fotnotsplacering, vilket förbättrar dokumentformatering och läsbarhet.
type: docs
weight: 4980
url: /sv/net/aspose.words.notes/footnoteposition/
---
## FootnotePosition enumeration

Definierar fotnotens position.

```csharp
public enum FootnotePosition
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| BottomOfPage | `1` | Fotnoter visas längst ner på varje sida. |
| BeneathText | `2` | Fotnoter visas under texten på varje sida. |

## Exempel

Visar hur man väljer en annan plats där dokumentet samlas och visar sina fotnoter.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// En fotnot är ett sätt att lägga till en referens eller en sidokommentar till text
 // som inte stör huvudtextens flöde.
// Om du infogar en fotnot läggs en liten upphöjd referenssymbol till
// vid huvudtexten där vi infogar fotnoten.
// Varje fotnot skapar också en post längst ner på sidan, bestående av en symbol
// som matchar referenssymbolen i huvudtexten.
// Referenstexten som vi skickar till dokumentbyggarens metod "InsertFootnote".
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// Vi kan använda egenskapen "Position" för att avgöra var dokumentet ska placera alla sina fotnoter.
// Om vi ställer in värdet för egenskapen "Position" till "FootnotePosition.BottomOfPage",
// varje fotnot visas längst ner på sidan som innehåller dess referensmarkering. Detta är standardvärdet.
// Om vi ställer in värdet för egenskapen "Position" till "FootnotePosition.BeneathText",
// varje fotnot kommer att visas i slutet av sidans text som innehåller dess referensmarkering.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

### Se även

* class [FootnoteOptions](../footnoteoptions/)
* namnutrymme [Aspose.Words.Notes](../../aspose.words.notes/)
* hopsättning [Aspose.Words](../../)
