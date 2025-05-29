---
title: Table.VerticalAnchor
linktitle: VerticalAnchor
articleTitle: VerticalAnchor
second_title: Aspose.Words for .NET
description: 探索 Table VerticalAnchor 属性，以优化浮动表格的定位。学习如何使用其默认 Margin 值来增强布局控制。
type: docs
weight: 340
url: /zh/net/aspose.words.tables/table/verticalanchor/
---
## Table.VerticalAnchor property

获取计算浮动表垂直定位的基础对象。 默认值为Margin.

```csharp
public RelativeVerticalPosition VerticalAnchor { get; set; }
```

## 例子

展示如何使用浮动表属性。

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

if (table.TextWrapping == TextWrapping.Around)
{
    Assert.AreEqual(RelativeHorizontalPosition.Margin, table.HorizontalAnchor);
    Assert.AreEqual(RelativeVerticalPosition.Paragraph, table.VerticalAnchor);
    Assert.AreEqual(false, table.AllowOverlap);

    // 仅 Margin、Page、Column 在 RelativeHorizontalPosition 中可用于 HorizontalAnchor 设置器。
    // 对于任何其他值，都会抛出 ArgumentException。
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // 仅 Margin、Page、Paragraph 在 RelativeVerticalPosition 中可用于 VerticalAnchor 设置器。
    // 对于任何其他值，都会抛出 ArgumentException。
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### 也可以看看

* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
