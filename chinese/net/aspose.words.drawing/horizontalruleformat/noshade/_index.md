---
title: HorizontalRuleFormat.NoShade
linktitle: NoShade
articleTitle: NoShade
second_title: 用于 .NET 的 Aspose.Words
description: HorizontalRuleFormat NoShade 财产. 指示水平线存在 3D 阴影 如果真的则水平线没有 3D 阴影并使用纯色 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.drawing/horizontalruleformat/noshade/
---
## HorizontalRuleFormat.NoShade property

指示水平线存在 3D 阴影。 如果`真的`，则水平线没有 3D 阴影并使用纯色。

```csharp
public bool NoShade { get; set; }
```

## 评论

默认值为`错误的`。

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
