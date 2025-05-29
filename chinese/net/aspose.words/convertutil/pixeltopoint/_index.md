---
title: ConvertUtil.PixelToPoint
linktitle: PixelToPoint
articleTitle: PixelToPoint
second_title: Aspose.Words for .NET
description: 使用 ConvertUtil 的 PixelToPoint 方法，轻松将像素转换为 96 dpi 的点。立即提升您的设计精度！
type: docs
weight: 40
url: /zh/net/aspose.words/convertutil/pixeltopoint/
---
## PixelToPoint(*double*) {#pixeltopoint}

将像素转换为 96 dpi 的点。

```csharp
public static double PixelToPoint(double pixels)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pixels | Double | 要转换的值。 |

## 评论

1 英寸等于 72 点。

## 例子

显示如何以像素为单位指定页面属性。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 部分“页面设置”定义页边距的大小（以点为单位）。
// 我们还可以使用“ConvertUtil”类来使用不同的测量单位，
// 例如定义边界时的像素。
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.PixelToPoint(100);
pageSetup.BottomMargin = ConvertUtil.PixelToPoint(200);
pageSetup.LeftMargin = ConvertUtil.PixelToPoint(225);
pageSetup.RightMargin = ConvertUtil.PixelToPoint(125);

// 一个像素等于0.75个点。
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1));
Assert.AreEqual(1.0d, ConvertUtil.PointToPixel(0.75));

// 使用的默认 DPI 值为 96。
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1, 96));

// 添加内容来演示新的边距。
builder.Writeln($"This Text is {pageSetup.LeftMargin} points/{ConvertUtil.PointToPixel(pageSetup.LeftMargin)} pixels from the left, " +
                $"{pageSetup.RightMargin} points/{ConvertUtil.PointToPixel(pageSetup.RightMargin)} pixels from the right, " +
                $"{pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin)} pixels from the top, " +
                $"and {pageSetup.BottomMargin} points/{ConvertUtil.PointToPixel(pageSetup.BottomMargin)} pixels from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndPixels.docx");
```

### 也可以看看

* class [ConvertUtil](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## PixelToPoint(*double, double*) {#pixeltopoint_1}

将像素转换为指定像素分辨率的点。

```csharp
public static double PixelToPoint(double pixels, double resolution)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pixels | Double | 要转换的值。 |
| resolution | Double | dpi（每英寸点数）分辨率。 |

## 评论

1 英寸等于 72 点。

## 例子

展示如何使用默认和自定义分辨率将点转换为像素。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 根据自定义 DPI，以像素为单位定义此部分顶部边距的大小。
const double myDpi = 192;

PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.PixelToPoint(100, myDpi);

Assert.AreEqual(37.5d, pageSetup.TopMargin, 0.01d);

// 在默认 DPI 96 下，一个像素等于 0.75 点。
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1));

builder.Writeln($"This Text is {pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin, myDpi)} " +
                $"pixels (at a DPI of {myDpi}) from the top of the page.");

// 设置新的 DPI 并相应调整顶部边距值。
const double newDpi = 300;
pageSetup.TopMargin = ConvertUtil.PixelToNewDpi(pageSetup.TopMargin, myDpi, newDpi);
Assert.AreEqual(59.0d, pageSetup.TopMargin, 0.01d);

builder.Writeln($"At a DPI of {newDpi}, the text is now {pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin, myDpi)} " +
                "pixels from the top of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndPixelsDpi.docx");
```

### 也可以看看

* class [ConvertUtil](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
