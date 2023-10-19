---
title: EmbeddedFontStyle Enum
linktitle: EmbeddedFontStyle
articleTitle: EmbeddedFontStyle
second_title: Aspose.Words for .NET
description: Aspose.Words.Fonts.EmbeddedFontStyle Sıralama. Bir dosyanın içindeki gömülü yazı tipinin stilini belirtir.FontInfo nesne C#'da.
type: docs
weight: 2860
url: /tr/net/aspose.words.fonts/embeddedfontstyle/
---
## EmbeddedFontStyle enumeration

Bir dosyanın içindeki gömülü yazı tipinin stilini belirtir.[`FontInfo`](../fontinfo/) nesne.

```csharp
[Flags]
public enum EmbeddedFontStyle
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Regular | `0` | Normal gömülü yazı tipini belirtir. |
| Bold | `1` | Kalın gömülü yazı tipini belirtir. |
| Italic | `2` | İtalik gömülü yazı tipini belirtir. |
| BoldItalic | `3` | Kalın-İtalik gömülü yazı tipini belirtir. |

## Örnekler

Katıştırılmış bir yazı tipinin bir belgeden nasıl çıkarılacağını ve yerel dosya sistemine nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// Gömülü yazı tipi formatları .doc gibi diğer formatlarda farklı olabilir.
// Fontu çıkarmadan önce doğru formatı bilmemiz gerekiyor.
doc = new Document(MyDir + "Embedded font.doc");

Assert.IsNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular));
Assert.IsNotNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular));

// Ayrıca .doc dokümanlarından gelen gömülü OpenType formatını OpenType'a dönüştürebiliriz.
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)
