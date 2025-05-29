---
title: HorizontalRuleAlignment Enum
linktitle: HorizontalRuleAlignment
articleTitle: HorizontalRuleAlignment
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.HorizontalRuleAlignment 枚举，以精确控制水平规则对齐，增强文档格式和设计。
type: docs
weight: 1370
url: /zh/net/aspose.words.drawing/horizontalrulealignment/
---
## HorizontalRuleAlignment enumeration

表示指定水平规则的对齐方式。

```csharp
public enum HorizontalRuleAlignment
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Left | `0` | 左对齐。 |
| Center | `1` | 对齐中心。 |
| Right | `2` | 右对齐。 |

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

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
