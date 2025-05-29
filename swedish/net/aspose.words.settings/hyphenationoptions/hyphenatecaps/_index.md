---
title: HyphenationOptions.HyphenateCaps
linktitle: HyphenateCaps
articleTitle: HyphenateCaps
second_title: Aspose.Words för .NET
description: Upptäck egenskapen HyphenateCaps i HyphenationOptions. Kontrollera enkelt avstavning för ord med versaler – standardinställningen är sant. Optimera din text idag!
type: docs
weight: 40
url: /sv/net/aspose.words.settings/hyphenationoptions/hyphenatecaps/
---
## HyphenationOptions.HyphenateCaps property

Hämtar eller anger värde som avgör om ord skrivna med enbart versaler ska vara avstängda. Standardvärdet för den här egenskapen är`sann` .

```csharp
public bool HyphenateCaps { get; set; }
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
