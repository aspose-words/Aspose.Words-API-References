---
title: Class FontInfo
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Fonts.FontInfo klass. Anger information om ett teckensnitt som används i dokumentet.
type: docs
weight: 2920
url: /sv/net/aspose.words.fonts/fontinfo/
---
## FontInfo class

Anger information om ett teckensnitt som används i dokumentet.

För att lära dig mer, besök[Arbeta med teckensnitt](https://docs.aspose.com/words/net/working-with-fonts/) dokumentationsartikel.

```csharp
public class FontInfo
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AltName](../../aspose.words.fonts/fontinfo/altname/) { get; set; } | Hämtar eller ställer in det alternativa namnet för teckensnittet. |
| [Charset](../../aspose.words.fonts/fontinfo/charset/) { get; set; } | Hämtar eller ställer in teckenuppsättningen för teckensnittet. |
| [Family](../../aspose.words.fonts/fontinfo/family/) { get; set; } | Hämtar eller ställer in teckensnittsfamiljen som detta teckensnitt tillhör. |
| [IsTrueType](../../aspose.words.fonts/fontinfo/istruetype/) { get; set; } | Indikerar att detta teckensnitt är ett TrueType- eller OpenType-teckensnitt i motsats till ett raster- eller vektorteckensnitt. Standard är`Sann` . |
| [Name](../../aspose.words.fonts/fontinfo/name/) { get; } | Hämtar namnet på teckensnittet. |
| [Panose](../../aspose.words.fonts/fontinfo/panose/) { get; set; } | Hämtar eller ställer in PANOSE-typsnittsklassificeringsnumret. |
| [Pitch](../../aspose.words.fonts/fontinfo/pitch/) { get; set; } | Tonhöjden indikerar om teckensnittet har fast tonhöjd, proportionellt fördelat eller är beroende av en standardinställning. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetEmbeddedFont](../../aspose.words.fonts/fontinfo/getembeddedfont/)(EmbeddedFontFormat, EmbeddedFontStyle) | Får en specifik inbäddad teckensnittsfil. |
| [GetEmbeddedFontAsOpenType](../../aspose.words.fonts/fontinfo/getembeddedfontasopentype/)(EmbeddedFontStyle) | Hämtar en inbäddad teckensnittsfil i OpenType-format. Teckensnitt i Embedded OpenType-format konverteras till OpenType. |

### Anmärkningar

Du skapar inte instanser av den här klassen direkt. Använd[`FontInfos`](../../aspose.words/documentbase/fontinfos/) egenskap för att komma åt samlingen av teckensnitt definierade i ett dokument.

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

### Se även

* namnutrymme [Aspose.Words.Fonts](../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../)


