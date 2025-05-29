---
title: LineSpacingRule Enum
linktitle: LineSpacingRule
articleTitle: LineSpacingRule
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.LineSpacingRule 枚举，实现可自定义的段落行距。通过精确控制增强文档格式，提升可读性。
type: docs
weight: 3890
url: /zh/net/aspose.words/linespacingrule/
---
## LineSpacingRule enumeration

指定段落的行距值。

```csharp
public enum LineSpacingRule
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| AtLeast | `0` | 行距可以大于或等于，但不能小于， 中指定的值[`LineSpacing`](../paragraphformat/linespacing/)属性. |
| Exactly | `1` | 行距始终与 中指定的值相同[`LineSpacing`](../paragraphformat/linespacing/)属性， 即使在段落中使用了较大的字体。 |
| Multiple | `2` | 行距在[`LineSpacing`](../paragraphformat/linespacing/) 属性表示线数。一条线等于 12 个点。 |

## 例子

展示如何使用行距。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 下面是我们可以使用以下三个行距规则来定义
// 段落的“LineSpacingRule”属性用于配置段落之间的间距。
// 1 - 设置最小间距。
// 这将为任意大小的文本行提供垂直填充
// 太小，无法维持最小行高。
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.AtLeast;
builder.ParagraphFormat.LineSpacing = 20;

builder.Writeln("Minimum line spacing of 20.");
builder.Writeln("Minimum line spacing of 20.");

// 2 - 设置精确间距。
// 使用对于间距来说过大的字体大小将会截断文本。
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Exactly;
builder.ParagraphFormat.LineSpacing = 5;

builder.Writeln("Line spacing of exactly 5.");
builder.Writeln("Line spacing of exactly 5.");

// 3 - 将间距设置为默认行距的倍数，默认为 12 点。
// 这种间距将适应不同的字体大小。
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Multiple;
builder.ParagraphFormat.LineSpacing = 18;

builder.Writeln("Line spacing of 1.5 default lines.");
builder.Writeln("Line spacing of 1.5 default lines.");

doc.Save(ArtifactsDir + "ParagraphFormat.LineSpacing.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
