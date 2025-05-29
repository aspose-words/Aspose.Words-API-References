---
title: FileFontSource Class
linktitle: FileFontSource
articleTitle: FileFontSource
second_title: .NET için Aspose.Words
description: Aspose.Words.Fonts.FileFontSource'u keşfedin. Gelişmiş belge biçimlendirme ve tasarım esnekliği için TrueType yazı tipi dosyalarını sisteminizde kolayca yönetin.
type: docs
weight: 3280
url: /tr/net/aspose.words.fonts/filefontsource/
---
## FileFontSource class

Dosya sisteminde saklanan tek TrueType yazı tipi dosyasını temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yazı Tipleriyle Çalışma](https://docs.aspose.com/words/net/working-with-fonts/) belgeleme makalesi.

```csharp
public class FileFontSource : FontSourceBase
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FileFontSource](filefontsource/#constructor)(*string*) | İşlemci. |
| [FileFontSource](filefontsource/#constructor_1)(*string, int*) | İşlemci. |
| [FileFontSource](filefontsource/#constructor_2)(*string, int, string*) | İşlemci. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/filefontsource/cachekey/) { get; } | Önbellekteki bu kaynağın anahtarı. |
| [FilePath](../../aspose.words.fonts/filefontsource/filepath/) { get; } | Yazı tipi dosyasının yolu. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Yazı tipi kaynak önceliğini döndürür. |
| override [Type](../../aspose.words.fonts/filefontsource/type/) { get; } | Yazı tipi kaynağının türünü döndürür. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Biçimlendirme sadakat kaybına yol açabilecek bir sorun algılandığında yazı tipi kaynağının işlenmesi sırasında çağrılır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Bu kaynak aracılığıyla kullanılabilir yazı tiplerinin listesini döndürür. |

## Örnekler

Yerel dosya sistemindeki bir yazı tipi dosyasının yazı tipi kaynağı olarak nasıl kullanılacağını gösterir.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### Ayrıca bakınız

* class [FontSourceBase](../fontsourcebase/)
* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)
