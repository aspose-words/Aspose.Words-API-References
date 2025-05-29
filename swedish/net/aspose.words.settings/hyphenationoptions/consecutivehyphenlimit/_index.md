---
title: HyphenationOptions.ConsecutiveHyphenLimit
linktitle: ConsecutiveHyphenLimit
articleTitle: ConsecutiveHyphenLimit
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ConsecutiveHyphenLimit i HyphenationOptions. Kontrollera användningen av bindestreck i din text för förbättrad läsbarhet och formatering. Standardvärde, 0.
type: docs
weight: 30
url: /sv/net/aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/
---
## HyphenationOptions.ConsecutiveHyphenLimit property

Hämtar eller anger det maximala antalet på varandra följande rader som kan sluta med bindestreck. Standardvärdet för den här egenskapen är 0.

```csharp
public int ConsecutiveHyphenLimit { get; set; }
```

## Anmärkningar

Om värdet för den här egenskapen är satt till 0 kan valfritt antal rader i följd avslutas med bindestreck.

Egenskapen har ingen effekt när man sparar till fasta sidformat, t.ex. PDF.

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

* class [HyphenationOptions](../)
* namnutrymme [Aspose.Words.Settings](../../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../../)
