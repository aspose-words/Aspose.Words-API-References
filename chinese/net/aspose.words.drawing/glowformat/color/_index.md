---
title: GlowFormat.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words for .NET
description: 探索 GlowFormat Color 属性，自定义您的发光效果。轻松设置鲜艳色彩，打造惊艳视觉效果。默认为黑色。
type: docs
weight: 10
url: /zh/net/aspose.words.drawing/glowformat/color/
---
## GlowFormat.Color property

获取或设置Color表示发光效果颜色的对象。 默认值为Black.

```csharp
public Color Color { get; set; }
```

## 例子

展示如何与辉光形状效果进行交互。

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

shape.Glow.Color = Color.Salmon;
shape.Glow.Radius = 30;
shape.Glow.Transparency = 0.15;

doc.Save(ArtifactsDir + "Shape.Glow.docx");

doc = new Document(ArtifactsDir + "Shape.Glow.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(Color.FromArgb(217, 250, 128, 114).ToArgb(), shape.Glow.Color.ToArgb());
Assert.AreEqual(30, shape.Glow.Radius);
Assert.AreEqual(0.15d, shape.Glow.Transparency, 0.01d);

shape.Glow.Remove();

Assert.AreEqual(Color.Black.ToArgb(), shape.Glow.Color.ToArgb());
Assert.AreEqual(0, shape.Glow.Radius);
Assert.AreEqual(0, shape.Glow.Transparency);
```

### 也可以看看

* class [GlowFormat](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
