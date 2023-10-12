---
title: HorizontalRuleFormat.Alignment
second_title: Aspose.Words for .NET API 参考
description: HorizontalRuleFormat 财产. 获取或设置水平线的对齐方式
type: docs
weight: 10
url: /zh/net/aspose.words.drawing/horizontalruleformat/alignment/
---
## HorizontalRuleFormat.Alignment property

获取或设置水平线的对齐方式。

```csharp
public HorizontalRuleAlignment Alignment { get; set; }
```

### 评论

默认值为Left。

### 例子

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

* enum [HorizontalRuleAlignment](../../horizontalrulealignment/)
* class [HorizontalRuleFormat](../)
* 命名空间 [Aspose.Words.Drawing](../../horizontalruleformat/)
* 部件 [Aspose.Words](../../../)


