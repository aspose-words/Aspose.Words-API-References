---
title: ParagraphFormat.LineSpacing
linktitle: LineSpacing
articleTitle: LineSpacing
second_title: Aspose.Words för .NET
description: Justera radavståndet i dina stycken enkelt med egenskapen ParagraphFormat LineSpacing. Förbättra läsbarheten och stilen i dina dokument!
type: docs
weight: 190
url: /sv/net/aspose.words/paragraphformat/linespacing/
---
## ParagraphFormat.LineSpacing property

Hämtar eller ställer in radavståndet (i punkter) för stycket.

```csharp
public double LineSpacing { get; set; }
```

## Anmärkningar

När[`LineSpacingRule`](../linespacingrule/) egendomen är inställd påAtLeast , radavståndet kan vara större än eller lika med men aldrig mindre än det angivna`LineSpacing` värde.

När[`LineSpacingRule`](../linespacingrule/) egendomen är inställd påExactly , radavståndet ändras aldrig från det angivna`LineSpacing` värde, även om ett större teckensnitt används i stycket.

## Exempel

Visar hur man arbetar med radavstånd.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan följer tre radavståndsregler som vi kan definiera med hjälp av
// styckets "LineSpacingRule"-egenskap för att konfigurera avståndet mellan stycken.
// 1 - Ange ett minsta avstånd.
// Detta ger vertikal utfyllnad till textrader av valfri storlek
// som är för liten för att bibehålla den minsta radhöjden.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.AtLeast;
builder.ParagraphFormat.LineSpacing = 20;

builder.Writeln("Minimum line spacing of 20.");
builder.Writeln("Minimum line spacing of 20.");

// 2 - Ange exakt avstånd.
// Om du använder för stora teckenstorlekar för avståndet kommer texten att avkortas.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Exactly;
builder.ParagraphFormat.LineSpacing = 5;

builder.Writeln("Line spacing of exactly 5.");
builder.Writeln("Line spacing of exactly 5.");

// 3 - Ange radavståndet som en multipel av standardradavståndet, vilket är 12 punkter som standard.
// Den här typen av avstånd skalas till olika teckenstorlekar.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Multiple;
builder.ParagraphFormat.LineSpacing = 18;

builder.Writeln("Line spacing of 1.5 default lines.");
builder.Writeln("Line spacing of 1.5 default lines.");

doc.Save(ArtifactsDir + "ParagraphFormat.LineSpacing.docx");
```

### Se även

* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
