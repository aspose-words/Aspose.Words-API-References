---
title: FontSourceType Enum
linktitle: FontSourceType
articleTitle: FontSourceType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fonts.FontSourceType 枚举，实现高效的字体源管理。使用灵活的字体选项优化您的文档处理。
type: docs
weight: 3420
url: /zh/net/aspose.words.fonts/fontsourcetype/
---
## FontSourceType enumeration

指定字体源的类型。

```csharp
public enum FontSourceType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| FontFile | `0` | A[`FileFontSource`](../filefontsource/)代表单个字体文件的对象. |
| FontsFolder | `1` | A[`FolderFontSource`](../folderfontsource/)表示包含字体文件的文件夹的对象。 |
| MemoryFont | `2` | A[`MemoryFontSource`](../memoryfontsource/)代表内存中单一字体的对象。 |
| SystemFonts | `3` | A[`SystemFontSource`](../systemfontsource/)代表系统中安装的所有字体的对象。 |
| FontStream | `4` | A[`StreamFontSource`](../streamfontsource/)表示带有字体数据流的对象。 |

## 例子

展示如何使用本地文件系统中的字体文件作为字体源。

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
