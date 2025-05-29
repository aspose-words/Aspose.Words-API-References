---
title: FontInfo.GetEmbeddedFontAsOpenType
linktitle: GetEmbeddedFontAsOpenType
articleTitle: GetEmbeddedFontAsOpenType
second_title: .NET için Aspose.Words
description: FontInfo GetEmbeddedFontAsOpenType yönteminin OpenType formatında gömülü fontları nasıl aldığını, tasarım esnekliğinizi ve kalitenizi nasıl artırdığını keşfedin.
type: docs
weight: 100
url: /tr/net/aspose.words.fonts/fontinfo/getembeddedfontasopentype/
---
## FontInfo.GetEmbeddedFontAsOpenType method

OpenType biçiminde gömülü bir yazı tipi dosyası alır. Gömülü OpenType biçimindeki yazı tipleri OpenType'a dönüştürülür.

```csharp
public byte[] GetEmbeddedFontAsOpenType(EmbeddedFontStyle style)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| style | EmbeddedFontStyle | Alınacak yazı tipi stilini belirtir. |

### Geri dönüş değeri

İade`hükümsüz` belirtilen yazı tipi gömülü değilse.

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

* enum [EmbeddedFontStyle](../../embeddedfontstyle/)
* class [FontInfo](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
