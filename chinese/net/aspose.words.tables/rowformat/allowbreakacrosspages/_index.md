---
title: RowFormat.AllowBreakAcrossPages
linktitle: AllowBreakAcrossPages
articleTitle: AllowBreakAcrossPages
second_title: Aspose.Words for .NET
description: 发现 RowFormat AllowBreakAcrossPages 属性，使跨分页符的表格行中的文本能够无缝流动，从而增强可读性和演示效果。
type: docs
weight: 10
url: /zh/net/aspose.words.tables/rowformat/allowbreakacrosspages/
---
## RowFormat.AllowBreakAcrossPages property

如果允许表格行中的文本跨分页符拆分，则为 True。

```csharp
public bool AllowBreakAcrossPages { get; set; }
```

## 例子

展示如何禁用表中每一行的跨页分行。

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// 将“AllowBreakAcrossPages”属性设置为“false”以保留行
// 如果表格跨越两页，则将其分解为一个整体，并沿着该行分解。
// 如果行太大，无法在一页中容纳，Microsoft Word 会将其推到下一页。
// 将“AllowBreakAcrossPages”属性设置为“true”以允许行跨越两页。
foreach (Row row in table)
    row.RowFormat.AllowBreakAcrossPages = allowBreakAcrossPages;

doc.Save(ArtifactsDir + "Table.AllowBreakAcrossPages.docx");
```

### 也可以看看

* class [RowFormat](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
