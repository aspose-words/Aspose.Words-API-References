---
title: FileFontSource.FilePath
linktitle: FilePath
articleTitle: FilePath
second_title: 用于 .NET 的 Aspose.Words
description: FileFontSource FilePath 财产. 字体文件的路径 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.fonts/filefontsource/filepath/
---
## FileFontSource.FilePath property

字体文件的路径。

```csharp
public string FilePath { get; }
```

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

* class [FileFontSource](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
