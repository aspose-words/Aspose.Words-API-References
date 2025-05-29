---
title: FontSourceBase.Type
linktitle: Type
articleTitle: Type
second_title: .NET için Aspose.Words
description: FontSourceBase Type özelliğini keşfedin, web tasarımınızı geliştirmek ve kullanıcı deneyimini optimize etmek için font kaynak türlerini kolayca alın.
type: docs
weight: 20
url: /tr/net/aspose.words.fonts/fontsourcebase/type/
---
## FontSourceBase.Type property

Yazı tipi kaynağının türünü döndürür.

```csharp
public abstract FontSourceType Type { get; }
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
* class [FontSourceBase](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
