---
title: Enum RelativeHorizontalSize
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Drawing.RelativeHorizontalSize 枚举. 指定相对于形状或文本框架的水平计算宽度
type: docs
weight: 1200
url: /zh/net/aspose.words.drawing/relativehorizontalsize/
---
## RelativeHorizontalSize enumeration

指定相对于形状或文本框架的水平计算宽度。

```csharp
public enum RelativeHorizontalSize
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Margin | `0` | 指定宽度是相对于左右边距之间的空间计算的。 |
| Page | `1` | 指定宽度是相对于页面宽度计算的。 |
| LeftMargin | `2` | 指定宽度是相对于左边距区域大小计算的。 |
| RightMargin | `3` | 指定宽度是相对于右边距区域大小计算的。 |
| InnerMargin | `4` | 指定宽度是相对于内边距区域大小计算的， 是奇数页的左边距区域大小，偶数页的右边距区域大小。 |
| OuterMargin | `5` | 指定宽度是相对于外边距区域大小计算的， 是奇数页的右边距区域大小，偶数页的左边距区域大小。 |
| Default | `1` | 默认值为Margin. |

### 例子

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

* property [RelativeHorizontalSize](../shapebase/relativehorizontalsize/)
* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)


