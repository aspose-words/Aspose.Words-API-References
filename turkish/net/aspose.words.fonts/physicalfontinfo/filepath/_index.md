---
title: FilePath
second_title: Aspose.Words for .NET API Referansı
description: Varsa yazı tipi dosyasının yolu.
type: docs
weight: 10
url: /tr/net/aspose.words.fonts/physicalfontinfo/filepath/
---
## PhysicalFontInfo.FilePath property

Varsa yazı tipi dosyasının yolu.

```csharp
public string FilePath { get; }
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

* class [PhysicalFontInfo](../../physicalfontinfo)
* ad alanı [Aspose.Words.Fonts](../../physicalfontinfo)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->