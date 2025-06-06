---
title: PhysicalFontInfo.FullFontName
linktitle: FullFontName
articleTitle: FullFontName
second_title: .NET için Aspose.Words
description: Yazı tipi adlarına kolay erişim için PhysicalFontInfo'nun FullFontName özelliğini keşfedin. Tipografinizi hassas yazı tipi tanımlamasıyla geliştirin!
type: docs
weight: 40
url: /tr/net/aspose.words.fonts/physicalfontinfo/fullfontname/
---
## PhysicalFontInfo.FullFontName property

Yazı tipinin tam adı.

```csharp
public string FullFontName { get; }
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
