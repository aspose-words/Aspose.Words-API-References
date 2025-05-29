---
title: HyphenationOptions Class
linktitle: HyphenationOptions
articleTitle: HyphenationOptions
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Settings.HyphenationOptions för att enkelt anpassa bindestrecksinställningar för dina dokument och förbättra textpresentationen.
type: docs
weight: 6620
url: /sv/net/aspose.words.settings/hyphenationoptions/
---
## HyphenationOptions class

Gör det möjligt att konfigurera alternativ för bindestreck i dokument.

För att lära dig mer, besök[Arbeta med bindestreck](https://docs.aspose.com/words/net/working-with-hyphenation/) dokumentationsartikel.

```csharp
public class HyphenationOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [HyphenationOptions](hyphenationoptions/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AutoHyphenation](../../aspose.words.settings/hyphenationoptions/autohyphenation/) { get; set; } | Hämtar eller anger värde som avgör om automatisk bindestreck är aktiverat för dokumentet. Standardvärde för den här egenskapen är`falsk` . |
| [ConsecutiveHyphenLimit](../../aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/) { get; set; } | Hämtar eller anger det maximala antalet på varandra följande rader som kan sluta med bindestreck. Standardvärdet för den här egenskapen är 0. |
| [HyphenateCaps](../../aspose.words.settings/hyphenationoptions/hyphenatecaps/) { get; set; } | Hämtar eller anger värde som avgör om ord skrivna med enbart versaler ska vara avstängda. Standardvärdet för den här egenskapen är`sann` . |
| [HyphenationZone](../../aspose.words.settings/hyphenationoptions/hyphenationzone/) { get; set; } | Hämtar eller ställer in avståndet i 1/20 av en punkt från högermarginalen inom vilket du inte vill att ord ska bindestreckas. Standardvärdet för den här egenskapen är 360 (0,25 tum). |

## Exempel

Visar hur man konfigurerar automatisk bindestreck.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.HyphenationOptions.AutoHyphenation = true;
doc.HyphenationOptions.ConsecutiveHyphenLimit = 2;
doc.HyphenationOptions.HyphenationZone = 720;
doc.HyphenationOptions.HyphenateCaps = true;

doc.Save(ArtifactsDir + "Document.HyphenationOptions.docx");
```

### Se även

* namnutrymme [Aspose.Words.Settings](../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../)
