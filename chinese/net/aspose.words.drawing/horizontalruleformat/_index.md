---
title: HorizontalRuleFormat Class
linktitle: HorizontalRuleFormat
articleTitle: HorizontalRuleFormat
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.HorizontalRuleFormat 类，实现高级水平线格式设置。轻松提升您的文档设计！
type: docs
weight: 1380
url: /zh/net/aspose.words.drawing/horizontalruleformat/
---
## HorizontalRuleFormat class

表示水平规则格式。

要了解更多信息，请访问[使用形状](https://docs.aspose.com/words/net/working-with-shapes/)文档文章。

```csharp
public class HorizontalRuleFormat
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Alignment](../../aspose.words.drawing/horizontalruleformat/alignment/) { get; set; } | 获取或设置水平规则的对齐方式。 |
| [Color](../../aspose.words.drawing/horizontalruleformat/color/) { get; set; } | 获取或设置填充水平规则的画笔颜色。 |
| [Height](../../aspose.words.drawing/horizontalruleformat/height/) { get; set; } | 获取或设置水平规则的高度。 |
| [NoShade](../../aspose.words.drawing/horizontalruleformat/noshade/) { get; set; } | 表示水平线存在 3D 阴影。 如果`真的`，则水平线不带 3D 阴影，并使用纯色。 |
| [WidthPercent](../../aspose.words.drawing/horizontalruleformat/widthpercent/) { get; set; } | 获取或设置指定水平规则的长度，以窗口宽度的百分比表示。 |

## 例子

展示如何插入水平线形状并自定义其格式。

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
