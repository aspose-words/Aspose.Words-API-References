---
title: FolderFontSource.FolderFontSource
second_title: Aspose.Words for .NET API 参考
description: FolderFontSource 构造函数. 克托尔.
type: docs
weight: 10
url: /zh/net/aspose.words.fonts/folderfontsource/folderfontsource/
---
## FolderFontSource(string, bool) {#constructor}

克托尔.

```csharp
public FolderFontSource(string folderPath, bool scanSubfolders)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| folderPath | String | 文件夹路径。 |
| scanSubfolders | Boolean | 确定是否扫描子文件夹。 |

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

---

## FolderFontSource(string, bool, int) {#constructor_1}

克托尔.

```csharp
public FolderFontSource(string folderPath, bool scanSubfolders, int priority)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| folderPath | String | 文件夹路径。 |
| scanSubfolders | Boolean | 确定是否扫描子文件夹。 |
| priority | Int32 | 字体来源优先。见[`Priority`](../../fontsourcebase/priority/)属性描述以获取更多信息。 |

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


