---
title: ParagraphFormat.LineSpacing
second_title: Aspose.Words för .NET API Referens
description: ParagraphFormat fast egendom. Hämtar eller ställer in radavståndet i punkter för stycket.
type: docs
weight: 180
url: /sv/net/aspose.words/paragraphformat/linespacing/
---
## ParagraphFormat.LineSpacing property

Hämtar eller ställer in radavståndet (i punkter) för stycket.

```csharp
public double LineSpacing { get; set; }
```

### Anmärkningar

När egenskapen LineSpacingRule är inställd på AtMinst, kan radavståndet vara större än eller lika med, men aldrig mindre än det angivna värdet för LineSpacing.

När LineSpacingRule-egenskapen är inställd på Exactly, ändras radavståndet aldrig from det angivna LineSpacing-värdet, även om ett större teckensnitt används i stycket.

### Exempel

Visar hur man arbetar med radavstånd.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan finns tre radavståndsregler som vi kan definiera med hjälp av
// styckets "LineSpacingRule"-egenskap för att konfigurera avståndet mellan stycken.
// 1 - Ställ in ett minsta avstånd.
// Detta kommer att ge vertikal utfyllnad till textrader av valfri storlek
// som är för liten för att bibehålla den lägsta linjehöjden.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.AtLeast;
builder.ParagraphFormat.LineSpacing = 20;

builder.Writeln("Minimum line spacing of 20.");
builder.Writeln("Minimum line spacing of 20.");

// 2 - Ställ in exakt avstånd.
// Om du använder teckenstorlekar som är för stora för avståndet kommer texten att trunkeras.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Exactly;
builder.ParagraphFormat.LineSpacing = 5;

builder.Writeln("Line spacing of exactly 5.");
builder.Writeln("Line spacing of exactly 5.");

// 3 - Ange avstånd som en multipel av standard radavstånd, vilket är 12 punkter som standard.
// Den här typen av mellanrum kommer att skalas till olika teckenstorlekar.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Multiple;
builder.ParagraphFormat.LineSpacing = 18;

builder.Writeln("Line spacing of 1.5 default lines.");
builder.Writeln("Line spacing of 1.5 default lines.");

doc.Save(ArtifactsDir + "ParagraphFormat.LineSpacing.docx");
```

### Se även

* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../paragraphformat/)
* hopsättning [Aspose.Words](../../../)


