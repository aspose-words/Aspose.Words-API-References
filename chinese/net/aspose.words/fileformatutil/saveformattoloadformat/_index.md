---
title: FileFormatUtil.SaveFormatToLoadFormat
linktitle: SaveFormatToLoadFormat
articleTitle: SaveFormatToLoadFormat
second_title: Aspose.Words for .NET
description: 使用 FileFormatUtil 方法轻松将 SaveFormat 转换为 LoadFormat。立即简化文件管理并增强兼容性！
type: docs
weight: 90
url: /zh/net/aspose.words/fileformatutil/saveformattoloadformat/
---
## FileFormatUtil.SaveFormatToLoadFormat method

转换[`SaveFormat`](../../saveformat/)价值[`LoadFormat`](../../loadformat/)如果可能的话，值。

```csharp
public static LoadFormat SaveFormatToLoadFormat(SaveFormat saveFormat)
```

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentException | 无法转换时抛出。 |

## 例子

展示如何将保存格式转换为其相应的加载格式。

```csharp
Assert.AreEqual(LoadFormat.Html, FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Html));

// 某些文件类型可以保存文档，但不能使用 Aspose.Words 加载。
// 如果我们尝试将这种类型的保存格式转换为加载格式，则会引发异常。
Assert.Throws<ArgumentException>(() => FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Jpeg));
```

### 也可以看看

* enum [LoadFormat](../../loadformat/)
* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
