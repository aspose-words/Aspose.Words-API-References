---
title: Fill.Opacity
linktitle: Opacity
articleTitle: Opacity
second_title: Aspose.Words for .NET
description: 使用填充不透明度属性控制设计的透明度，将清晰度从完全清晰调整到完全不透明，以获得令人惊叹的视觉效果。
type: docs
weight: 150
url: /zh/net/aspose.words.drawing/fill/opacity/
---
## Fill.Opacity property

获取或设置指定填充的不透明度，其值为 0.0（透明）至 1.0（不透明）之间的值。

```csharp
public double Opacity { get; set; }
```

## 评论

此属性与属性相反[`Transparency`](../transparency/)。

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

* class [Fill](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
