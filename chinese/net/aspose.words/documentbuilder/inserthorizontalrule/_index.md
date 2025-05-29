---
title: DocumentBuilder.InsertHorizontalRule
linktitle: InsertHorizontalRule
articleTitle: InsertHorizontalRule
second_title: Aspose.Words for .NET
description: 使用 DocumentBuilder InsertHorizontalRule 方法增强您的文档，轻松添加时尚的水平线，以实现更好的组织和视觉吸引力。
type: docs
weight: 370
url: /zh/net/aspose.words/documentbuilder/inserthorizontalrule/
---
## DocumentBuilder.InsertHorizontalRule method

在文档中插入水平规则形状。

```csharp
public Shape InsertHorizontalRule()
```

### 返回值

水平线形状。

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

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
