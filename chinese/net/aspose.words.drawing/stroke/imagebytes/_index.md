---
title: Stroke.ImageBytes
linktitle: ImageBytes
articleTitle: ImageBytes
second_title: 用于 .NET 的 Aspose.Words
description: Stroke ImageBytes 财产. 定义描边图像或图案填充的图像 在 C#.
type: docs
weight: 110
url: /zh/net/aspose.words.drawing/stroke/imagebytes/
---
## Stroke.ImageBytes property

定义描边图像或图案填充的图像。

```csharp
public byte[] ImageBytes { get; }
```

## 例子

展示如何处理形状笔划特征。

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
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
