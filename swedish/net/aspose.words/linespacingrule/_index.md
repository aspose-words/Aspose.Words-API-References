---
title: LineSpacingRule Enum
linktitle: LineSpacingRule
articleTitle: LineSpacingRule
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.LineSpacingRule-enum för anpassningsbart radavstånd i stycket. Förbättra dokumentformateringen med exakt kontroll och förbättrad läsbarhet.
type: docs
weight: 3890
url: /sv/net/aspose.words/linespacingrule/
---
## LineSpacingRule enumeration

Anger radavståndsvärden för ett stycke.

```csharp
public enum LineSpacingRule
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| AtLeast | `0` | Radavståndet kan vara större än eller lika med, men aldrig mindre än, det värde som anges i[`LineSpacing`](../paragraphformat/linespacing/) egendom. |
| Exactly | `1` | Radavståndet ändras aldrig från det värde som anges i [`LineSpacing`](../paragraphformat/linespacing/) egenskap, även om ett större teckensnitt används i stycket. |
| Multiple | `2` | Radavståndet anges i[`LineSpacing`](../paragraphformat/linespacing/) egenskapen som antalet rader. En rad motsvarar 12 punkter. |

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

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
