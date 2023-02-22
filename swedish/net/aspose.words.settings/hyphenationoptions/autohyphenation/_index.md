---
title: HyphenationOptions.AutoHyphenation
second_title: Aspose.Words för .NET API Referens
description: HyphenationOptions fast egendom. Hämtar eller ställer in värde som avgör om automatisk avstavning är aktiverad för dokumentet. Standardvärdet för den här egenskapen är falsk .
type: docs
weight: 20
url: /sv/net/aspose.words.settings/hyphenationoptions/autohyphenation/
---
## HyphenationOptions.AutoHyphenation property

Hämtar eller ställer in värde som avgör om automatisk avstavning är aktiverad för dokumentet. Standardvärdet för den här egenskapen är **falsk** .

```csharp
public bool AutoHyphenation { get; set; }
```

### Exempel

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

* class [HyphenationOptions](../)
* namnutrymme [Aspose.Words.Settings](../../hyphenationoptions/)
* hopsättning [Aspose.Words](../../../)


