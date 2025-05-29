---
title: MemoryFontSource Class
linktitle: MemoryFontSource
articleTitle: MemoryFontSource
second_title: .NET için Aspose.Words
description: Gelişmiş belge işleme için bellekte depolanan TrueType yazı tiplerine sorunsuz erişim sağlayan Aspose.Words.Fonts.MemoryFontSource sınıfını keşfedin.
type: docs
weight: 3450
url: /tr/net/aspose.words.fonts/memoryfontsource/
---
## MemoryFontSource class

Bellekte depolanan tek TrueType yazı tipi dosyasını temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yazı Tipleriyle Çalışma](https://docs.aspose.com/words/net/working-with-fonts/) belgeleme makalesi.

```csharp
public class MemoryFontSource : FontSourceBase
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [MemoryFontSource](memoryfontsource/#constructor)(*byte[]*) | İşlemci. |
| [MemoryFontSource](memoryfontsource/#constructor_1)(*byte[], int*) | İşlemci. |
| [MemoryFontSource](memoryfontsource/#constructor_2)(*byte[], int, string*) | İşlemci. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/memoryfontsource/cachekey/) { get; } | Önbellekteki bu kaynağın anahtarı. |
| [FontData](../../aspose.words.fonts/memoryfontsource/fontdata/) { get; } | İkili yazı tipi verileri. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Yazı tipi kaynak önceliğini döndürür. |
| override [Type](../../aspose.words.fonts/memoryfontsource/type/) { get; } | Yazı tipi kaynağının türünü döndürür. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Biçimlendirme sadakat kaybına yol açabilecek bir sorun algılandığında yazı tipi kaynağının işlenmesi sırasında çağrılır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Bu kaynak aracılığıyla kullanılabilir yazı tiplerinin listesini döndürür. |

## Örnekler

Bir font dosyasındaki verilerle bir bayt dizisinin font kaynağı olarak nasıl kullanılacağını gösterir.

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### Ayrıca bakınız

* class [FontSourceBase](../fontsourcebase/)
* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)
