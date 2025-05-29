---
title: Stroke.ImageBytes
linktitle: ImageBytes
articleTitle: ImageBytes
second_title: Aspose.Words for .NET
description: 了解如何使用 ImageBytes 属性为您的设计创建精美的描边图像和独特的图案填充。立即提升您的视觉效果！
type: docs
weight: 160
url: /zh/net/aspose.words.drawing/stroke/imagebytes/
---
## Stroke.ImageBytes property

定义描边图像或图案填充的图像。

```csharp
public byte[] ImageBytes { get; }
```

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
