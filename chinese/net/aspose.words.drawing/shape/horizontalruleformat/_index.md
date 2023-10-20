---
title: Shape.HorizontalRuleFormat
linktitle: HorizontalRuleFormat
articleTitle: HorizontalRuleFormat
second_title: 用于 .NET 的 Aspose.Words
description: Shape HorizontalRuleFormat 财产. 提供对水平标尺形状属性的访问 对于不是水平标尺的形状返回无效的 在 C#.
type: docs
weight: 100
url: /zh/net/aspose.words.drawing/shape/horizontalruleformat/
---
## Shape.HorizontalRuleFormat property

提供对水平标尺形状属性的访问。 对于不是水平标尺的形状，返回`无效的`.

```csharp
public HorizontalRuleFormat HorizontalRuleFormat { get; }
```

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

* class [HorizontalRuleFormat](../../horizontalruleformat/)
* class [Shape](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
