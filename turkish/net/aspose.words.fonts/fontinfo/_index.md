---
title: FontInfo Class
linktitle: FontInfo
articleTitle: FontInfo
second_title: Aspose.Words for .NET
description: Aspose.Words.Fonts.FontInfo sınıf. Belgede kullanılan yazı tipiyle ilgili bilgileri belirtir C#'da.
type: docs
weight: 2920
url: /tr/net/aspose.words.fonts/fontinfo/
---
## FontInfo class

Belgede kullanılan yazı tipiyle ilgili bilgileri belirtir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Fontlarla Çalışmak](https://docs.aspose.com/words/net/working-with-fonts/) dokümantasyon makalesi.

```csharp
public class FontInfo
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AltName](../../aspose.words.fonts/fontinfo/altname/) { get; set; } | Yazı tipinin alternatif adını alır veya ayarlar. |
| [Charset](../../aspose.words.fonts/fontinfo/charset/) { get; set; } | Yazı tipi için karakter kümesini alır veya ayarlar. |
| [Family](../../aspose.words.fonts/fontinfo/family/) { get; set; } | Bu yazı tipinin ait olduğu yazı tipi ailesini alır veya ayarlar. |
| [IsTrueType](../../aspose.words.fonts/fontinfo/istruetype/) { get; set; } | Bu yazı tipinin raster veya vektör yazı tipi yerine TrueType veya OpenType yazı tipi olduğunu belirtir. Varsayılan:`doğru` . |
| [Name](../../aspose.words.fonts/fontinfo/name/) { get; } | Yazı tipinin adını alır. |
| [Panose](../../aspose.words.fonts/fontinfo/panose/) { get; set; } | PANOSE yazı tipi sınıflandırma numarasını alır veya ayarlar. |
| [Pitch](../../aspose.words.fonts/fontinfo/pitch/) { get; set; } | Karakter aralığı, yazı tipinin sabit aralıklı mı, orantılı aralıklı mı olduğunu yoksa varsayılan bir ayara mı bağlı olduğunu gösterir. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetEmbeddedFont](../../aspose.words.fonts/fontinfo/getembeddedfont/)(*[EmbeddedFontFormat](../embeddedfontformat/), [EmbeddedFontStyle](../embeddedfontstyle/)*) | Belirli bir gömülü yazı tipi dosyasını alır. |
| [GetEmbeddedFontAsOpenType](../../aspose.words.fonts/fontinfo/getembeddedfontasopentype/)(*[EmbeddedFontStyle](../embeddedfontstyle/)*) | OpenType formatında gömülü bir yazı tipi dosyası alır. Gömülü OpenType biçimindeki yazı tipleri OpenType. 'ye dönüştürülür |

## Notlar

Bu sınıfın örneklerini doğrudan oluşturmazsınız. Kullan[`FontInfos`](../../aspose.words/documentbase/fontinfos/) Bir belgede tanımlanan yazı tiplerinin koleksiyonuna erişme özelliği.

## Örnekler

Bir belgede hangi yazı tiplerinin mevcut olduğuna ilişkin ayrıntıların nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Belgedeki tüm kullanılan ve kullanılmayan yazı tiplerini yazdırın.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)
