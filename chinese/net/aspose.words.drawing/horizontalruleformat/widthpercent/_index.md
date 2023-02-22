---
title: HorizontalRuleFormat.WidthPercent
second_title: Aspose.Words for .NET API 参考
description: HorizontalRuleFormat 财产. 获取或设置指定水平线的长度以窗口宽度的百分比表示
type: docs
weight: 50
url: /zh/net/aspose.words.drawing/horizontalruleformat/widthpercent/
---
## HorizontalRuleFormat.WidthPercent property

获取或设置指定水平线的长度，以窗口宽度的百分比表示。

```csharp
public double WidthPercent { get; set; }
```

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentOutOfRangeException | 当参数超出有效值范围时抛出。 |

### 评论

有效值范围从 1 到 100（含）。

默认值为 100。

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


