---
title: Table.HorizontalAnchor
linktitle: HorizontalAnchor
articleTitle: HorizontalAnchor
second_title: Aspose.Words for .NET
description: 探索 Table HorizontalAnchor 属性，优化浮动表格的定位。轻松自定义水平对齐，增强布局控制。
type: docs
weight: 170
url: /zh/net/aspose.words.tables/table/horizontalanchor/
---
## Table.HorizontalAnchor property

获取计算浮动表水平定位的基础对象。 默认值为Column.

```csharp
public RelativeHorizontalPosition HorizontalAnchor { get; set; }
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

* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
