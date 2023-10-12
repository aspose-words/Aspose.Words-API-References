---
title: Class FolderFontSource
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fonts.FolderFontSource sınıf. TrueType yazı tipi dosyalarını içeren klasörü temsil eder.
type: docs
weight: 2880
url: /tr/net/aspose.words.fonts/folderfontsource/
---
## FolderFontSource class

TrueType yazı tipi dosyalarını içeren klasörü temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Fontlarla Çalışmak](https://docs.aspose.com/words/net/working-with-fonts/) dokümantasyon makalesi.

```csharp
public class FolderFontSource : FontSourceBase
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FolderFontSource](folderfontsource/#constructor)(string, bool) | Ctor. |
| [FolderFontSource](folderfontsource/#constructor_1)(string, bool, int) | Ctor. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [FolderPath](../../aspose.words.fonts/folderfontsource/folderpath/) { get; } | Klasörün yolu. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Yazı tipi kaynağı önceliğini döndürür. |
| [ScanSubfolders](../../aspose.words.fonts/folderfontsource/scansubfolders/) { get; } | Alt klasörlerin taranıp taranmayacağını belirler. |
| override [Type](../../aspose.words.fonts/folderfontsource/type/) { get; } | Yazı tipi kaynağının türünü döndürür. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Yazı tipi kaynağının işlenmesi sırasında, biçimlendirmenin aslına uygunluk kaybına yol açabilecek bir sorun algılandığında çağrılır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Bu kaynak aracılığıyla kullanılabilen yazı tiplerinin listesini döndürür. |

### Örnekler

Yazı tipi kaynağı olarak yazı tiplerini içeren yerel sistem klasörünün nasıl kullanılacağını gösterir.

```csharp
// Yazı tipi dosyalarını içeren bir klasörden yazı tipi kaynağı oluşturun.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false, 1);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

Assert.AreEqual(FontsDir, folderFontSource.FolderPath);
Assert.AreEqual(false, folderFontSource.ScanSubfolders);
Assert.AreEqual(FontSourceType.FontsFolder, folderFontSource.Type);
Assert.AreEqual(1, folderFontSource.Priority);
```

### Ayrıca bakınız

* class [FontSourceBase](../fontsourcebase/)
* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)


