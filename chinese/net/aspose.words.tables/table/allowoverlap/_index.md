---
title: Table.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: Aspose.Words for .NET
description: 探索表格的 AllowOverlap 属性，该属性控制浮动对象是否可以与表格重叠。增强布局灵活性，实现更佳的文档呈现效果。
type: docs
weight: 70
url: /zh/net/aspose.words.tables/table/allowoverlap/
---
## Table.AllowOverlap property

获取浮动表格是否允许文档中的其他浮动对象在显示时与其范围重叠。 默认值为`真的`.

```csharp
public bool AllowOverlap { get; }
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

* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
