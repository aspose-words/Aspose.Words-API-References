---
title: Shape.FillColor
linktitle: FillColor
articleTitle: FillColor
second_title: Aspose.Words for .NET
description: 探索形状填充颜色属性，使用鲜艳的画笔颜色自定义您的设计，增强您的形状并提升您的项目。
type: docs
weight: 50
url: /zh/net/aspose.words.drawing/shape/fillcolor/
---
## Shape.FillColor property

定义填充形状闭合路径的画笔颜色。

```csharp
public Color FillColor { get; set; }
```

## 评论

这是[`Color`](../../fill/color/)财产。

默认值为 White.

## 例子

展示如何用纯色填充形状。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 写一些文字，然后用浮动形状覆盖它。
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// 使用“StrokeColor”属性设置形状轮廓的颜色。
shape.StrokeColor = Color.CadetBlue;

// 使用“FillColor”属性设置形状内部区域的颜色。
shape.FillColor = Color.LightBlue;

// “不透明度”属性决定了颜色在 0-1 范围内的透明度，
// 其中 1 表示完全不透明，0 表示不可见。
// 默认情况下，形状填充是完全不透明的，因此我们看不到该形状上方的文本。
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// 将形状填充颜色的不透明度设置为较低的值，以便我们可以看到其下方的文本。
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### 也可以看看

* class [Shape](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
