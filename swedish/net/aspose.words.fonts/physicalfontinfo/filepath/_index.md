---
title: PhysicalFontInfo.FilePath
linktitle: FilePath
articleTitle: FilePath
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PhysicalFontInfo FilePath, hitta enkelt dina typsnittsfiler för sömlös designintegration och förbättrad typografi i dina projekt.
type: docs
weight: 20
url: /sv/net/aspose.words.fonts/physicalfontinfo/filepath/
---
## PhysicalFontInfo.FilePath property

Sökväg till typsnittsfilen om sådan finns.

```csharp
public string FilePath { get; }
```

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

* class [PhysicalFontInfo](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
