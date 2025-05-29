---
title: PhysicalFontInfo.Version
linktitle: Version
articleTitle: Version
second_title: .NET için Aspose.Words
description: PhysicalFontInfo Sürüm özelliğini keşfedin, gelişmiş tasarım tutarlılığı ve iyileştirilmiş tipografi için yazı tipinin sürüm dizesine kolayca erişin.
type: docs
weight: 50
url: /tr/net/aspose.words.fonts/physicalfontinfo/version/
---
## PhysicalFontInfo.Version property

Yazı tipinin sürüm dizesi.

```csharp
public string Version { get; }
```

## Örnekler

Mevcut yazı tiplerinin nasıl listeleneceğini gösterir.

```csharp
// Aspose.Words'ü yazı tiplerini özel bir klasörden kaynaklayacak şekilde yapılandırın ve ardından kullanılabilir tüm yazı tiplerini yazdırın.
FontSourceBase[] folderFontSource = { new FolderFontSource(FontsDir, true) };

foreach (PhysicalFontInfo fontInfo in folderFontSource[0].GetAvailableFonts())
{
    Console.WriteLine("FontFamilyName : {0}", fontInfo.FontFamilyName);
    Console.WriteLine("FullFontName  : {0}", fontInfo.FullFontName);
    Console.WriteLine("Version  : {0}", fontInfo.Version);
    Console.WriteLine("FilePath : {0}\n", fontInfo.FilePath);
}
```

### Ayrıca bakınız

* class [PhysicalFontInfo](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
