---
title: Table.VerticalAnchor
second_title: Aspose.Words for .NET API 参考
description: Table 财产. 获取计算浮动表垂直定位的基础对象 默认值为Margin.
type: docs
weight: 340
url: /zh/net/aspose.words.tables/table/verticalanchor/
---
## Table.VerticalAnchor property

获取计算浮动表垂直定位的基础对象。 默认值为Margin.

```csharp
public RelativeVerticalPosition VerticalAnchor { get; set; }
```

### 例子

显示如何使用浮动表属性。

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

if (table.TextWrapping == TextWrapping.Around)
{
    Assert.AreEqual(RelativeHorizontalPosition.Margin, table.HorizontalAnchor);
    Assert.AreEqual(RelativeVerticalPosition.Paragraph, table.VerticalAnchor);
    Assert.AreEqual(false, table.AllowOverlap);

    // 对于 HorizontalAnchor 设置器，RelativeHorizontalPosition 中只有 Margin、Page、Column 可用。
    // 对于任何其他值，都会抛出 ArgumentException。
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // 对于 VerticalAnchor 设置器，RelativeVerticalPosition 中只有 Margin、Page、Paragraph 可用。
    // 对于任何其他值，都会抛出 ArgumentException。
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### 也可以看看

* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../table/)
* 部件 [Aspose.Words](../../../)


