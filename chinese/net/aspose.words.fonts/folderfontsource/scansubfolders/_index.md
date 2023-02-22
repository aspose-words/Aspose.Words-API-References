---
title: FolderFontSource.ScanSubfolders
second_title: Aspose.Words for .NET API 参考
description: FolderFontSource 财产. 确定是否扫描子文件夹
type: docs
weight: 30
url: /zh/net/aspose.words.fonts/folderfontsource/scansubfolders/
---
## FolderFontSource.ScanSubfolders property

确定是否扫描子文件夹。

```csharp
public bool ScanSubfolders { get; }
```

### 例子

展示如何使用包含字体的本地系统文件夹作为字体源。

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
* 命名空间 [Aspose.Words.Fonts](../../folderfontsource/)
* 部件 [Aspose.Words](../../../)


