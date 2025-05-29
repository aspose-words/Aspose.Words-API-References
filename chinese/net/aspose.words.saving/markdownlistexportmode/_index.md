---
title: MarkdownListExportMode Enum
linktitle: MarkdownListExportMode
articleTitle: MarkdownListExportMode
second_title: Aspose.Words for .NET
description: 了解 Aspose.Words 的 MarkdownListExportMode 枚举如何增强列表导出到 Markdown，确保文档的精确格式和无缝集成。
type: docs
weight: 6040
url: /zh/net/aspose.words.saving/markdownlistexportmode/
---
## MarkdownListExportMode enumeration

指定如何将列表导出到 Markdown。

```csharp
public enum MarkdownListExportMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| MarkdownSyntax | `0` | 导出与 Markdown 语法兼容的列表项。 |
| PlainText | `1` | 将列表项导出为纯文本。 |

## 例子

展示如何列出将写入 markdown 文档的项目。

```csharp
Document doc = new Document(MyDir + "List item.docx");

// 使用 MarkdownListExportMode.PlainText 或 MarkdownListExportMode.MarkdownSyntax 导出列表。
MarkdownSaveOptions options = new MarkdownSaveOptions { ListExportMode = markdownListExportMode };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ListExportMode.md", options);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
