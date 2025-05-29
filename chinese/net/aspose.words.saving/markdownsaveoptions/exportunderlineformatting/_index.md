---
title: MarkdownSaveOptions.ExportUnderlineFormatting
linktitle: ExportUnderlineFormatting
articleTitle: ExportUnderlineFormatting
second_title: Aspose.Words for .NET
description: 了解 MarkdownSaveOptions ExportUnderlineFormatting 属性如何增强文本导出功能。使用此布尔设置轻松控制下划线格式。
type: docs
weight: 50
url: /zh/net/aspose.words.saving/markdownsaveoptions/exportunderlineformatting/
---
## MarkdownSaveOptions.ExportUnderlineFormatting property

获取或设置一个布尔值，指示将下划线 文本格式导出为两个加号字符“++”的序列。 默认值为`错误的`.

```csharp
public bool ExportUnderlineFormatting { get; set; }
```

## 例子

展示如何将下划线格式导出为++。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Underline = Underline.Single;
builder.Write("Lorem ipsum. Dolor sit amet.");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions() { ExportUnderlineFormatting = true };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportUnderlineFormatting.md", saveOptions);
```

### 也可以看看

* class [MarkdownSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
