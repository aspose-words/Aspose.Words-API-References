---
title: HorizontalRuleFormat.Color
linktitle: Color
articleTitle: Color
second_title: 用于 .NET 的 Aspose.Words
description: HorizontalRuleFormat Color 财产. 获取或设置填充水平线的画笔颜色 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.drawing/horizontalruleformat/color/
---
## HorizontalRuleFormat.Color property

获取或设置填充水平线的画笔颜色。

```csharp
public Color Color { get; set; }
```

## 评论

这是一个快捷方式[`Color`](../../fill/color/)财产。

默认值为 Gray.

## 例子

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
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
