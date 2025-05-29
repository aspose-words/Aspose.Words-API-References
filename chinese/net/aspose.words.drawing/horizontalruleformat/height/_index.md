---
title: HorizontalRuleFormat.Height
linktitle: Height
articleTitle: Height
second_title: Aspose.Words for .NET
description: 轻松调整水平线的高度。探索高度属性，为您的网页项目提供可定制的设计。立即优化您的布局！
type: docs
weight: 30
url: /zh/net/aspose.words.drawing/horizontalruleformat/height/
---
## HorizontalRuleFormat.Height property

获取或设置水平规则的高度。

```csharp
public double Height { get; set; }
```

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentOutOfRangeException | 当参数超出有效值范围时抛出。 |

## 评论

这是[`Height`](../../shapebase/height/)财产。

有效值范围为 0 至 1584（含）。

默认值为 1.5。

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
