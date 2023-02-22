---
title: HorizontalRuleFormat.Height
second_title: Aspose.Words for .NET API 参考
description: HorizontalRuleFormat 财产. 获取或设置水平尺的高度
type: docs
weight: 30
url: /zh/net/aspose.words.drawing/horizontalruleformat/height/
---
## HorizontalRuleFormat.Height property

获取或设置水平尺的高度。

```csharp
public double Height { get; set; }
```

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentOutOfRangeException | 当参数超出有效值范围时抛出。 |

### 评论

这是一个快捷方式[`Height`](../../shapebase/height/)财产。

有效值范围从 0 到 1584（含）。

默认值为 1.5。

### 例子

显示如何插入水平线形，并自定义其格式。

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
* 命名空间 [Aspose.Words.Drawing](../../horizontalruleformat/)
* 部件 [Aspose.Words](../../../)


