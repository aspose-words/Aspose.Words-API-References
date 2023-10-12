---
title: RowFormat.AllowBreakAcrossPages
second_title: Aspose.Words for .NET API 参考
description: RowFormat 财产. 如果允许表格行中的文本跨分页符拆分则为 True
type: docs
weight: 10
url: /zh/net/aspose.words.tables/rowformat/allowbreakacrosspages/
---
## RowFormat.AllowBreakAcrossPages property

如果允许表格行中的文本跨分页符拆分，则为 True。

```csharp
public bool AllowBreakAcrossPages { get; set; }
```

### 例子

演示如何禁用表中每一行的跨页行分隔。

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// 将“AllowBreakAcrossPages”属性设置为“false”以保留该行
// 如果表格跨越两页，则在一个片段中，两页沿着该行分开。
// 如果该行太大而无法容纳在一页中，Microsoft Word 会将其推到下一页。
// 将“AllowBreakAcrossPages”属性设置为“true”以允许行跨两页分解。
foreach (Row row in table.OfType<Row>())
    row.RowFormat.AllowBreakAcrossPages = allowBreakAcrossPages;

doc.Save(ArtifactsDir + "Table.AllowBreakAcrossPages.docx");
```

### 也可以看看

* class [RowFormat](../)
* 命名空间 [Aspose.Words.Tables](../../rowformat/)
* 部件 [Aspose.Words](../../../)


