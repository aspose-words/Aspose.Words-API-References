---
title: FootnoteOptions.Position
second_title: Aspose.Words för .NET API Referens
description: FootnoteOptions fast egendom. Anger fotnoternas position.
type: docs
weight: 30
url: /sv/net/aspose.words.notes/footnoteoptions/position/
---
## FootnoteOptions.Position property

Anger fotnoternas position.

```csharp
public FootnotePosition Position { get; set; }
```

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

* enum [FootnotePosition](../../footnoteposition/)
* class [FootnoteOptions](../)
* namnutrymme [Aspose.Words.Notes](../../footnoteoptions/)
* hopsättning [Aspose.Words](../../../)


