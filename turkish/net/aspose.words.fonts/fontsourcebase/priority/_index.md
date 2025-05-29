---
title: FontSourceBase.Priority
linktitle: Priority
articleTitle: Priority
second_title: .NET için Aspose.Words
description: Font kaynaklarınızı optimize etmek için FontSourceBase Öncelik özelliğini keşfedin. Performansı artırın ve kullanıcı deneyimini zahmetsizce iyileştirin!
type: docs
weight: 10
url: /tr/net/aspose.words.fonts/fontsourcebase/priority/
---
## FontSourceBase.Priority property

Yazı tipi kaynak önceliğini döndürür.

```csharp
public int Priority { get; }
```

## Notlar

Bu değer, farklı font kaynaklarında aynı aile adına ve stile sahip fontlar olduğunda kullanılır. Bu durumda Aspose.Words kaynaktan daha yüksek öncelik değerine sahip fontu seçer.

Varsayılan değer 0'dır.

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

* class [FontSourceBase](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
