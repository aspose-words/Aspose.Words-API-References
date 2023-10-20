---
title: PhysicalFontInfo Class
linktitle: PhysicalFontInfo
articleTitle: PhysicalFontInfo
second_title: Aspose.Words för .NET
description: Aspose.Words.Fonts.PhysicalFontInfo klass. Anger information om fysiska teckensnitt som är tillgängliga för Aspose.Words teckensnittsmotor i C#.
type: docs
weight: 3030
url: /sv/net/aspose.words.fonts/physicalfontinfo/
---
## PhysicalFontInfo class

Anger information om fysiska teckensnitt som är tillgängliga för Aspose.Words teckensnittsmotor.

För att lära dig mer, besök[Arbeta med teckensnitt](https://docs.aspose.com/words/net/working-with-fonts/) dokumentationsartikel.

```csharp
public class PhysicalFontInfo
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [FilePath](../../aspose.words.fonts/physicalfontinfo/filepath/) { get; } | Sökväg till teckensnittsfilen om någon. |
| [FontFamilyName](../../aspose.words.fonts/physicalfontinfo/fontfamilyname/) { get; } | Teckensnittets efternamn. |
| [FullFontName](../../aspose.words.fonts/physicalfontinfo/fullfontname/) { get; } | Teckensnittets fullständiga namn. |
| [Version](../../aspose.words.fonts/physicalfontinfo/version/) { get; } | Teckensnittets versionssträng. |

## Exempel

Visar hur man listar tillgängliga teckensnitt.

```csharp
// Konfigurera Aspose.Words för att hämta teckensnitt från en anpassad mapp och skriv sedan ut alla tillgängliga teckensnitt.
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
