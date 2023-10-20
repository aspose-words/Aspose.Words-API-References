---
title: FontInfoCollection.EmbedTrueTypeFonts
linktitle: EmbedTrueTypeFonts
articleTitle: EmbedTrueTypeFonts
second_title: Aspose.Words för .NET
description: FontInfoCollection EmbedTrueTypeFonts fast egendom. Anger om TrueTypeteckensnitt ska bäddas in i ett dokument eller inte när det sparas. Standardvärdet för den här egenskapen ärfalsk  i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.fonts/fontinfocollection/embedtruetypefonts/
---
## FontInfoCollection.EmbedTrueTypeFonts property

Anger om TrueType-teckensnitt ska bäddas in i ett dokument eller inte när det sparas. Standardvärdet för den här egenskapen är`falsk` .

```csharp
public bool EmbedTrueTypeFonts { get; set; }
```

## Anmärkningar

Genom att bädda in TrueType-teckensnitt kan andra visa dokumentet med samma typsnitt som användes för att skapa det, men kan öka dokumentstorleken avsevärt.

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

if (embedAllFonts)
    Assert.That(25000, Is.LessThan(new FileInfo(ArtifactsDir + "Font.FontInfoCollection.docx").Length));
else
    Assert.That(15000, Is.AtLeast(new FileInfo(ArtifactsDir + "Font.FontInfoCollection.docx").Length));
```

### Se även

* class [FontInfoCollection](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
