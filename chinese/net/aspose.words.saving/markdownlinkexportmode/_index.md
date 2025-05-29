---
title: MarkdownLinkExportMode Enum
linktitle: MarkdownLinkExportMode
articleTitle: MarkdownLinkExportMode
second_title: Aspose.Words for .NET
description: 了解 Aspose.Words MarkdownLinkExportMode 枚举如何增强 Markdown 中的链接导出，轻松优化您的文档转换过程。
type: docs
weight: 6030
url: /zh/net/aspose.words.saving/markdownlinkexportmode/
---
## MarkdownLinkExportMode enumeration

指定如何将链接导出到 Markdown。

```csharp
public enum MarkdownLinkExportMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Auto | `0` | 自动检测每个链接的导出模式。 |
| Inline | `1` | 将所有链接导出为内联块。 |
| Reference | `2` | 将所有链接导出为参考块。 |

## 例子

展示如何将链接写入 .md 文件。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertShape(ShapeType.Balloon, 100, 100);

// 图像将被写入作为参考：
// ![ref1]
//
// [ref1]: aw_ref.001.png
MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.LinkExportMode = MarkdownLinkExportMode.Reference;
doc.Save(ArtifactsDir + "MarkdownSaveOptions.LinkExportMode.Reference.md", saveOptions);

// 图像将以内联形式写入：
// ![](aw_inline.001.png)
saveOptions.LinkExportMode = MarkdownLinkExportMode.Inline;
doc.Save(ArtifactsDir + "MarkdownSaveOptions.LinkExportMode.Inline.md", saveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
