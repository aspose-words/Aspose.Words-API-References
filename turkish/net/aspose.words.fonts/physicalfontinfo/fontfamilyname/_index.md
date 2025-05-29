---
title: PhysicalFontInfo.FontFamilyName
linktitle: FontFamilyName
articleTitle: FontFamilyName
second_title: .NET için Aspose.Words
description: Projelerinizde font ailelerini etkili bir şekilde tanımlamanın ve kullanmanın anahtarı olan PhysicalFontInfo FontFamilyName özelliğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.fonts/physicalfontinfo/fontfamilyname/
---
## PhysicalFontInfo.FontFamilyName property

Yazı tipinin aile adı.

```csharp
public string FontFamilyName { get; }
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
