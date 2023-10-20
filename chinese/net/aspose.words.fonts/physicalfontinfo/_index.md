---
title: PhysicalFontInfo Class
linktitle: PhysicalFontInfo
articleTitle: PhysicalFontInfo
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Fonts.PhysicalFontInfo 班级. 指定有关 Aspose.Words 字体引擎可用的物理字体的信息 在 C#.
type: docs
weight: 3030
url: /zh/net/aspose.words.fonts/physicalfontinfo/
---
## PhysicalFontInfo class

指定有关 Aspose.Words 字体引擎可用的物理字体的信息。

要了解更多信息，请访问[使用字体](https://docs.aspose.com/words/net/working-with-fonts/)文档文章。

```csharp
public class PhysicalFontInfo
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [FilePath](../../aspose.words.fonts/physicalfontinfo/filepath/) { get; } | 字体文件的路径（如果有）。 |
| [FontFamilyName](../../aspose.words.fonts/physicalfontinfo/fontfamilyname/) { get; } | 字体的系列名称。 |
| [FullFontName](../../aspose.words.fonts/physicalfontinfo/fullfontname/) { get; } | 字体的全名。 |
| [Version](../../aspose.words.fonts/physicalfontinfo/version/) { get; } | 字体的版本字符串。 |

## 例子

演示如何列出可用字体。

```csharp
// 将 Aspose.Words 配置为从自定义文件夹获取字体，然后打印每种可用字体。
FontSourceBase[] folderFontSource = { new FolderFontSource(FontsDir, true) };

foreach (PhysicalFontInfo fontInfo in folderFontSource[0].GetAvailableFonts())
{
    Console.WriteLine("FontFamilyName : {0}", fontInfo.FontFamilyName);
    Console.WriteLine("FullFontName  : {0}", fontInfo.FullFontName);
    Console.WriteLine("Version  : {0}", fontInfo.Version);
    Console.WriteLine("FilePath : {0}\n", fontInfo.FilePath);
}
```

### 也可以看看

* 命名空间 [Aspose.Words.Fonts](../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../)
