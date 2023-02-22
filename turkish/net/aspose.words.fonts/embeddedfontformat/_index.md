---
title: Enum EmbeddedFontFormat
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fonts.EmbeddedFontFormat Sıralama. İçerideki belirli gömülü yazı tipinin biçimini belirtirFontInfo nesne.
type: docs
weight: 2670
url: /tr/net/aspose.words.fonts/embeddedfontformat/
---
## EmbeddedFontFormat enumeration

İçerideki belirli gömülü yazı tipinin biçimini belirtir[`FontInfo`](../fontinfo/) nesne.

Bir belgeyi bir dosyaya kaydederken, yalnızca ilgili formattaki gömülü yazı tipleri yazılır.

```csharp
public enum EmbeddedFontFormat
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| EmbeddedOpenType | `0` | Katıştırılmış OpenType (EOT) Dosya Biçimini belirtir. |
| OpenType | `1` | OpenType (TrueType) yazı tipi dosyasının düz kopyası olarak gömülü yazı tipini belirtir. |

### Örnekler

Belgeden gömülü bir yazı tipinin nasıl çıkarılacağını ve yerel dosya sistemine nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// Gömülü yazı tipi biçimleri, .doc gibi diğer biçimlerde farklı olabilir.
// Yazı tipini çıkarmadan önce doğru formatı bilmemiz gerekiyor.
doc = new Document(MyDir + "Embedded font.doc");

Assert.IsNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular));
Assert.IsNotNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular));

// Ayrıca .doc dokümanlarından gelen gömülü OpenType formatını OpenType'a çevirebiliriz.
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)


