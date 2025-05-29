---
title: FontInfoCollection.EmbedTrueTypeFonts
linktitle: EmbedTrueTypeFonts
articleTitle: EmbedTrueTypeFonts
second_title: Aspose.Words för .NET
description: Lär dig hur egenskapen EmbedTrueTypeFonts i FontInfoCollection förbättrar dokumentkvaliteten genom att tillåta inbäddning av TrueType-teckensnitt. Standardvärdet är falskt.
type: docs
weight: 30
url: /sv/net/aspose.words.fonts/fontinfocollection/embedtruetypefonts/
---
## FontInfoCollection.EmbedTrueTypeFonts property

Anger om TrueType-teckensnitt ska bäddas in i ett dokument när det sparas. Standardvärdet för den här egenskapen är`falsk` .

```csharp
public bool EmbedTrueTypeFonts { get; set; }
```

## Anmärkningar

Genom att bädda in TrueType-teckensnitt kan andra visa dokumentet med samma teckensnitt som användes för att skapa det, men det kan öka dokumentstorleken avsevärt.

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
