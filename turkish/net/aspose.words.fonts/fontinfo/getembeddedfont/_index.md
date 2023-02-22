---
title: FontInfo.GetEmbeddedFont
second_title: Aspose.Words for .NET API Referansı
description: FontInfo yöntem. Belirli bir gömülü yazı tipi dosyasını alır.
type: docs
weight: 80
url: /tr/net/aspose.words.fonts/fontinfo/getembeddedfont/
---
## FontInfo.GetEmbeddedFont method

Belirli bir gömülü yazı tipi dosyasını alır.

```csharp
public byte[] GetEmbeddedFont(EmbeddedFontFormat format, EmbeddedFontStyle style)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| format | EmbeddedFontFormat | Alınacak yazı tipi biçimini belirtir. |
| style | EmbeddedFontStyle | Alınacak yazı tipi stilini belirtir. |

### Geri dönüş değeri

İadeler`hükümsüz`belirtilen yazı tipi gömülü değilse.

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

* enum [EmbeddedFontFormat](../../embeddedfontformat/)
* enum [EmbeddedFontStyle](../../embeddedfontstyle/)
* class [FontInfo](../)
* ad alanı [Aspose.Words.Fonts](../../fontinfo/)
* toplantı [Aspose.Words](../../../)


