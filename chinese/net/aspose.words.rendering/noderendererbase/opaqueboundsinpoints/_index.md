---
title: NodeRendererBase.OpaqueBoundsInPoints
linktitle: OpaqueBoundsInPoints
articleTitle: OpaqueBoundsInPoints
second_title: 用于 .NET 的 Aspose.Words
description: NodeRendererBase OpaqueBoundsInPoints 财产. 获取形状的不透明边界以点为单位 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.rendering/noderendererbase/opaqueboundsinpoints/
---
## NodeRendererBase.OpaqueBoundsInPoints property

获取形状的不透明边界（以点为单位）。

```csharp
public RectangleF OpaqueBoundsInPoints { get; }
```

## 评论

此属性返回形状的不透明（即形状的透明部分被忽略）边界框。 边界考虑了形状旋转。

## 例子

展示如何测量和缩放形状。

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// 验证 OfficeMath 对象在渲染时将创建的图像的大小。
Assert.AreEqual(119.0f, renderer.SizeInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.1f);

Assert.AreEqual(119.0f, renderer.BoundsInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.1f);

// 具有透明部分的形状可能在“OpaqueBoundsInPoints”属性中包含不同的值。
Assert.AreEqual(119.0f, renderer.OpaqueBoundsInPoints.Width, 0.2f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// 获取形状大小（以像素为单位），并线性缩放到特定 DPI。
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// 获取形状大小（以像素为单位），但水平和垂直尺寸具有不同的 DPI。
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(28, bounds.Height);

// 此处的不透明边界也可能有所不同。
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(30, bounds.Height);
```

### 也可以看看

* class [NodeRendererBase](../)
* 命名空间 [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* 部件 [Aspose.Words](../../../)
