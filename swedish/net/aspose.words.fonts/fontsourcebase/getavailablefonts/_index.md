---
title: FontSourceBase.GetAvailableFonts
linktitle: GetAvailableFonts
articleTitle: GetAvailableFonts
second_title: Aspose.Words för .NET
description: FontSourceBase GetAvailableFonts metod. Returnerar en lista över teckensnitt som är tillgängliga via den här källan i C#.
type: docs
weight: 40
url: /sv/net/aspose.words.fonts/fontsourcebase/getavailablefonts/
---
## FontSourceBase.GetAvailableFonts method

Returnerar en lista över teckensnitt som är tillgängliga via den här källan.

```csharp
public IList<PhysicalFontInfo> GetAvailableFonts()
```

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

* class [PhysicalFontInfo](../../physicalfontinfo/)
* class [FontSourceBase](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
