---
title: ShapeBase.RelativeHorizontalSize
linktitle: RelativeHorizontalSize
articleTitle: RelativeHorizontalSize
second_title: Aspose.Words for .NET
description: 探索 ShapeBase RelativeHorizontalSize 属性，轻松水平调整形状大小，从而增强设计灵活性和精确度。
type: docs
weight: 460
url: /zh/net/aspose.words.drawing/shapebase/relativehorizontalsize/
---
## ShapeBase.RelativeHorizontalSize property

获取或设置形状在水平方向上的相对大小值。

```csharp
public RelativeHorizontalSize RelativeHorizontalSize { get; set; }
```

## 评论

默认值为[`RelativeHorizontalSize`](../../relativehorizontalsize/)。

仅在以下情况下有效[`WidthRelative`](../widthrelative/)已设置。

## 例子

展示如何设置相对大小和位置。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 添加具有绝对大小和位置的简单形状。
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 40);
// 将 WrapType 设置为 WrapType.None，因为内联形状会自动转换为绝对单位。
shape.WrapType = WrapType.None;

// 检查并设置相对水平尺寸。
if (shape.RelativeHorizontalSize == RelativeHorizontalSize.Default)
{
    // 设置水平尺寸绑定到Margin。
    shape.RelativeHorizontalSize = RelativeHorizontalSize.Margin;
    // 将宽度设置为边距宽度的 50%。
    shape.WidthRelative = 50;
}

// 检查并设置相对垂直尺寸。
if (shape.RelativeVerticalSize == RelativeVerticalSize.Default)
{
    // 设置垂直尺寸绑定到Margin。
    shape.RelativeVerticalSize = RelativeVerticalSize.Margin;
    // 将高度设置为边距高度的 30%。
    shape.HeightRelative = 30;
}

// 检查并设置相对垂直位置。
if (shape.RelativeVerticalPosition == RelativeVerticalPosition.Paragraph)
{
    // 设置与 TopMargin 的位置绑定。
    shape.RelativeVerticalPosition = RelativeVerticalPosition.TopMargin;
    // 将相对 Top 设置为 TopMargin 位置的 30%。
    shape.TopRelative = 30;
}

// 检查并设置相对水平位置。
if (shape.RelativeHorizontalPosition == RelativeHorizontalPosition.Default)
{
    // 设置位置绑定到RightMargin。
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.RightMargin;
    // 位置相对值可以为负数。
    shape.LeftRelative = -260;
}

doc.Save(ArtifactsDir + "Shape.RelativeSizeAndPosition.docx");
```

### 也可以看看

* enum [RelativeHorizontalSize](../../relativehorizontalsize/)
* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
