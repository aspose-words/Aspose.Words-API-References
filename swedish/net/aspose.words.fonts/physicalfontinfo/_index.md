---
title: PhysicalFontInfo Class
linktitle: PhysicalFontInfo
articleTitle: PhysicalFontInfo
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fonts.PhysicalFontInfo, som ger viktig information om fysiska teckensnitt för förbättrad dokumentbehandling och design.
type: docs
weight: 3460
url: /sv/net/aspose.words.fonts/physicalfontinfo/
---
## PhysicalFontInfo class

Anger information om fysiskt teckensnitt som är tillgängligt för Aspose.Words teckensnittsmotor.

För att lära dig mer, besök[Arbeta med teckensnitt](https://docs.aspose.com/words/net/working-with-fonts/) dokumentationsartikel.

```csharp
public class PhysicalFontInfo
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [EmbeddingLicensingRights](../../aspose.words.fonts/physicalfontinfo/embeddinglicensingrights/) { get; } | Bäddar in licensrättigheter för teckensnittet. |
| [FilePath](../../aspose.words.fonts/physicalfontinfo/filepath/) { get; } | Sökväg till typsnittsfilen om sådan finns. |
| [FontFamilyName](../../aspose.words.fonts/physicalfontinfo/fontfamilyname/) { get; } | Typsnittets efternamn. |
| [FullFontName](../../aspose.words.fonts/physicalfontinfo/fullfontname/) { get; } | Typsnittets fullständiga namn. |
| [Version](../../aspose.words.fonts/physicalfontinfo/version/) { get; } | Versionssträng för teckensnittet. |

## Exempel

Visar hur man listar tillgängliga teckensnitt.

```csharp
// Konfigurera Aspose.Words för att hämta teckensnitt från en anpassad mapp och sedan skriva ut alla tillgängliga teckensnitt.
FontSourceBase[] folderFontSource = { new FolderFontSource(FontsDir, true) };

foreach (PhysicalFontInfo fontInfo in folderFontSource[0].GetAvailableFonts())
{
    Console.WriteLine("FontFamilyName : {0}", fontInfo.FontFamilyName);
    Console.WriteLine("FullFontName  : {0}", fontInfo.FullFontName);
    Console.WriteLine("Version  : {0}", fontInfo.Version);
    Console.WriteLine("FilePath : {0}\n", fontInfo.FilePath);
}
```

### Se även

* namnutrymme [Aspose.Words.Fonts](../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../)
