---
title: MarkdownSaveOptions.ListExportMode
linktitle: ListExportMode
articleTitle: ListExportMode
second_title: Aspose.Words for .NET
description: 探索 MarkdownSaveOptions 的 ListExportMode 属性，它控制列表项的输出方式。使用灵活的 MarkdownSyntax 优化你的文件！
type: docs
weight: 110
url: /zh/net/aspose.words.saving/markdownsaveoptions/listexportmode/
---
## MarkdownSaveOptions.ListExportMode property

指定列表项如何写入输出文件。 默认值为MarkdownSyntax.

```csharp
public MarkdownListExportMode ListExportMode { get; set; }
```

## 评论

当此属性设置为PlainText所有列表标签均 使用更新[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/)并导出其实际值。此类lists 可能与Markdown格式不兼容，在这种情况下导入时将被识别为纯文本。

当此属性设置为MarkdownSyntax，作者尝试以允许通过 Markdown 在自动模式下对列表项进行编号的方式导出 列表项。

## 例子

展示如何列出将写入 markdown 文档的项目。

```csharp
Document doc = new Document(MyDir + "List item.docx");

// 使用 MarkdownListExportMode.PlainText 或 MarkdownListExportMode.MarkdownSyntax 导出列表。
MarkdownSaveOptions options = new MarkdownSaveOptions { ListExportMode = markdownListExportMode };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ListExportMode.md", options);
```

### 也可以看看

* enum [MarkdownListExportMode](../../markdownlistexportmode/)
* class [MarkdownSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
