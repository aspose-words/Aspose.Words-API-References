---
title: HorizontalRuleFormat.Height
linktitle: Height
articleTitle: Height
second_title: 用于 .NET 的 Aspose.Words
description: HorizontalRuleFormat Height 财产. 获取或设置水平线的高度 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.drawing/horizontalruleformat/height/
---
## HorizontalRuleFormat.Height property

获取或设置水平线的高度。

```csharp
public double Height { get; set; }
```

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentOutOfRangeException | 当参数超出有效值范围时抛出。 |

## 评论

这是一个快捷方式[`Height`](../../shapebase/height/)财产。

有效值范围从 0 到 1584（含）。

默认值为 1.5。

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

* class [HorizontalRuleFormat](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
