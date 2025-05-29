---
title: RelativeVerticalSize Enum
linktitle: RelativeVerticalSize
articleTitle: RelativeVerticalSize
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.RelativeVerticalSize 枚举，它定义形状和文本框的垂直高度计算，增强文档布局精度。
type: docs
weight: 1610
url: /zh/net/aspose.words.drawing/relativeverticalsize/
---
## RelativeVerticalSize enumeration

指定形状或文本框的垂直高度计算依据。

```csharp
public enum RelativeVerticalSize
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Margin | `0` | 指定高度是相对于顶部和底部边距之间的空间计算的。 |
| Page | `1` | 指定高度是相对于页面高度计算的。 |
| TopMargin | `2` | 指定高度是相对于顶部边距区域大小计算的。 |
| BottomMargin | `3` | 指定高度是相对于底部边距区域大小计算的。 |
| InnerMargin | `4` | 指定高度是相对于内边距区域大小计算的， 对于奇数页，是相对于顶部边距区域大小计算的，对于偶数页，是相对于底部边距区域大小计算的。 |
| OuterMargin | `5` | 指定高度是相对于外部边距区域大小计算的， 对于奇数页，是相对于底部边距区域大小计算的，对于偶数页，是相对于顶部边距区域大小计算的。 |
| Default | `1` | 默认值为Margin. |

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

* property [RelativeVerticalSize](../shapebase/relativeverticalsize/)
* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
