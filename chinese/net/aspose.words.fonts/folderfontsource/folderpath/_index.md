---
title: FolderFontSource.FolderPath
linktitle: FolderPath
articleTitle: FolderPath
second_title: 用于 .NET 的 Aspose.Words
description: FolderFontSource FolderPath 财产. 文件夹路径 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.fonts/folderfontsource/folderpath/
---
## FolderFontSource.FolderPath property

文件夹路径。

```csharp
public string FolderPath { get; }
```

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

* class [FolderFontSource](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
