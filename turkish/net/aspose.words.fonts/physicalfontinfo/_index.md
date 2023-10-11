---
title: Class PhysicalFontInfo
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fonts.PhysicalFontInfo sınıf. Aspose.Words yazı tipi motorunun kullanabileceği fiziksel yazı tipi hakkındaki bilgileri belirtir.
type: docs
weight: 3030
url: /tr/net/aspose.words.fonts/physicalfontinfo/
---
## PhysicalFontInfo class

Aspose.Words yazı tipi motorunun kullanabileceği fiziksel yazı tipi hakkındaki bilgileri belirtir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Fontlarla Çalışmak](https://docs.aspose.com/words/net/working-with-fonts/) dokümantasyon makalesi.

```csharp
public class PhysicalFontInfo
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [FilePath](../../aspose.words.fonts/physicalfontinfo/filepath/) { get; } | Varsa yazı tipi dosyasının yolu. |
| [FontFamilyName](../../aspose.words.fonts/physicalfontinfo/fontfamilyname/) { get; } | Yazı tipinin aile adı. |
| [FullFontName](../../aspose.words.fonts/physicalfontinfo/fullfontname/) { get; } | Yazı tipinin tam adı. |
| [Version](../../aspose.words.fonts/physicalfontinfo/version/) { get; } | Yazı tipinin sürüm dizesi. |

### Örnekler

Kullanılabilir yazı tiplerinin nasıl listeleneceğini gösterir.

```csharp
// Aspose.Words'ü yazı tiplerini özel bir klasörden kaynaklayacak şekilde yapılandırın ve ardından mevcut tüm yazı tiplerini yazdırın.
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


