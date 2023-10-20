---
title: MemoryFontSource Class
linktitle: MemoryFontSource
articleTitle: MemoryFontSource
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Fonts.MemoryFontSource 班级. 表示存储在内存中的单个 TrueType 字体文件 在 C#.
type: docs
weight: 3020
url: /zh/net/aspose.words.fonts/memoryfontsource/
---
## MemoryFontSource class

表示存储在内存中的单个 TrueType 字体文件。

要了解更多信息，请访问[使用字体](https://docs.aspose.com/words/net/working-with-fonts/)文档文章。

```csharp
public class MemoryFontSource : FontSourceBase
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [MemoryFontSource](memoryfontsource/#constructor)(*byte[]*) | 向量. |
| [MemoryFontSource](memoryfontsource/#constructor_1)(*byte[], int*) | 向量. |
| [MemoryFontSource](memoryfontsource/#constructor_2)(*byte[], int, string*) | 向量. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/memoryfontsource/cachekey/) { get; } | 缓存中此源的键。 |
| [FontData](../../aspose.words.fonts/memoryfontsource/fontdata/) { get; } | 二进制字体数据。 |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | 返回字体源优先级。 |
| override [Type](../../aspose.words.fonts/memoryfontsource/type/) { get; } | 返回字体源的类型。 |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | 在处理字体源期间检测到可能导致格式保真度损失的问题时调用。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | 返回通过此源可用的字体列表。 |

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

* class [FontSourceBase](../fontsourcebase/)
* 命名空间 [Aspose.Words.Fonts](../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../)
