---
title: RelativeVerticalSize Enum
linktitle: RelativeVerticalSize
articleTitle: RelativeVerticalSize
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Drawing.RelativeVerticalSize 枚举. 指定相对于垂直计算的形状或文本框架的高度 在 C#.
type: docs
weight: 1220
url: /zh/net/aspose.words.drawing/relativeverticalsize/
---
## RelativeVerticalSize enumeration

指定相对于垂直计算的形状或文本框架的高度。

```csharp
public enum RelativeVerticalSize
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Margin | `0` | 指定相对于顶部和底部边距之间的空间计算高度。 |
| Page | `1` | 指定高度是相对于页面高度计算的。 |
| TopMargin | `2` | 指定相对于上边距区域大小计算高度。 |
| BottomMargin | `3` | 指定相对于底部边距区域大小计算高度。 |
| InnerMargin | `4` | 指定高度是相对于内部页边距区域大小计算的， 是奇数页的顶部页边距区域大小和偶数页的底部页边距区域大小。 |
| OuterMargin | `5` | 指定高度是相对于外部页边距区域大小计算的， 是奇数页的底部页边距区域大小和偶数页的顶部页边距区域大小。 |
| Default | `1` | 默认值为Margin. |

## 例子

展示如何设置相对大小和位置。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 添加一个具有绝对大小和位置的简单形状。
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 40);
// 将 WrapType 设置为 WrapType.None，因为内联形状会自动转换为绝对单位。
shape.WrapType = WrapType.None;

// 检查并设置相对水平尺寸。
if (shape.RelativeHorizontalSize == RelativeHorizontalSize.Default)
{
    // 将水平尺寸绑定设置为 Margin。
    shape.RelativeHorizontalSize = RelativeHorizontalSize.Margin;
    // 将宽度设置为边距宽度的 50%。
    shape.WidthRelative = 50;
}

// 检查并设置相对垂直尺寸。
if (shape.RelativeVerticalSize == RelativeVerticalSize.Default)
{
    // 将垂直尺寸绑定设置为 Margin。
    shape.RelativeVerticalSize = RelativeVerticalSize.Margin;
    // 将高度设置为边距高度的 30%。
    shape.HeightRelative = 30;
}

// 检查并设置相对垂直位置。
if (shape.RelativeVerticalPosition == RelativeVerticalPosition.Paragraph)
{
    // 设置绑定到 TopMargin 的位置。
    shape.RelativeVerticalPosition = RelativeVerticalPosition.TopMargin;
    // 将相对顶部设置为 TopMargin 位置的 30%。
    shape.TopRelative = 30;
}

// 检查并设置相对水平位置。
if (shape.RelativeHorizontalPosition == RelativeHorizontalPosition.Default)
{
    // 将位置绑定设置为 RightMargin。
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
