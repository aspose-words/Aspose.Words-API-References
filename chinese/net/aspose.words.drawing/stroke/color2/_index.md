---
title: Stroke.Color2
linktitle: Color2
articleTitle: Color2
second_title: Aspose.Words for .NET
description: 探索描边颜色 2 属性 - 使用可自定义的第二种描边颜色增强您的设计，以获得生动、引人注目的视觉效果。
type: docs
weight: 60
url: /zh/net/aspose.words.drawing/stroke/color2/
---
## Stroke.Color2 property

定义笔触的第二种颜色。

```csharp
public Color Color2 { get; set; }
```

## 评论

默认值为[`Shape`](../../shape/)is White.

## 例子

展示如何处理形状笔触特征。

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;

// 笔触可以有两种颜色，用于创建由双色调图像数据定义的图案。
// 单一颜色的笔触不使用 Color2 属性。
Assert.AreEqual(Color.FromArgb(255, 128, 0, 0), stroke.Color);
Assert.AreEqual(Color.FromArgb(255, 255, 255, 0), stroke.Color2);

Assert.NotNull(stroke.ImageBytes);
File.WriteAllBytes(ArtifactsDir + "Drawing.StrokePattern.png", stroke.ImageBytes);
```

### 也可以看看

* class [Stroke](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
