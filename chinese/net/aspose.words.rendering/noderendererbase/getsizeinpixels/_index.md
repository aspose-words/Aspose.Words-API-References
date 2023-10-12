---
title: NodeRendererBase.GetSizeInPixels
second_title: Aspose.Words for .NET API 参考
description: NodeRendererBase 方法. 计算指定缩放系数和分辨率下形状的大小以像素为单位
type: docs
weight: 60
url: /zh/net/aspose.words.rendering/noderendererbase/getsizeinpixels/
---
## GetSizeInPixels(float, float) {#getsizeinpixels}

计算指定缩放系数和分辨率下形状的大小（以像素为单位）。

```csharp
public Size GetSizeInPixels(float scale, float dpi)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| scale | Single | 缩放系数（1.0 为 100%）。 |
| dpi | Single | 从点转换为像素（每英寸点数）的分辨率（水平和垂直）。 |

### 返回值

形状的大小（以像素为单位）。

### 评论

这个方法转换[`SizeInPoints`](../sizeinpoints/)以像素为单位的大小，当您想要创建一个位图以将形状整齐地渲染到位图上时，它很有用 。

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
* 命名空间 [Aspose.Words.Rendering](../../noderendererbase/)
* 部件 [Aspose.Words](../../../)

---

## GetSizeInPixels(float, float, float) {#getsizeinpixels_1}

计算指定缩放系数和分辨率下形状的大小（以像素为单位）。

```csharp
public Size GetSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| scale | Single | 缩放系数（1.0 为 100%）。 |
| horizontalDpi | Single | 从点转换为像素（每英寸点数）的水平分辨率。 |
| verticalDpi | Single | 从点转换为像素（每英寸点数）的垂直分辨率。 |

### 返回值

形状的大小（以像素为单位）。

### 评论

这个方法转换[`SizeInPoints`](../sizeinpoints/)以像素为单位的大小，当您想要创建一个位图以将形状整齐地渲染到位图上时，它很有用 。

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
* 命名空间 [Aspose.Words.Rendering](../../noderendererbase/)
* 部件 [Aspose.Words](../../../)


