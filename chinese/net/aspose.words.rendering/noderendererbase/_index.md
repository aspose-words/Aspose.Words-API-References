---
title: Class NodeRendererBase
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Rendering.NodeRendererBase 班级. 基类ShapeRenderer和OfficeMathRenderer.
type: docs
weight: 4290
url: /zh/net/aspose.words.rendering/noderendererbase/
---
## NodeRendererBase class

基类[`ShapeRenderer`](../shaperenderer/)和[`OfficeMathRenderer`](../officemathrenderer/).

```csharp
public abstract class NodeRendererBase
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BoundsInPoints](../../aspose.words.rendering/noderendererbase/boundsinpoints/) { get; } | 以点为单位获取形状的实际边界。 |
| [OpaqueBoundsInPoints](../../aspose.words.rendering/noderendererbase/opaqueboundsinpoints/) { get; } | 以点为单位获取形状的不透明边界。 |
| [SizeInPoints](../../aspose.words.rendering/noderendererbase/sizeinpoints/) { get; } | 以点为单位获取形状的实际大小。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/#getboundsinpixels)(float, float) | 计算指定缩放因子和分辨率的形状边界（以像素为单位）。 |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/#getboundsinpixels_1)(float, float, float) | 计算指定缩放因子和分辨率的形状边界（以像素为单位）。 |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/#getopaqueboundsinpixels)(float, float) | 计算指定缩放因子和分辨率下形状的不透明边界（以像素为单位）。 |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/#getopaqueboundsinpixels_1)(float, float, float) | 计算指定缩放因子和分辨率下形状的不透明边界（以像素为单位）。 |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/#getsizeinpixels)(float, float) | 计算指定缩放因子和分辨率的形状大小（以像素为单位）。 |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/#getsizeinpixels_1)(float, float, float) | 计算指定缩放因子和分辨率的形状大小（以像素为单位）。 |
| [RenderToScale](../../aspose.words.rendering/noderendererbase/rendertoscale/)(Graphics, float, float, float) | 将形状渲染为Graphics 对象到指定的比例。 |
| [RenderToSize](../../aspose.words.rendering/noderendererbase/rendertosize/)(Graphics, float, float, float, float) | 将形状渲染为Graphics 对象到指定的大小。 |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save)(Stream, ImageSaveOptions) | 将形状渲染成图像并保存到流中。 |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save_1)(string, ImageSaveOptions) | 将形状渲染成图像并保存到文件中。 |

### 例子

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

// 以像素为单位获取形状大小，线性缩放到特定的 DPI。
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// 以像素为单位获取形状大小，但水平和垂直尺寸使用不同的 DPI。
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(28, bounds.Height);

// 这里的不透明边界也可能不同。
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(30, bounds.Height);
```

### 也可以看看

* 命名空间 [Aspose.Words.Rendering](../../aspose.words.rendering/)
* 部件 [Aspose.Words](../../)


