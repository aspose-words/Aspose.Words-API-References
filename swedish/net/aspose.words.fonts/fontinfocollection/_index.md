---
title: Class FontInfoCollection
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Fonts.FontInfoCollection klass. Representerar en samling teckensnitt som används i ett dokument.
type: docs
weight: 2930
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
| [EmbedTrueTypeFonts](../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) { get; set; } | Anger om TrueType-teckensnitt ska bäddas in i ett dokument eller inte när det sparas. Standardvärdet för den här egenskapen är`falsk` . |
| [Item](../../aspose.words.fonts/fontinfocollection/item/) { get; } | Får ett teckensnitt med det angivna namnet. (2 indexers) |
| [SaveSubsetFonts](../../aspose.words.fonts/fontinfocollection/savesubsetfonts/) { get; set; } | Anger om en delmängd av de inbäddade TrueType-teckensnitten ska sparas eller inte med dokumentet. Standardvärdet för den här egenskapen är`falsk`. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Contains](../../aspose.words.fonts/fontinfocollection/contains/)(string) | Bestämmer om samlingen innehåller ett teckensnitt med det angivna namnet. |
| [GetEnumerator](../../aspose.words.fonts/fontinfocollection/getenumerator/)() | Returnerar ett uppräkningsobjekt som kan användas för att iterera över alla objekt i samlingen. |

### Anmärkningar

Objekt är[`FontInfo`](../fontinfo/) föremål.

Du skapar inte instanser av den här klassen direkt. Använd[`FontInfos`](../../aspose.words/documentbase/fontinfos/) egenskap för att komma åt samlingen av teckensnitt som definieras i dokumentet.

### Exempel

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

* class [FontInfo](../fontinfo/)
* namnutrymme [Aspose.Words.Fonts](../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../)


