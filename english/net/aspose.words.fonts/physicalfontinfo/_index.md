---
title: PhysicalFontInfo Class
linktitle: PhysicalFontInfo
articleTitle: PhysicalFontInfo
second_title: Aspose.Words for .NET
description: Aspose.Words.Fonts.PhysicalFontInfo class. Specifies information about physical font available to Aspose.Words font engine in C#.
type: docs
weight: 3400
url: /net/aspose.words.fonts/physicalfontinfo/
---
## PhysicalFontInfo class

Specifies information about physical font available to Aspose.Words font engine.

To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/net/working-with-fonts/) documentation article.

```csharp
public class PhysicalFontInfo
```

## Properties

| Name | Description |
| --- | --- |
| [EmbeddingLicensingRights](../../aspose.words.fonts/physicalfontinfo/embeddinglicensingrights/) { get; } | Embedding licensing rights for the font. |
| [FilePath](../../aspose.words.fonts/physicalfontinfo/filepath/) { get; } | Path to the font file if any. |
| [FontFamilyName](../../aspose.words.fonts/physicalfontinfo/fontfamilyname/) { get; } | Family name of the font. |
| [FullFontName](../../aspose.words.fonts/physicalfontinfo/fullfontname/) { get; } | Full name of the font. |
| [Version](../../aspose.words.fonts/physicalfontinfo/version/) { get; } | Version string of the font. |

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

* namespace [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assembly [Aspose.Words](../../)
