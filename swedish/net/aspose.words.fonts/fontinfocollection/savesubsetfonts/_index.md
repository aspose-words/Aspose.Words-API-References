---
title: FontInfoCollection.SaveSubsetFonts
linktitle: SaveSubsetFonts
articleTitle: SaveSubsetFonts
second_title: Aspose.Words för .NET
description: Upptäck egenskapen SaveSubsetFonts i FontInfoCollection och kontrollera inbäddade TrueType-teckensnittsdelmängder i dina dokument för optimerad filstorlek och prestanda.
type: docs
weight: 50
url: /sv/net/aspose.words.fonts/fontinfocollection/savesubsetfonts/
---
## FontInfoCollection.SaveSubsetFonts property

Anger om en delmängd av de inbäddade TrueType-teckensnitten ska sparas med dokumentet. Standardvärdet för den här egenskapen är`falsk`.

Det här alternativet fungerar endast när[`EmbedTrueTypeFonts`](../embedtruetypefonts/) egendomen är inställd på`sann`.

```csharp
public bool SaveSubsetFonts { get; set; }
```

## Anmärkningar

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
