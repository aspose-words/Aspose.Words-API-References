---
title: DocumentBase.FontInfos
linktitle: FontInfos
articleTitle: FontInfos
second_title: Aspose.Words för .NET
description: DocumentBase FontInfos fast egendom. Ger tillgång till egenskaperna för teckensnitt som används i detta dokument i C#.
type: docs
weight: 30
url: /sv/net/aspose.words/documentbase/fontinfos/
---
## DocumentBase.FontInfos property

Ger tillgång till egenskaperna för teckensnitt som används i detta dokument.

```csharp
public FontInfoCollection FontInfos { get; }
```

## Anmärkningar

Denna samling teckensnittsdefinitioner laddas som den är från dokumentet. Teckensnittsdefinitioner kan vara valfria, saknas eller ofullständiga i vissa dokument.

Lita inte på den här samlingen för att försäkra dig om att ett visst teckensnitt används i dokumentet. Du bör endast använda den här samlingen för att få information om teckensnitt som kan användas i dokumentet.

## Exempel

Visar hur man skriver ut information om vilka typsnitt som finns i ett dokument.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Skriv ut alla använda och oanvända typsnitt i dokumentet.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

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

* class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* class [DocumentBase](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
