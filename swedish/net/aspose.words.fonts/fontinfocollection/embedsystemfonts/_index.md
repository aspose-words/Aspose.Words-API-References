---
title: FontInfoCollection.EmbedSystemFonts
linktitle: EmbedSystemFonts
articleTitle: EmbedSystemFonts
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen FontInfoCollection EmbedSystemFonts förbättrar dina dokument genom att bädda in systemteckensnitt. Lär dig dess standardvärde och fördelar!
type: docs
weight: 20
url: /sv/net/aspose.words.fonts/fontinfocollection/embedsystemfonts/
---
## FontInfoCollection.EmbedSystemFonts property

Anger om systemteckensnitt ska bäddas in i dokumentet eller inte. Standardvärdet för den här egenskapen är`falsk`.

Det här alternativet fungerar endast när[`EmbedTrueTypeFonts`](../embedtruetypefonts/) alternativet är inställt på`sann`.

```csharp
public bool EmbedSystemFonts { get; set; }
```

## Anmärkningar

Ställer in den här egenskapen på`sann` är användbart om användaren använder ett östasiatiskt system och vill skapa ett dokument som är läsbart för andra som inte har teckensnitt för det språket på sitt system. Till exempel kan en användare på ett japanskt system välja att bädda in teckensnitten i ett dokument så att det japanska dokumentet blir läsbart på alla system.

Det här alternativet fungerar endast för DOC-, DOCX- och RTF-format.

## Exempel

Visar hur man sparar ett dokument med inbäddade TrueType-teckensnitt.

```csharp
Document doc = new Document(MyDir + "Document.docx");

FontInfoCollection fontInfos = doc.FontInfos;
fontInfos.EmbedTrueTypeFonts = embedAllFonts;
fontInfos.EmbedSystemFonts = embedAllFonts;
fontInfos.SaveSubsetFonts = embedAllFonts;

doc.Save(ArtifactsDir + "Font.FontInfoCollection.docx");
```

### Se även

* class [FontInfoCollection](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
