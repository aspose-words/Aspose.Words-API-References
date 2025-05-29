---
title: ShapeBase.IsHorizontalRule
linktitle: IsHorizontalRule
articleTitle: IsHorizontalRule
second_title: Aspose.Words for .NET
description: 发现 ShapeBase IsHorizontalRule 属性，轻松识别设计中的水平规则，以提高布局和样式效率。
type: docs
weight: 290
url: /zh/net/aspose.words.drawing/shapebase/ishorizontalrule/
---
## ShapeBase.IsHorizontalRule property

返回`真的`如果此形状是水平规则。

```csharp
public bool IsHorizontalRule { get; }
```

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

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
