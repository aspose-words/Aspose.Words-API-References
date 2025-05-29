---
title: GlowFormat Class
linktitle: GlowFormat
articleTitle: GlowFormat
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.GlowFormat 类，使用令人惊叹的光晕效果增强您的文档。使用独特的格式选项提升您的设计！
type: docs
weight: 1300
url: /zh/net/aspose.words.drawing/glowformat/
---
## GlowFormat class

表示对象的发光格式。

```csharp
public class GlowFormat
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Color](../../aspose.words.drawing/glowformat/color/) { get; set; } | 获取或设置Color表示发光效果颜色的对象。 默认值为Black. |
| [Radius](../../aspose.words.drawing/glowformat/radius/) { get; set; } | 获取或设置一个双精度值，以点 (pt) 为单位表示发光效果半径的长度。 默认值为 0.0。 |
| [Transparency](../../aspose.words.drawing/glowformat/transparency/) { get; set; } | 获取或设置发光效果的透明度，值为 0.0（不透明）至 1.0（透明）之间的值。 默认值为 0.0。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Remove](../../aspose.words.drawing/glowformat/remove/)() | 删除`GlowFormat`来自父对象。 |

## 评论

使用[`Glow`](../shapebase/glow/)属性来访问对象的发光属性。 您不创建`GlowFormat`直接上课。

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

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
