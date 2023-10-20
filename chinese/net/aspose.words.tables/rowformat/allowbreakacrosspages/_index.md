---
title: RowFormat.AllowBreakAcrossPages
linktitle: AllowBreakAcrossPages
articleTitle: AllowBreakAcrossPages
second_title: 用于 .NET 的 Aspose.Words
description: RowFormat AllowBreakAcrossPages 财产. 如果允许表格行中的文本跨分页符拆分则为真 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.tables/rowformat/allowbreakacrosspages/
---
## RowFormat.AllowBreakAcrossPages property

如果允许表格行中的文本跨分页符拆分，则为真。

```csharp
public bool AllowBreakAcrossPages { get; set; }
```

## 例子

演示如何禁用表中每一行的跨页行中断。

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// 将“AllowBreakAcrossPages”属性设置为“false”以保留该行
// 如果一个表跨越两页，则沿着该行分开。
// 如果行太大而无法放入一页，Microsoft Word 会将其下推到下一页。
// 将“AllowBreakAcrossPages”属性设置为“true”以允许该行跨越两个页面。
foreach (Row row in table.OfType<Row>())
    row.RowFormat.AllowBreakAcrossPages = allowBreakAcrossPages;

doc.Save(ArtifactsDir + "Table.AllowBreakAcrossPages.docx");
```

### 也可以看看

* class [RowFormat](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
