---
title: FontSourceBase Class
linktitle: FontSourceBase
articleTitle: FontSourceBase
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Fonts.FontSourceBase 班级. 这是允许用户指定各种字体源的类的抽象基类 在 C#.
type: docs
weight: 2980
url: /zh/net/aspose.words.fonts/fontsourcebase/
---
## FontSourceBase class

这是允许用户指定各种字体源的类的抽象基类。

要了解更多信息，请访问[使用字体](https://docs.aspose.com/words/net/working-with-fonts/)文档文章。

```csharp
public abstract class FontSourceBase
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | 返回字体源优先级。 |
| abstract [Type](../../aspose.words.fonts/fontsourcebase/type/) { get; } | 返回字体源的类型。 |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | 在处理字体源期间检测到可能导致格式保真度损失的问题时调用。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | 返回通过此源可用的字体列表。 |

## 例子

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

* 命名空间 [Aspose.Words.Fonts](../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../)
