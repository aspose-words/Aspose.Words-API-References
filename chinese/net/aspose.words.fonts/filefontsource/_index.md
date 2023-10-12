---
title: Class FileFontSource
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Fonts.FileFontSource 班级. 表示存储在文件系统中的单个 TrueType 字体文件
type: docs
weight: 2870
url: /zh/net/aspose.words.fonts/filefontsource/
---
## FileFontSource class

表示存储在文件系统中的单个 TrueType 字体文件。

要了解更多信息，请访问[使用字体](https://docs.aspose.com/words/net/working-with-fonts/)文档文章。

```csharp
public class FileFontSource : FontSourceBase
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FileFontSource](filefontsource/#constructor)(string) | 向量. |
| [FileFontSource](filefontsource/#constructor_1)(string, int) | 向量. |
| [FileFontSource](filefontsource/#constructor_2)(string, int, string) | 向量. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/filefontsource/cachekey/) { get; } | 缓存中此源的键。 |
| [FilePath](../../aspose.words.fonts/filefontsource/filepath/) { get; } | 字体文件的路径。 |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | 返回字体源优先级。 |
| override [Type](../../aspose.words.fonts/filefontsource/type/) { get; } | 返回字体源的类型。 |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | 在处理字体源期间检测到可能导致格式保真度损失的问题时调用。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | 返回通过此源可用的字体列表。 |

### 例子

演示如何使用本地文件系统中的字体文件作为字体源。

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### 也可以看看

* class [FontSourceBase](../fontsourcebase/)
* 命名空间 [Aspose.Words.Fonts](../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../)


