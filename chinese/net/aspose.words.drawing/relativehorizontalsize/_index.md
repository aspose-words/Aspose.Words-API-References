---
title: RelativeHorizontalSize Enum
linktitle: RelativeHorizontalSize
articleTitle: RelativeHorizontalSize
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.RelativeHorizontalSize 枚举，精确控制文档中形状和文本框的宽度。立即增强您的格式！
type: docs
weight: 1590
url: /zh/net/aspose.words.drawing/relativehorizontalsize/
---
## RelativeHorizontalSize enumeration

指定形状或文本框的宽度相对于水平方向的计算。

```csharp
public enum RelativeHorizontalSize
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Margin | `0` | 指定宽度是相对于左边距和右边距之间的空间来计算的。 |
| Page | `1` | 指定宽度是相对于页面宽度计算的。 |
| LeftMargin | `2` | 指定宽度是相对于左边距区域大小计算的。 |
| RightMargin | `3` | 指定宽度是相对于右边距区域大小计算的。 |
| InnerMargin | `4` | 指定宽度是相对于内边距区域大小计算的， 对于奇数页，宽度是相对于左边距区域大小计算的，对于偶数页，宽度是相对于右边距区域大小计算的。 |
| OuterMargin | `5` | 指定宽度是相对于外部边距区域大小计算的， 对于奇数页，是相对于右边距区域大小计算的，对于偶数页，是相对于左边距区域大小计算的。 |
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

* property [RelativeHorizontalSize](../shapebase/relativehorizontalsize/)
* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
