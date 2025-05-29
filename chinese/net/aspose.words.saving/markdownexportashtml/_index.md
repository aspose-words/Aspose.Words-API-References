---
title: MarkdownExportAsHtml Enum
linktitle: MarkdownExportAsHtml
articleTitle: MarkdownExportAsHtml
second_title: Aspose.Words for .NET
description: 发现 Aspose.Words.Saving.MarkdownExportAsHtml 枚举，轻松将 Markdown 元素转换为原始 HTML，增强您的文档导出选项。
type: docs
weight: 6020
url: /zh/net/aspose.words.saving/markdownexportashtml/
---
## MarkdownExportAsHtml enumeration

允许指定要作为原始 HTML 导出到 Markdown 的元素。

```csharp
[Flags]
public enum MarkdownExportAsHtml
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 使用 Markdown 语法导出所有元素，无需任何原始 HTML。 |
| Tables | `1` | 将表格导出为原始 HTML。 |

## 例子

展示如何将表格作为原始 HTML 导出到 Markdown。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Sample table:");

// 创建表。
builder.InsertCell();
builder.ParagraphFormat.Alignment = ParagraphAlignment.Right;
builder.Write("Cell1");
builder.InsertCell();
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write("Cell2");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.ExportAsHtml = MarkdownExportAsHtml.Tables;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportTableAsHtml.md", saveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
