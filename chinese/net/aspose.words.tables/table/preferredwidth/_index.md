---
title: Table.PreferredWidth
linktitle: PreferredWidth
articleTitle: PreferredWidth
second_title: 用于 .NET 的 Aspose.Words
description: Table PreferredWidth 财产. 获取或设置表格首选宽度 在 C#.
type: docs
weight: 220
url: /zh/net/aspose.words.tables/table/preferredwidth/
---
## Table.PreferredWidth property

获取或设置表格首选宽度。

```csharp
public PreferredWidth PreferredWidth { get; set; }
```

## 评论

默认值为[`Auto`](../../preferredwidth/auto/)。

## 例子

演示如何将表格设置为自动适合页面宽度的 50%。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell #1");
builder.InsertCell();
builder.Write("Cell #2");
builder.InsertCell();
builder.Write("Cell #3");

table.PreferredWidth = PreferredWidth.FromPercent(50);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

### 也可以看看

* class [PreferredWidth](../../preferredwidth/)
* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
