---
title: EmbeddedFontFormat Enum
linktitle: EmbeddedFontFormat
articleTitle: EmbeddedFontFormat
second_title: .NET için Aspose.Words
description: Gelişmiş belge stili için FontInfo nesnesindeki gömülü yazı tiplerinin biçimlerini tanımlayan Aspose.Words.EmbeddedFontFormat enum'ını keşfedin.
type: docs
weight: 3260
url: /tr/net/aspose.words.fonts/embeddedfontformat/
---
## EmbeddedFontFormat enumeration

İçerisindeki belirli gömülü yazı tipinin biçimini belirtir[`FontInfo`](../fontinfo/) nesne.

Bir belgeyi dosyaya kaydederken, yalnızca ilgili formattaki gömülü yazı tipleri yazılır.

```csharp
public enum EmbeddedFontFormat
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| EmbeddedOpenType | `0` | Gömülü OpenType (EOT) Dosya Biçimini belirtir. |
| OpenType | `1` | OpenType (TrueType) yazı tipi dosyasının düz kopyası olarak gömülen yazı tipini belirtir. |

## Örnekler

Bir belgeden gömülü yazı tipinin nasıl çıkarılacağını ve yerel dosya sistemine nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// Gömülü yazı tipleri .doc gibi diğer formatlarda farklı olabilir.
// Yazı tipini çıkarabilmek için öncelikle doğru formatı bilmemiz gerekiyor.
doc = new Document(MyDir + "Embedded font.doc");

Assert.IsNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular));
Assert.IsNotNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular));

// Ayrıca .doc belgelerinden gelen gömülü OpenType formatını OpenType'a dönüştürebiliriz.
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)
