---
title: FontInfoCollection.Item
linktitle: Item
articleTitle: Item
second_title: .NET için Aspose.Words
description: FontInfoCollection Item özelliğini keşfederek fontları adlarına göre kolayca alabilir, tasarım projelerinizi hassasiyet ve stil ile geliştirebilirsiniz.
type: docs
weight: 40
url: /tr/net/aspose.words.fonts/fontinfocollection/item/
---
## FontInfoCollection indexer (1 of 2)

Belirtilen ada sahip bir yazı tipi alır.

```csharp
public FontInfo this[string name] { get; }
```

| Parametre | Tanım |
| --- | --- |
| name | Bulunacak yazı tipinin büyük/küçük harfe duyarlı olmayan adı. |

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

* class [FontInfo](../../fontinfo/)
* class [FontInfoCollection](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)

---

## FontInfoCollection indexer (2 of 2)

Belirtilen dizinde bir yazı tipi alır.

```csharp
public FontInfo this[int index] { get; }
```

| Parametre | Tanım |
| --- | --- |
| index | Yazı tipinin sıfır tabanlı indeksi. |

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

* class [FontInfo](../../fontinfo/)
* class [FontInfoCollection](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
