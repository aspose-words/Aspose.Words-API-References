---
title: ShapeBase.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: 用于 .NET 的 Aspose.Words
description: ShapeBase AllowOverlap 财产. 获取或设置一个值该值指定此形状是否可以与其他形状重叠 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.drawing/shapebase/allowoverlap/
---
## ShapeBase.AllowOverlap property

获取或设置一个值，该值指定此形状是否可以与其他形状重叠。

```csharp
public bool AllowOverlap { get; set; }
```

## 评论

此属性影响 Microsoft Word 中形状的行为。 Aspose.Words 忽略此属性的值。

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

    // 只有 Margin、Page、Column 在 HorizontalAnchor setter 的relativehorizontalposition 中可用。
    // 对于任何其他值，都将引发 ArgumentException。
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // 仅边距、页面、段落可用于 VerticalAnchor setter 的relativeverticalposition。
    // 对于任何其他值，都将引发 ArgumentException。
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
