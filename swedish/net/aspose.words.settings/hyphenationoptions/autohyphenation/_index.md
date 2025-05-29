---
title: HyphenationOptions.AutoHyphenation
linktitle: AutoHyphenation
articleTitle: AutoHyphenation
second_title: Aspose.Words för .NET
description: Styr automatisk avstavning med egenskapen HyphenationOptions. Förbättra enkelt dokumentets läsbarhet genom att aktivera eller inaktivera den här funktionen.
type: docs
weight: 20
url: /sv/net/aspose.words.settings/hyphenationoptions/autohyphenation/
---
## HyphenationOptions.AutoHyphenation property

Hämtar eller anger värde som avgör om automatisk bindestreck är aktiverat för dokumentet. Standardvärde för den här egenskapen är`falsk` .

```csharp
public bool AutoHyphenation { get; set; }
```

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
