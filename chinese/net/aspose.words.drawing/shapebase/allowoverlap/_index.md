---
title: ShapeBase.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: Aspose.Words for .NET
description: 探索 ShapeBase AllowOverlap 属性，通过启用或禁用与其他形状的重叠来控制形状交互，以增强设计灵活性。
type: docs
weight: 10
url: /zh/net/aspose.words.drawing/shapebase/allowoverlap/
---
## ShapeBase.AllowOverlap property

获取或设置一个值，指定此形状是否可以与其他形状重叠。

```csharp
public bool AllowOverlap { get; set; }
```

## 评论

此属性会影响 Microsoft Word 中形状的行为。 Aspose.Words 忽略此属性的值。

此属性仅适用于顶级形状。

默认值为`真的`。

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

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
