---
title: NodeRendererBase.GetBoundsInPixels
linktitle: GetBoundsInPixels
articleTitle: GetBoundsInPixels
second_title: Aspose.Words for .NET
description: 探索 NodeRendererBase GetBoundsInPixels 方法，根据缩放和分辨率准确计算像素中的形状尺寸，从而提高精度。
type: docs
weight: 40
url: /zh/net/aspose.words.rendering/noderendererbase/getboundsinpixels/
---
## GetBoundsInPixels(*float, float*) {#getboundsinpixels}

计算指定缩放系数和分辨率的形状边界（以像素为单位）。

```csharp
public Rectangle GetBoundsInPixels(float scale, float dpi)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| scale | Single | 缩放系数（1.0 为 100%）。 |
| dpi | Single | 从点转换为像素（每英寸点数）的分辨率（水平和垂直）。 |

### 返回值

形状的实际（在页面上呈现）边界框（以像素为单位）。

## 评论

此方法将[`BoundsInPoints`](../boundsinpoints/)以像素为单位转换成矩形。

## 例子

展示如何测量和缩放形状。

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// 验证 OfficeMath 对象在我们渲染时将创建的图像的大小。
Assert.AreEqual(122.0f, renderer.SizeInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.15f);

Assert.AreEqual(122.0f, renderer.BoundsInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.15f);

// 具有透明部分的形状可能在“OpaqueBoundsInPoints”属性中包含不同的值。
Assert.AreEqual(122.0f, renderer.OpaqueBoundsInPoints.Width, 0.25f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// 获取形状大小（以像素为单位），并线性缩放至特定的 DPI。
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// 获取形状大小（以像素为单位），但水平和垂直尺寸使用不同的 DPI。
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(27, bounds.Height);

// 不透明边界在这里也可能有所不同。
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(19, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(29, bounds.Height);
```

### 也可以看看

* class [NodeRendererBase](../)
* 命名空间 [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* 部件 [Aspose.Words](../../../)

---

## GetBoundsInPixels(*float, float, float*) {#getboundsinpixels_1}

计算指定缩放系数和分辨率的形状边界（以像素为单位）。

```csharp
public Rectangle GetBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| scale | Single | 缩放系数（1.0 为 100%）。 |
| horizontalDpi | Single | 从点转换为像素（每英寸点数）的水平分辨率。 |
| verticalDpi | Single | 从点转换为像素（每英寸点数）的垂直分辨率。 |

### 返回值

形状的实际（在页面上呈现）边界框（以像素为单位）。

## 评论

此方法将[`BoundsInPoints`](../boundsinpoints/)以像素为单位转换成矩形。

## 例子

展示如何测量和缩放形状。

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// 验证 OfficeMath 对象在我们渲染时将创建的图像的大小。
Assert.AreEqual(122.0f, renderer.SizeInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.15f);

Assert.AreEqual(122.0f, renderer.BoundsInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.15f);

// 具有透明部分的形状可能在“OpaqueBoundsInPoints”属性中包含不同的值。
Assert.AreEqual(122.0f, renderer.OpaqueBoundsInPoints.Width, 0.25f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// 获取形状大小（以像素为单位），并线性缩放至特定的 DPI。
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// 获取形状大小（以像素为单位），但水平和垂直尺寸使用不同的 DPI。
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(27, bounds.Height);

// 不透明边界在这里也可能有所不同。
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(19, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(29, bounds.Height);
```

### 也可以看看

* class [NodeRendererBase](../)
* 命名空间 [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* 部件 [Aspose.Words](../../../)
