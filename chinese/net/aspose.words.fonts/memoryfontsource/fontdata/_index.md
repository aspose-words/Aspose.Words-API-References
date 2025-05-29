---
title: MemoryFontSource.FontData
linktitle: FontData
articleTitle: FontData
second_title: Aspose.Words for .NET
description: 探索 MemoryFontSource 的 FontData 属性，实现无缝二进制字体集成。使用高效的字体管理解决方案，提升您的项目质量。
type: docs
weight: 30
url: /zh/net/aspose.words.fonts/memoryfontsource/fontdata/
---
## MemoryFontSource.FontData property

二进制字体数据.

```csharp
public byte[] FontData { get; }
```

## 例子

展示如何使用包含字体文件中数据的字节数组作为字体源。

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
