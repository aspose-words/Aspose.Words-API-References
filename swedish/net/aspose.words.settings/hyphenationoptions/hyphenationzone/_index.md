---
title: HyphenationOptions.HyphenationZone
linktitle: HyphenationZone
articleTitle: HyphenationZone
second_title: Aspose.Words för .NET
description: Optimera textlayouten med egenskapen HyphenationZone. Kontrollera avståndet mellan bindestreck och högermarginalen för renare, professionella dokument.
type: docs
weight: 50
url: /sv/net/aspose.words.settings/hyphenationoptions/hyphenationzone/
---
## HyphenationOptions.HyphenationZone property

Hämtar eller ställer in avståndet i 1/20 av en punkt från högermarginalen inom vilket du inte vill att ord ska bindestreckas. Standardvärdet för den här egenskapen är 360 (0,25 tum).

```csharp
public int HyphenationZone { get; set; }
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
