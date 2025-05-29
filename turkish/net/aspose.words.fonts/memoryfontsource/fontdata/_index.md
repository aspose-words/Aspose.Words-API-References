---
title: MemoryFontSource.FontData
linktitle: FontData
articleTitle: FontData
second_title: .NET için Aspose.Words
description: Sorunsuz ikili font entegrasyonu için MemoryFontSource'un FontData özelliğini keşfedin. Projelerinizi verimli font yönetimi çözümleriyle geliştirin.
type: docs
weight: 30
url: /tr/net/aspose.words.fonts/memoryfontsource/fontdata/
---
## MemoryFontSource.FontData property

İkili yazı tipi verileri.

```csharp
public byte[] FontData { get; }
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

* class [MemoryFontSource](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
