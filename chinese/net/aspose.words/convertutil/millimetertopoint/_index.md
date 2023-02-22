---
title: ConvertUtil.MillimeterToPoint
second_title: Aspose.Words for .NET API 参考
description: ConvertUtil 方法. 将毫米转换为磅
type: docs
weight: 20
url: /zh/net/aspose.words/convertutil/millimetertopoint/
---
## ConvertUtil.MillimeterToPoint method

将毫米转换为磅。

```csharp
public static double MillimeterToPoint(double millimeters)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| millimeters | Double | 要转换的值。 |

### 评论

1 英寸等于 25.4 毫米。 1 英寸等于 72 磅。

### 例子

显示如何以毫米为单位指定页面属性。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 一个部分的“页面设置”定义了页边距的大小，以磅为单位。
// 我们也可以使用“ConvertUtil”类来使用更熟悉的度量单位，
// 例如定义边界时的毫米。
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.MillimeterToPoint(30);
pageSetup.BottomMargin = ConvertUtil.MillimeterToPoint(50);
pageSetup.LeftMargin = ConvertUtil.MillimeterToPoint(80);
pageSetup.RightMargin = ConvertUtil.MillimeterToPoint(40);

// 一厘米大约是 28.3 磅。
Assert.AreEqual(28.34d, ConvertUtil.MillimeterToPoint(10), 0.01d);

// 添加内容以演示新的边距。
builder.Writeln($"This Text is {pageSetup.LeftMargin} points from the left, " +
                $"{pageSetup.RightMargin} points from the right, " +
                $"{pageSetup.TopMargin} points from the top, " +
                $"and {pageSetup.BottomMargin} points from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndMillimeters.docx");
```

### 也可以看看

* class [ConvertUtil](../)
* 命名空间 [Aspose.Words](../../convertutil/)
* 部件 [Aspose.Words](../../../)


