---
title: Type
second_title: Aspose.Words for .NET API Referansı
description: Yazı tipi kaynağının türünü döndürür.
type: docs
weight: 20
url: /tr/net/aspose.words.fonts/fontsourcebase/type/
---
## FontSourceBase.Type property

Yazı tipi kaynağının türünü döndürür.

```csharp
public abstract FontSourceType Type { get; }
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

* enum [FontSourceType](../../fontsourcetype)
* class [FontSourceBase](../../fontsourcebase)
* ad alanı [Aspose.Words.Fonts](../../fontsourcebase)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->