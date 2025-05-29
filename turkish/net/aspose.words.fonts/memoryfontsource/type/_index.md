---
title: MemoryFontSource.Type
linktitle: Type
articleTitle: Type
second_title: .NET için Aspose.Words
description: Tasarım hassasiyetinizi ve yaratıcılığınızı geliştirerek yazı tipi kaynak türünüzü ortaya çıkaran MemoryFontSource Type özelliğini keşfedin. Yazı tipi potansiyelinizi açığa çıkarın!
type: docs
weight: 40
url: /tr/net/aspose.words.fonts/memoryfontsource/type/
---
## MemoryFontSource.Type property

Yazı tipi kaynağının türünü döndürür.

```csharp
public override FontSourceType Type { get; }
```

## Örnekler

Bir font dosyasındaki verilerle bir bayt dizisinin font kaynağı olarak nasıl kullanılacağını gösterir.

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### Ayrıca bakınız

* enum [FontSourceType](../../fontsourcetype/)
* class [MemoryFontSource](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
