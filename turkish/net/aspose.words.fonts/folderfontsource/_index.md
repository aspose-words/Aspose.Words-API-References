---
title: FolderFontSource Class
linktitle: FolderFontSource
articleTitle: FolderFontSource
second_title: .NET için Aspose.Words
description: TrueType yazı tiplerini verimli bir şekilde yönetmeniz için çözümünüz olan Aspose.Words.Fonts.FolderFontSource sınıfını keşfedin. Belgenizin tipografisini bugün geliştirin!
type: docs
weight: 3290
url: /tr/net/aspose.words.fonts/folderfontsource/
---
## FolderFontSource class

TrueType yazı tipi dosyalarını içeren klasörü temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yazı Tipleriyle Çalışma](https://docs.aspose.com/words/net/working-with-fonts/) belgeleme makalesi.

```csharp
public class FolderFontSource : FontSourceBase
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FolderFontSource](folderfontsource/#constructor)(*string, bool*) | İşlemci. |
| [FolderFontSource](folderfontsource/#constructor_1)(*string, bool, int*) | İşlemci. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [FolderPath](../../aspose.words.fonts/folderfontsource/folderpath/) { get; } | Klasöre giden yol. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Yazı tipi kaynak önceliğini döndürür. |
| [ScanSubfolders](../../aspose.words.fonts/folderfontsource/scansubfolders/) { get; } | Alt klasörlerin taranıp taranmayacağını belirler. |
| override [Type](../../aspose.words.fonts/folderfontsource/type/) { get; } | Yazı tipi kaynağının türünü döndürür. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Biçimlendirme sadakat kaybına yol açabilecek bir sorun algılandığında yazı tipi kaynağının işlenmesi sırasında çağrılır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Bu kaynak aracılığıyla kullanılabilir yazı tiplerinin listesini döndürür. |

## Örnekler

Font kaynağı olarak fontları içeren yerel bir sistem klasörünün nasıl kullanılacağını gösterir.

```csharp
// Font dosyalarını içeren bir klasörden bir font kaynağı oluştur.
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
