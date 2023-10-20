---
title: FolderFontSource Class
linktitle: FolderFontSource
articleTitle: FolderFontSource
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Fonts.FolderFontSource 班级. 表示包含 TrueType 字体文件的文件夹 在 C#.
type: docs
weight: 2880
url: /zh/net/aspose.words.fonts/folderfontsource/
---
## FolderFontSource class

表示包含 TrueType 字体文件的文件夹。

要了解更多信息，请访问[使用字体](https://docs.aspose.com/words/net/working-with-fonts/)文档文章。

```csharp
public class FolderFontSource : FontSourceBase
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FolderFontSource](folderfontsource/#constructor)(*string, bool*) | 向量. |
| [FolderFontSource](folderfontsource/#constructor_1)(*string, bool, int*) | 向量. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [FolderPath](../../aspose.words.fonts/folderfontsource/folderpath/) { get; } | 文件夹路径。 |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | 返回字体源优先级。 |
| [ScanSubfolders](../../aspose.words.fonts/folderfontsource/scansubfolders/) { get; } | 确定是否扫描子文件夹。 |
| override [Type](../../aspose.words.fonts/folderfontsource/type/) { get; } | 返回字体源的类型。 |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | 在处理字体源期间检测到可能导致格式保真度损失的问题时调用。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | 返回通过此源可用的字体列表。 |

## 例子

演示如何使用包含字体的本地系统文件夹作为字体源。

```csharp
// 从包含字体文件的文件夹创建字体源。
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false, 1);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

Assert.AreEqual(FontsDir, folderFontSource.FolderPath);
Assert.AreEqual(false, folderFontSource.ScanSubfolders);
Assert.AreEqual(FontSourceType.FontsFolder, folderFontSource.Type);
Assert.AreEqual(1, folderFontSource.Priority);
```

### 也可以看看

* class [FontSourceBase](../fontsourcebase/)
* 命名空间 [Aspose.Words.Fonts](../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../)
