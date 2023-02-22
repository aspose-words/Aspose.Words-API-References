---
title: FontSourceBase.GetAvailableFonts
second_title: Aspose.Words for .NET API Referansı
description: FontSourceBase yöntem. Bu kaynak aracılığıyla kullanılabilen yazı tiplerinin listesini döndürür.
type: docs
weight: 40
url: /tr/net/aspose.words.fonts/fontsourcebase/getavailablefonts/
---
## FontSourceBase.GetAvailableFonts method

Bu kaynak aracılığıyla kullanılabilen yazı tiplerinin listesini döndürür.

```csharp
public IList<PhysicalFontInfo> GetAvailableFonts()
```

### Örnekler

Kullanılabilir yazı tiplerinin nasıl listeleneceğini gösterir.

```csharp
// Aspose.Words'ü fontları özel bir klasörden kaynaklayacak şekilde yapılandırın ve ardından mevcut her fontu yazdırın.
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

* class [PhysicalFontInfo](../../physicalfontinfo/)
* class [FontSourceBase](../)
* ad alanı [Aspose.Words.Fonts](../../fontsourcebase/)
* toplantı [Aspose.Words](../../../)


