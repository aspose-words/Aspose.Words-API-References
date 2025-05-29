---
title: FontInfoCollection Class
linktitle: FontInfoCollection
articleTitle: FontInfoCollection
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fonts.FontInfoCollection, din lösning för att hantera dokumentteckensnitt effektivt och förbättra dokumentets visuella attraktionskraft.
type: docs
weight: 3360
url: /sv/net/aspose.words.fonts/fontinfocollection/
---
## FontInfoCollection class

Representerar en samling teckensnitt som används i ett dokument.

För att lära dig mer, besök[Arbeta med teckensnitt](https://docs.aspose.com/words/net/working-with-fonts/) dokumentationsartikel.

```csharp
public class FontInfoCollection : IEnumerable<FontInfo>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.fonts/fontinfocollection/count/) { get; } | Hämtar antalet element som finns i samlingen. |
| [EmbedSystemFonts](../../aspose.words.fonts/fontinfocollection/embedsystemfonts/) { get; set; } | Anger om systemteckensnitt ska bäddas in i dokumentet eller inte. Standardvärdet för den här egenskapen är`falsk`. |
| [EmbedTrueTypeFonts](../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) { get; set; } | Anger om TrueType-teckensnitt ska bäddas in i ett dokument när det sparas. Standardvärdet för den här egenskapen är`falsk` . |
| [Item](../../aspose.words.fonts/fontinfocollection/item/) { get; } | Hämtar ett teckensnitt med det angivna namnet. (2 indexers) |
| [SaveSubsetFonts](../../aspose.words.fonts/fontinfocollection/savesubsetfonts/) { get; set; } | Anger om en delmängd av de inbäddade TrueType-teckensnitten ska sparas med dokumentet. Standardvärdet för den här egenskapen är`falsk`. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Contains](../../aspose.words.fonts/fontinfocollection/contains/)(*string*) | Avgör om samlingen innehåller ett teckensnitt med det angivna namnet. |
| [GetEnumerator](../../aspose.words.fonts/fontinfocollection/getenumerator/)() | Returnerar ett uppräknarobjekt som kan användas för att iterera över alla objekt i samlingen. |

## Anmärkningar

Föremålen är[`FontInfo`](../fontinfo/) föremål.

Du skapar inte instanser av den här klassen direkt. Använd[`FontInfos`](../../aspose.words/documentbase/fontinfos/) egenskapen för att komma åt samlingen av teckensnitt som definieras i dokumentet.

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

* class [FontInfo](../fontinfo/)
* namnutrymme [Aspose.Words.Fonts](../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../)
