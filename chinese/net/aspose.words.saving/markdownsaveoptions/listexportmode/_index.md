---
title: MarkdownSaveOptions.ListExportMode
second_title: Aspose.Words for .NET API 参考
description: MarkdownSaveOptions 财产. 指定如何将列表项写入输出文件 默认值为MarkdownSyntax.
type: docs
weight: 60
url: /zh/net/aspose.words.saving/markdownsaveoptions/listexportmode/
---
## MarkdownSaveOptions.ListExportMode property

指定如何将列表项写入输出文件。 默认值为MarkdownSyntax.

```csharp
public MarkdownListExportMode ListExportMode { get; set; }
```

### 评论

当该属性设置为PlainText所有列表标签均 使用更新[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/)并以其实际值导出。此类lists 可能与Markdown格式不兼容，在这种情况下导入时将被识别为纯文本。

当该属性设置为MarkdownSyntax，作者尝试以允许通过 Markdown 在自动模式下计算列表项的方式导出 列表项。

### 例子

展示如何将列表项写入 Markdown 文档。

```csharp
Document doc = new Document(MyDir + "List item.docx");

// 使用 MarkdownListExportMode.PlainText 或 MarkdownListExportMode.MarkdownSyntax 导出列表。
MarkdownSaveOptions options = new MarkdownSaveOptions { ListExportMode = markdownListExportMode };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ListExportMode.md", options);
```

### 也可以看看

* enum [MarkdownListExportMode](../../markdownlistexportmode/)
* class [MarkdownSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../markdownsaveoptions/)
* 部件 [Aspose.Words](../../../)


