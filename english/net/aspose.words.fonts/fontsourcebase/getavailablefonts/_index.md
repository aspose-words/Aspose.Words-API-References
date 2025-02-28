---
title: FontSourceBase.GetAvailableFonts
linktitle: GetAvailableFonts
articleTitle: GetAvailableFonts
second_title: Aspose.Words for .NET
description: Discover available fonts with FontSourceBase's GetAvailableFonts method. Enhance your projects with a diverse selection of high-quality typefaces!
type: docs
weight: 40
url: /net/aspose.words.fonts/fontsourcebase/getavailablefonts/
---
## FontSourceBase.GetAvailableFonts method

Returns list of fonts available via this source.

```csharp
public IList<PhysicalFontInfo> GetAvailableFonts()
```

## Examples

Shows how to list available fonts.

```csharp
// Configure Aspose.Words to source fonts from a custom folder, and then print every available font.
FontSourceBase[] folderFontSource = { new FolderFontSource(FontsDir, true) };

foreach (PhysicalFontInfo fontInfo in folderFontSource[0].GetAvailableFonts())
{
    Console.WriteLine("FontFamilyName : {0}", fontInfo.FontFamilyName);
    Console.WriteLine("FullFontName  : {0}", fontInfo.FullFontName);
    Console.WriteLine("Version  : {0}", fontInfo.Version);
    Console.WriteLine("FilePath : {0}\n", fontInfo.FilePath);
}
```

### See Also

* class [PhysicalFontInfo](../../physicalfontinfo/)
* class [FontSourceBase](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
