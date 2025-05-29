---
title: ConvertUtil.PointToInch
linktitle: PointToInch
articleTitle: PointToInch
second_title: Aspose.Words for .NET
description: 使用 ConvertUtil 的 PointToInch 方法轻松将磅转换为英寸。立即简化您的测量并提升设计精度！
type: docs
weight: 50
url: /zh/net/aspose.words/convertutil/pointtoinch/
---
## ConvertUtil.PointToInch method

将点转换为英寸。

```csharp
public static double PointToInch(double points)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| points | Double | 要转换的值。 |

## 评论

1 英寸等于 72 点。

## 例子

显示如何以英寸为单位指定页面属性。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 部分“页面设置”定义页边距的大小（以点为单位）。
// 我们还可以使用“ConvertUtil”类来使用更熟悉的测量单位，
// 例如定义边界时的英寸。
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
pageSetup.BottomMargin = ConvertUtil.InchToPoint(2.0);
pageSetup.LeftMargin = ConvertUtil.InchToPoint(2.5);
pageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);

// 一英寸等于 72 点。
Assert.AreEqual(72.0d, ConvertUtil.InchToPoint(1));
Assert.AreEqual(1.0d, ConvertUtil.PointToInch(72));

// 添加内容来演示新的边距。
builder.Writeln($"This Text is {pageSetup.LeftMargin} points/{ConvertUtil.PointToInch(pageSetup.LeftMargin)} inches from the left, " +
                $"{pageSetup.RightMargin} points/{ConvertUtil.PointToInch(pageSetup.RightMargin)} inches from the right, " +
                $"{pageSetup.TopMargin} points/{ConvertUtil.PointToInch(pageSetup.TopMargin)} inches from the top, " +
                $"and {pageSetup.BottomMargin} points/{ConvertUtil.PointToInch(pageSetup.BottomMargin)} inches from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndInches.docx");
```

### 也可以看看

* class [ConvertUtil](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
