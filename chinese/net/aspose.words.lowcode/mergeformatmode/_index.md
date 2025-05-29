---
title: MergeFormatMode Enum
linktitle: MergeFormatMode
articleTitle: MergeFormatMode
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.LowCode.MergeFormatMode 枚举，优化文档合并。轻松增强合并多个文件时的格式控制。
type: docs
weight: 4290
url: /zh/net/aspose.words.lowcode/mergeformatmode/
---
## MergeFormatMode enumeration

指定合并多个文档时如何合并格式。

```csharp
public enum MergeFormatMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| MergeFormatting | `0` | 结合合并文档的格式。 |
| KeepSourceFormatting | `1` | 表示源文档将保留其原始格式， 例如字体样式、大小、颜色、缩进以及应用于其内容的任何其他格式元素。 |
| KeepSourceLayout | `2` | 在最终文档中保留原始文档的布局。 |

## 例子

展示如何将文档合并为单个输出文档。

```csharp
//合并文档有几种方法：
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../)
