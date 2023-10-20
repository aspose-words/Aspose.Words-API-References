---
title: HorizontalRuleFormat Class
linktitle: HorizontalRuleFormat
articleTitle: HorizontalRuleFormat
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Drawing.HorizontalRuleFormat 班级. 表示水平线格式化 在 C#.
type: docs
weight: 1050
url: /zh/net/aspose.words.drawing/horizontalruleformat/
---
## HorizontalRuleFormat class

表示水平线格式化。

要了解更多信息，请访问[使用形状](https://docs.aspose.com/words/net/working-with-shapes/)文档文章。

```csharp
public class HorizontalRuleFormat
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Alignment](../../aspose.words.drawing/horizontalruleformat/alignment/) { get; set; } | 获取或设置水平线的对齐方式。 |
| [Color](../../aspose.words.drawing/horizontalruleformat/color/) { get; set; } | 获取或设置填充水平线的画笔颜色。 |
| [Height](../../aspose.words.drawing/horizontalruleformat/height/) { get; set; } | 获取或设置水平线的高度。 |
| [NoShade](../../aspose.words.drawing/horizontalruleformat/noshade/) { get; set; } | 指示水平线存在 3D 阴影。 如果`真的`，则水平线没有 3D 阴影并使用纯色。 |
| [WidthPercent](../../aspose.words.drawing/horizontalruleformat/widthpercent/) { get; set; } | 获取或设置指定水平线的长度，以窗口宽度的百分比表示。 |

## 例子

演示如何插入水平标尺形状并自定义其格式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertHorizontalRule();

HorizontalRuleFormat horizontalRuleFormat = shape.HorizontalRuleFormat;
horizontalRuleFormat.Alignment = HorizontalRuleAlignment.Center;
horizontalRuleFormat.WidthPercent = 70;
horizontalRuleFormat.Height = 3;
horizontalRuleFormat.Color = Color.Blue;
horizontalRuleFormat.NoShade = true;

Assert.True(shape.IsHorizontalRule);
Assert.True(shape.HorizontalRuleFormat.NoShade);
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
