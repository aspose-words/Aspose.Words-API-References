---
title: FontInfo Class
linktitle: FontInfo
articleTitle: FontInfo
second_title: .NET için Aspose.Words
description: Belgeleriniz için ayrıntılı yazı tipi içgörülerine ulaşmanızı, metin kalitesini ve görsel çekiciliği artırmanızı sağlayacak Aspose.Words.Fonts.FontInfo sınıfını keşfedin.
type: docs
weight: 3350
url: /tr/net/aspose.words.fonts/fontinfo/
---
## FontInfo class

Belgede kullanılan bir yazı tipi hakkında bilgi belirtir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yazı Tipleriyle Çalışma](https://docs.aspose.com/words/net/working-with-fonts/) belgeleme makalesi.

```csharp
public class FontInfo
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AltName](../../aspose.words.fonts/fontinfo/altname/) { get; set; } | Yazı tipi için alternatif adı alır veya ayarlar. |
| [Charset](../../aspose.words.fonts/fontinfo/charset/) { get; set; } | Yazı tipi için karakter kümesini alır veya ayarlar. |
| [EmbeddingLicensingRights](../../aspose.words.fonts/fontinfo/embeddinglicensingrights/) { get; } | Gömülü yazı tipi lisanslama haklarını alır. |
| [Family](../../aspose.words.fonts/fontinfo/family/) { get; set; } | Bu yazı tipinin ait olduğu yazı tipi ailesini alır veya ayarlar. |
| [IsTrueType](../../aspose.words.fonts/fontinfo/istruetype/) { get; set; } | Bu yazı tipinin raster veya vektör yazı tipinin aksine TrueType veya OpenType yazı tipi olduğunu belirtir. Varsayılan`doğru` . |
| [Name](../../aspose.words.fonts/fontinfo/name/) { get; } | Yazı tipinin adını alır. |
| [Panose](../../aspose.words.fonts/fontinfo/panose/) { get; set; } | PANOSE yazı tipi sınıflandırma numarasını alır veya ayarlar. |
| [Pitch](../../aspose.words.fonts/fontinfo/pitch/) { get; set; } | Perde, yazı tipinin sabit perdeli, orantılı aralıklı olup olmadığını veya varsayılan bir ayara bağlı olup olmadığını gösterir. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetEmbeddedFont](../../aspose.words.fonts/fontinfo/getembeddedfont/)(*[EmbeddedFontFormat](../embeddedfontformat/), [EmbeddedFontStyle](../embeddedfontstyle/)*) | Belirli bir gömülü yazı tipi dosyasını alır. |
| [GetEmbeddedFontAsOpenType](../../aspose.words.fonts/fontinfo/getembeddedfontasopentype/)(*[EmbeddedFontStyle](../embeddedfontstyle/)*) | OpenType biçiminde gömülü bir yazı tipi dosyası alır. Gömülü OpenType biçimindeki yazı tipleri OpenType'a dönüştürülür. |

## Notlar

Bu sınıfın örneklerini doğrudan oluşturmazsınız. [`FontInfos`](../../aspose.words/documentbase/fontinfos/) Bir belgede tanımlanan fonts koleksiyonuna erişmek için özellik.

## Örnekler

Bir belgede hangi yazı tiplerinin bulunduğunun ayrıntılarının nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Belgedeki tüm kullanılan ve kullanılmayan yazı tiplerini yazdır.
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
