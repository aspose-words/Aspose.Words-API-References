---
title: ConvertUtil.MillimeterToPoint
linktitle: MillimeterToPoint
articleTitle: MillimeterToPoint
second_title: Aspose.Words for .NET
description: 使用 ConvertUtil 的 MillimeterToPoint 方法，轻松将毫米转换为点。立即简化您的设计计算！
type: docs
weight: 20
url: /zh/net/aspose.words/convertutil/millimetertopoint/
---
## ConvertUtil.MillimeterToPoint method

将毫米转换为点。

```csharp
public static double MillimeterToPoint(double millimeters)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| millimeters | Double | 要转换的值。 |

## 评论

1 英寸等于 25.4 毫米。1 英寸等于 72 点。

## 例子

显示如何以毫米为单位指定页面属性。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 部分“页面设置”定义页边距的大小（以点为单位）。
// 我们还可以使用“ConvertUtil”类来使用更熟悉的测量单位，
// 例如定义边界时的毫米数。
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.MillimeterToPoint(30);
pageSetup.BottomMargin = ConvertUtil.MillimeterToPoint(50);
pageSetup.LeftMargin = ConvertUtil.MillimeterToPoint(80);
pageSetup.RightMargin = ConvertUtil.MillimeterToPoint(40);

// 一厘米约为 28.3 点。
Assert.AreEqual(28.34d, ConvertUtil.MillimeterToPoint(10), 0.01d);

// 添加内容来演示新的边距。
builder.Writeln($"This Text is {pageSetup.LeftMargin} points from the left, " +
                $"{pageSetup.RightMargin} points from the right, " +
                $"{pageSetup.TopMargin} points from the top, " +
                $"and {pageSetup.BottomMargin} points from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndMillimeters.docx");
```

### 也可以看看

* class [ConvertUtil](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
