---
title: Stroke.ImageBytes
second_title: Aspose.Words for .NET API 参考
description: Stroke 财产. 为描边图像或图案填充定义图像
type: docs
weight: 100
url: /zh/net/aspose.words.drawing/stroke/imagebytes/
---
## Stroke.ImageBytes property

为描边图像或图案填充定义图像。

```csharp
public byte[] ImageBytes { get; }
```

### 例子

显示如何处理形状笔划特征。

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;

// 笔画可以有两种颜色，用于创建由双色调图像数据定义的图案。
// 单一颜色的笔画不使用 Color2 属性。
Assert.AreEqual(Color.FromArgb(255, 128, 0, 0), stroke.Color);
Assert.AreEqual(Color.FromArgb(255, 255, 255, 0), stroke.Color2);

Assert.NotNull(stroke.ImageBytes);
File.WriteAllBytes(ArtifactsDir + "Drawing.StrokePattern.png", stroke.ImageBytes);
```

### 也可以看看

* class [Stroke](../)
* 命名空间 [Aspose.Words.Drawing](../../stroke/)
* 部件 [Aspose.Words](../../../)


