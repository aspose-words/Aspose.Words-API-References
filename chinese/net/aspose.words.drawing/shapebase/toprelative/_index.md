---
title: ShapeBase.TopRelative
linktitle: TopRelative
articleTitle: TopRelative
second_title: 用于 .NET 的 Aspose.Words
description: ShapeBase TopRelative 财产. 获取或设置表示形状相对顶部位置以百分比表示的值 在 C#.
type: docs
weight: 550
url: /zh/net/aspose.words.drawing/shapebase/toprelative/
---
## ShapeBase.TopRelative property

获取或设置表示形状相对顶部位置（以百分比表示）的值。

```csharp
public float TopRelative { get; set; }
```

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

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
