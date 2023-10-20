---
title: HyphenationOptions Class
linktitle: HyphenationOptions
articleTitle: HyphenationOptions
second_title: Aspose.Words för .NET
description: Aspose.Words.Settings.HyphenationOptions klass. Gör det möjligt att konfigurera alternativ för dokumentavstavning i C#.
type: docs
weight: 5790
url: /sv/net/aspose.words.settings/hyphenationoptions/
---
## HyphenationOptions class

Gör det möjligt att konfigurera alternativ för dokumentavstavning.

För att lära dig mer, besök[Arbeta med avstavning](https://docs.aspose.com/words/net/working-with-hyphenation/) dokumentationsartikel.

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
| [AutoHyphenation](../../aspose.words.settings/hyphenationoptions/autohyphenation/) { get; set; } | Hämtar eller ställer in värde som avgör om automatisk avstavning är aktiverad för dokumentet. Standardvärdet för den här egenskapen är`falsk` . |
| [ConsecutiveHyphenLimit](../../aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/) { get; set; } | Hämtar eller ställer in det maximala antalet rader i följd som kan sluta med bindestreck. Standardvärdet för den här egenskapen är 0. |
| [HyphenateCaps](../../aspose.words.settings/hyphenationoptions/hyphenatecaps/) { get; set; } | Hämtar eller ställer in ett värde som avgör om ord skrivna med stora bokstäver är avstavade. Standardvärdet för den här egenskapen är`Sann` . |
| [HyphenationZone](../../aspose.words.settings/hyphenationoptions/hyphenationzone/) { get; set; } | Hämtar eller ställer in avståndet i 1/20 av en punkt från högermarginalen inom vilken du inte vill att ska avstava ord. Standardvärdet för den här egenskapen är 360 (0,25 tum). |

## Exempel

Visar hur du konfigurerar automatisk avstavning.

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
