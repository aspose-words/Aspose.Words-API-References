---
title: Class MemoryFontSource
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Fonts.MemoryFontSource 班级. 表示存储在内存中的单个 TrueType 字体文件
type: docs
weight: 2840
url: /zh/net/aspose.words.fonts/memoryfontsource/
---
## MemoryFontSource class

表示存储在内存中的单个 TrueType 字体文件。

```csharp
public class MemoryFontSource : FontSourceBase
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [MemoryFontSource](memoryfontsource/#constructor)(byte[]) | 克托尔. |
| [MemoryFontSource](memoryfontsource/#constructor_1)(byte[], int) | 克托尔. |
| [MemoryFontSource](memoryfontsource/#constructor_2)(byte[], int, string) | 克托尔. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/memoryfontsource/cachekey/) { get; } | 这个源在缓存中的key。 |
| [FontData](../../aspose.words.fonts/memoryfontsource/fontdata/) { get; } | 二进制字体数据。 |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | 返回字体源优先级。 |
| override [Type](../../aspose.words.fonts/memoryfontsource/type/) { get; } | 返回字体源的类型。 |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | 当检测到可能导致格式保真度丢失的问题时，在处理字体源期间调用。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | 返回通过此源可用的字体列表。 |

### 例子

演示如何将字节数组与字体文件中的数据一起用作字体源。

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


