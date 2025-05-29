---
title: FontSourceBase Class
linktitle: FontSourceBase
articleTitle: FontSourceBase
second_title: .NET için Aspose.Words
description: Uygulamalarınızda çeşitli font kaynaklarını tanımlamak için temel soyut sınıf olan Aspose.Words.Fonts.FontSourceBase'i keşfedin. Belge biçimlendirmenizi geliştirin!
type: docs
weight: 3410
url: /tr/net/aspose.words.fonts/fontsourcebase/
---
## FontSourceBase class

Bu, kullanıcının çeşitli yazı tipi kaynaklarını belirtmesine izin veren sınıflar için soyut bir temel sınıftır.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yazı Tipleriyle Çalışma](https://docs.aspose.com/words/net/working-with-fonts/) belgeleme makalesi.

```csharp
public abstract class FontSourceBase
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Yazı tipi kaynak önceliğini döndürür. |
| abstract [Type](../../aspose.words.fonts/fontsourcebase/type/) { get; } | Yazı tipi kaynağının türünü döndürür. |
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

* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)
