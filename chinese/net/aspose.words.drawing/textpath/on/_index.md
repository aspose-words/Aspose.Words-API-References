---
title: TextPath.On
linktitle: On
articleTitle: On
second_title: Aspose.Words for .NET
description: 了解 TextPath 如何增强属性文本显示，确保设计清晰流畅、引人入胜。立即优化您的视觉效果！
type: docs
weight: 70
url: /zh/net/aspose.words.drawing/textpath/on/
---
## TextPath.On property

定义是否显示文本。

```csharp
public bool On { get; set; }
```

## 评论

默认值为`错误的`。

## 例子

演示如何使用艺术字。

```csharp
public void InsertTextPaths()
{
    Document doc = new Document();

    // 插入一个艺术字对象，以某种形状显示文本，我们可以在 Microsoft Word 中使用鼠标调整其大小并移动它。
    // 提供“ShapeType”作为参数来设置艺术字的形状。
    Shape shape = AppendWordArt(doc, "Hello World! This text is bold, and italic.",
        "Arial", 480, 24, Color.White, Color.Black, ShapeType.TextPlainText);

    // 使用相应的属性将“粗体”和“斜体”格式设置应用于文本。
    shape.TextPath.Bold = true;
    shape.TextPath.Italic = true;

    // 以下是其他各种与文本格式相关的属性。
    Assert.False(shape.TextPath.Underline);
    Assert.False(shape.TextPath.Shadow);
    Assert.False(shape.TextPath.StrikeThrough);
    Assert.False(shape.TextPath.ReverseRows);
    Assert.False(shape.TextPath.XScale);
    Assert.False(shape.TextPath.Trim);
    Assert.False(shape.TextPath.SmallCaps);

    Assert.AreEqual(36.0, shape.TextPath.Size);
    Assert.AreEqual("Hello World! This text is bold, and italic.", shape.TextPath.Text);
    Assert.AreEqual(ShapeType.TextPlainText, shape.ShapeType);

    // 使用“On”属性来显示/隐藏文本。
    shape = AppendWordArt(doc, "On set to \"true\"", "Calibri", 150, 24, Color.Yellow, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.On = true;

    shape = AppendWordArt(doc, "On set to \"false\"", "Calibri", 150, 24, Color.Yellow, Color.Purple, ShapeType.TextPlainText);
    shape.TextPath.On = false;

    // 使用“Kerning”属性来启用/禁用某些字符之间的字距调整。
    shape = AppendWordArt(doc, "Kerning: VAV", "Times New Roman", 90, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = true;

    shape = AppendWordArt(doc, "No kerning: VAV", "Times New Roman", 100, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = false;

    // 使用“Spacing”属性设置字符之间的自定义间距，范围从 0.0（无）到 1.0（默认）。
    shape = AppendWordArt(doc, "Spacing set to 0.1", "Calibri", 120, 24, Color.BlueViolet, Color.Blue, ShapeType.TextCascadeDown);
    shape.TextPath.Spacing = 0.1;

    // 将“RotateLetters”属性设置为“true”，以将每个字符逆时针旋转 90 度。
    shape = AppendWordArt(doc, "RotateLetters", "Calibri", 200, 36, Color.GreenYellow, Color.Green, ShapeType.TextWave);
    shape.TextPath.RotateLetters = true;

    // 将“SameLetterHeights”属性设置为“true”，以使每个字符的 x 高度等于大写字母高度。
    shape = AppendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300, 24, Color.DeepSkyBlue, Color.DodgerBlue, ShapeType.TextSlantUp);
    shape.TextPath.SameLetterHeights = true;

    // 默认情况下，文本的大小将始终缩放以适应包含形状的大小，从而覆盖文本大小设置。
    shape = AppendWordArt(doc, "FitShape on", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    Assert.True(shape.TextPath.FitShape);
    shape.TextPath.Size = 24.0;

    // 如果我们将“FitShape：属性设置为“false”，文本将保持大小
    // 无论形状的大小如何，“Size”属性都会指定。
    // 使用“TextPathAlignment”属性还可以将文本与形状的一侧对齐。
    shape = AppendWordArt(doc, "FitShape off", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    shape.TextPath.FitShape = false;
    shape.TextPath.Size = 24.0;
    shape.TextPath.TextPathAlignment = TextPathAlignment.Right;

    doc.Save(ArtifactsDir + "Shape.InsertTextPaths.docx");
}

/// <summary>
/// 插入一个带有艺术字形状的新段落。
/// </summary>
private static Shape AppendWordArt(Document doc, string text, string textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, ShapeType wordArtShapeType)
{
    // 创建一个内联形状，它将作为艺术字的容器。
    // 如果我们为该形状分配了艺术字指定的 ShapeType，则该形状只能是有效的艺术字形状。
    // 这些类型将在描述中包含“艺术字对象”，
    // 并且它们的枚举器常量名称都以“Text”开头。
    Shape shape = new Shape(doc, wordArtShapeType)
    {
        WrapType = WrapType.Inline,
        Width = shapeWidth,
        Height = shapeHeight,
        FillColor = wordArtFill,
        StrokeColor = line
    };

    shape.TextPath.Text = text;
    shape.TextPath.FontFamily = textFontFamily;

    Paragraph para = (Paragraph)doc.FirstSection.Body.AppendChild(new Paragraph(doc));
    para.AppendChild(shape);
    return shape;
}
```

### 也可以看看

* class [TextPath](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
