---
title: PhysicalFontInfo.FullFontName
linktitle: FullFontName
second_title: Aspose.Words for .NET API Reference
description: PhysicalFontInfo property. Full name of the font in C#.
type: docs
weight: 30
url: /net/aspose.words.fonts/physicalfontinfo/fullfontname/
---
## PhysicalFontInfo.FullFontName property

Full name of the font.

```csharp
public string FullFontName { get; }
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

* class [PhysicalFontInfo](../)
* namespace [Aspose.Words.Fonts](../../physicalfontinfo/)
* assembly [Aspose.Words](../../../)
