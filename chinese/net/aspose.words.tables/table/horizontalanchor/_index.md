---
title: Table.HorizontalAnchor
linktitle: HorizontalAnchor
articleTitle: HorizontalAnchor
second_title: 用于 .NET 的 Aspose.Words
description: Table HorizontalAnchor 财产. 获取计算浮动台水平位置的基础对象 默认值为Column 在 C#.
type: docs
weight: 170
url: /zh/net/aspose.words.tables/table/horizontalanchor/
---
## Table.HorizontalAnchor property

获取计算浮动台水平位置的基础对象。 默认值为Column.

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

    // 只有 Margin、Page、Column 在 HorizontalAnchor setter 的relativehorizontalposition 中可用。
    // 对于任何其他值，都将引发 ArgumentException。
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // 仅边距、页面、段落可用于 VerticalAnchor setter 的relativeverticalposition。
    // 对于任何其他值，都将引发 ArgumentException。
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### 也可以看看

* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
