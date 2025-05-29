---
title: PhysicalFontInfo Class
linktitle: PhysicalFontInfo
articleTitle: PhysicalFontInfo
second_title: .NET için Aspose.Words
description: Gelişmiş belge işleme ve tasarımı için fiziksel yazı tipleri hakkında temel ayrıntılar sağlayan Aspose.Words.Fonts.PhysicalFontInfo sınıfını keşfedin.
type: docs
weight: 3460
url: /tr/net/aspose.words.fonts/physicalfontinfo/
---
## PhysicalFontInfo class

Aspose.Words yazı tipi motorunda kullanılabilen fiziksel yazı tipi hakkında bilgi belirtir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yazı Tipleriyle Çalışma](https://docs.aspose.com/words/net/working-with-fonts/) belgeleme makalesi.

```csharp
public class PhysicalFontInfo
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [EmbeddingLicensingRights](../../aspose.words.fonts/physicalfontinfo/embeddinglicensingrights/) { get; } | Yazı tipi için lisanslama haklarının gömülmesi. |
| [FilePath](../../aspose.words.fonts/physicalfontinfo/filepath/) { get; } | Varsa yazı tipi dosyasının yolu. |
| [FontFamilyName](../../aspose.words.fonts/physicalfontinfo/fontfamilyname/) { get; } | Yazı tipinin aile adı. |
| [FullFontName](../../aspose.words.fonts/physicalfontinfo/fullfontname/) { get; } | Yazı tipinin tam adı. |
| [Version](../../aspose.words.fonts/physicalfontinfo/version/) { get; } | Yazı tipinin sürüm dizesi. |

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

* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)
