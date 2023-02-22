---
title: PhysicalFontInfo.FontFamilyName
second_title: Aspose.Words för .NET API Referens
description: PhysicalFontInfo fast egendom. Teckensnittets efternamn.
type: docs
weight: 20
url: /sv/net/aspose.words.fonts/physicalfontinfo/fontfamilyname/
---
## PhysicalFontInfo.FontFamilyName property

Teckensnittets efternamn.

```csharp
public string FontFamilyName { get; }
```

### Exempel

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

* class [PhysicalFontInfo](../)
* namnutrymme [Aspose.Words.Fonts](../../physicalfontinfo/)
* hopsättning [Aspose.Words](../../../)


