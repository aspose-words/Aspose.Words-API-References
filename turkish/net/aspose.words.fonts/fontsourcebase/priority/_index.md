---
title: FontSourceBase.Priority
second_title: Aspose.Words for .NET API Referansı
description: FontSourceBase mülk. Yazı tipi kaynağı önceliğini döndürür.
type: docs
weight: 10
url: /tr/net/aspose.words.fonts/fontsourcebase/priority/
---
## FontSourceBase.Priority property

Yazı tipi kaynağı önceliğini döndürür.

```csharp
public int Priority { get; }
```

### Notlar

Bu değer, farklı font kaynaklarında aynı aile adı ve stiline sahip fontlar bulunduğunda kullanılır. Bu durumda Aspose.Words, kaynaktan öncelik değeri daha yüksek olan fontu seçer.

Varsayılan değer 0'dır.

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

* class [FontSourceBase](../)
* ad alanı [Aspose.Words.Fonts](../../fontsourcebase/)
* toplantı [Aspose.Words](../../../)


