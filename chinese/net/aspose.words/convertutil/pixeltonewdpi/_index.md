---
title: ConvertUtil.PixelToNewDpi
linktitle: PixelToNewDpi
articleTitle: PixelToNewDpi
second_title: Aspose.Words for .NET
description: 使用 ConvertUtil 的 PixelToNewDpi 方法轻松转换像素分辨率。为您的项目实现最佳图像质量和精度。
type: docs
weight: 30
url: /zh/net/aspose.words/convertutil/pixeltonewdpi/
---
## ConvertUtil.PixelToNewDpi method

将像素从一种分辨率转换为另一种分辨率。

```csharp
public static int PixelToNewDpi(double pixels, double oldDpi, double newDpi)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pixels | Double | 要转换的值。 |
| oldDpi | Double | 当前 dpi（每英寸点数）分辨率。 |
| newDpi | Double | 新的 dpi（每英寸点数）分辨率。 |

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
