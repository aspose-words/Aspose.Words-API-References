---
title: FontInfoCollection.EmbedSystemFonts
second_title: Aspose.Words för .NET API Referens
description: FontInfoCollection fast egendom. Anger om systemteckensnitt ska bäddas in i dokumentet eller inte. Standardvärdet för den här egenskapen är falsk.
type: docs
weight: 20
url: /sv/net/aspose.words.fonts/fontinfocollection/embedsystemfonts/
---
## FontInfoCollection.EmbedSystemFonts property

Anger om systemteckensnitt ska bäddas in i dokumentet eller inte. Standardvärdet för den här egenskapen är **falsk**.

Det här alternativet fungerar endast när[`EmbedTrueTypeFonts`](../embedtruetypefonts/) alternativet är inställt på **Sann**.

```csharp
public bool EmbedSystemFonts { get; set; }
```

### Anmärkningar

Ställer in den här egenskapen till`Sann`är användbart om användaren är på ett östasiatiskt system och vill skapa ett dokument som är läsbart för andra som inte har teckensnitt för that -språket på sitt system. En användare på ett japanskt system kan till exempel välja att bädda in teckensnitten i ett dokument så att det japanska dokumentet är läsbart på alla system.

Det här alternativet fungerar endast för DOC-, DOCX- och RTF-format.

### Exempel

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
* namnutrymme [Aspose.Words.Fonts](../../fontinfocollection/)
* hopsättning [Aspose.Words](../../../)


