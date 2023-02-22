---
title: FileFontSource.FilePath
second_title: Aspose.Words for .NET API Referansı
description: FileFontSource mülk. Yazı tipi dosyasının yolu.
type: docs
weight: 30
url: /tr/net/aspose.words.fonts/filefontsource/filepath/
---
## FileFontSource.FilePath property

Yazı tipi dosyasının yolu.

```csharp
public string FilePath { get; }
```

### Örnekler

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

* class [FileFontSource](../)
* ad alanı [Aspose.Words.Fonts](../../filefontsource/)
* toplantı [Aspose.Words](../../../)


