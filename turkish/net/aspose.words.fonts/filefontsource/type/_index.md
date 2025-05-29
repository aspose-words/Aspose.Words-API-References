---
title: FileFontSource.Type
linktitle: Type
articleTitle: Type
second_title: .NET için Aspose.Words
description: Yazı tipi kaynak türlerini kolayca belirlemek ve tasarım projelerinizi hassas tipografi çözümleriyle geliştirmek için FileFontSource Type özelliğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.fonts/filefontsource/type/
---
## FileFontSource.Type property

Yazı tipi kaynağının türünü döndürür.

```csharp
public override FontSourceType Type { get; }
```

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

* enum [FontSourceType](../../fontsourcetype/)
* class [FileFontSource](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
