---
title: HorizontalRuleFormat.Alignment
linktitle: Alignment
articleTitle: Alignment
second_title: Aspose.Words for .NET
description: 探索 HorizontalRuleFormat Alignment 属性，轻松自定义水平规则的对齐方式，增强设计灵活性。
type: docs
weight: 10
url: /zh/net/aspose.words.drawing/horizontalruleformat/alignment/
---
## HorizontalRuleFormat.Alignment property

获取或设置水平规则的对齐方式。

```csharp
public HorizontalRuleAlignment Alignment { get; set; }
```

## 评论

默认值为Left。

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

* enum [HorizontalRuleAlignment](../../horizontalrulealignment/)
* class [HorizontalRuleFormat](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
