---
title: DocumentBase.FontInfos
linktitle: FontInfos
articleTitle: FontInfos
second_title: Aspose.Words för .NET
description: Få tillgång till detaljerade teckensnittsegenskaper med DocumentBases FontInfos-funktion, vilket enkelt förbättrar ditt dokuments design och läsbarhet.
type: docs
weight: 30
url: /sv/net/aspose.words/documentbase/fontinfos/
---
## DocumentBase.FontInfos property

Ger åtkomst till egenskaper för teckensnitt som används i detta dokument.

```csharp
public FontInfoCollection FontInfos { get; }
```

## Anmärkningar

Denna samling av teckensnittsdefinitioner laddas som de är från dokumentet. Teckensnittsdefinitioner kan vara valfria, saknas eller vara ofullständiga i vissa dokument.

Lita inte på den här samlingen för att fastställa att ett visst teckensnitt används i dokumentet. Du bör endast använda den här samlingen för att få information om teckensnitt som kan användas i dokumentet.

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

Visar hur man skriver ut information om vilka teckensnitt som finns i ett dokument.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Skriv ut alla använda och oanvända teckensnitt i dokumentet.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

### Se även

* class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* class [DocumentBase](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
