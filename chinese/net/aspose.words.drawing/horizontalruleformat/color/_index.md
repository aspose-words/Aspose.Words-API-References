---
title: HorizontalRuleFormat.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words for .NET
description: 探索 HorizontalRuleFormat Color 属性，自定义您的设计。轻松设置或获取画笔颜色，打造惊艳的水平线效果！
type: docs
weight: 20
url: /zh/net/aspose.words.drawing/horizontalruleformat/color/
---
## HorizontalRuleFormat.Color property

获取或设置填充水平规则的画笔颜色。

```csharp
public Color Color { get; set; }
```

## 评论

这是[`Color`](../../fill/color/)财产。

默认值为 Gray.

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

* class [HorizontalRuleFormat](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
