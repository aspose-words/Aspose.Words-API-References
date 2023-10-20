---
title: MemoryFontSource.FontData
linktitle: FontData
articleTitle: FontData
second_title: 用于 .NET 的 Aspose.Words
description: MemoryFontSource FontData 财产. 二进制字体数据 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.fonts/memoryfontsource/fontdata/
---
## MemoryFontSource.FontData property

二进制字体数据。

```csharp
public byte[] FontData { get; }
```

## 例子

演示如何使用字节数组和字体文件中的数据作为字体源。

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### 也可以看看

* class [MemoryFontSource](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
