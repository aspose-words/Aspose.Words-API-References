---
title: Class FontSourceBase
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fonts.FontSourceBase sınıf. Bu kullanıcının çeşitli yazı tipi kaynaklarını belirlemesine olanak tanıyan sınıflar için soyut bir temel sınıftır.
type: docs
weight: 2980
url: /tr/net/aspose.words.fonts/fontsourcebase/
---
## FontSourceBase class

Bu, kullanıcının çeşitli yazı tipi kaynaklarını belirlemesine olanak tanıyan, sınıflar için soyut bir temel sınıftır.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Fontlarla Çalışmak](https://docs.aspose.com/words/net/working-with-fonts/) dokümantasyon makalesi.

```csharp
public abstract class FontSourceBase
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Yazı tipi kaynağı önceliğini döndürür. |
| abstract [Type](../../aspose.words.fonts/fontsourcebase/type/) { get; } | Yazı tipi kaynağının türünü döndürür. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Yazı tipi kaynağının işlenmesi sırasında, biçimlendirmenin aslına uygunluk kaybına yol açabilecek bir sorun algılandığında çağrılır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Bu kaynak aracılığıyla kullanılabilen yazı tiplerinin listesini döndürür. |

### Örnekler

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

* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)


