---
title: FontInfo Class
linktitle: FontInfo
articleTitle: FontInfo
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fonts.FontInfo, din nyckel till detaljerade teckensnittsinsikter för dokument, vilket förbättrar textkvaliteten och det visuella intrycket.
type: docs
weight: 3350
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
| [AltName](../../aspose.words.fonts/fontinfo/altname/) { get; set; } | Hämtar eller anger det alternativa namnet för teckensnittet. |
| [Charset](../../aspose.words.fonts/fontinfo/charset/) { get; set; } | Hämtar eller anger teckenuppsättningen för typsnittet. |
| [EmbeddingLicensingRights](../../aspose.words.fonts/fontinfo/embeddinglicensingrights/) { get; } | Hämtar licensrättigheterna för inbäddade teckensnitt. |
| [Family](../../aspose.words.fonts/fontinfo/family/) { get; set; } | Hämtar eller anger vilken typsnittsfamilj detta typsnitt tillhör. |
| [IsTrueType](../../aspose.words.fonts/fontinfo/istruetype/) { get; set; } | Indikerar att det här teckensnittet är ett TrueType- eller OpenType-teckensnitt i motsats till ett raster- eller vektorteckensnitt. Standard är`sann` . |
| [Name](../../aspose.words.fonts/fontinfo/name/) { get; } | Hämtar namnet på teckensnittet. |
| [Panose](../../aspose.words.fonts/fontinfo/panose/) { get; set; } | Hämtar eller ställer in PANOSE-typsnittsklassificeringsnumret. |
| [Pitch](../../aspose.words.fonts/fontinfo/pitch/) { get; set; } | Bredvidden anger om teckensnittet har fast bredd, är proportionellt fördelat eller använder en standardinställning. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetEmbeddedFont](../../aspose.words.fonts/fontinfo/getembeddedfont/)(*[EmbeddedFontFormat](../embeddedfontformat/), [EmbeddedFontStyle](../embeddedfontstyle/)*) | Hämtar en specifik inbäddad teckensnittsfil. |
| [GetEmbeddedFontAsOpenType](../../aspose.words.fonts/fontinfo/getembeddedfontasopentype/)(*[EmbeddedFontStyle](../embeddedfontstyle/)*) | Hämtar en inbäddad typsnittsfil i OpenType-format. Typsnitt i inbäddat OpenType-format konverteras till OpenType. |

## Anmärkningar

Du skapar inte instanser av den här klassen direkt. Använd[`FontInfos`](../../aspose.words/documentbase/fontinfos/) egenskapen för att komma åt samlingen av fonts som definieras i ett dokument.

## Exempel

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

* namnutrymme [Aspose.Words.Fonts](../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../)
