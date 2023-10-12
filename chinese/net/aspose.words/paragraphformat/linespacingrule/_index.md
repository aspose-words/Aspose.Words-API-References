---
title: ParagraphFormat.LineSpacingRule
second_title: Aspose.Words for .NET API 参考
description: ParagraphFormat 财产. 获取或设置段落的行距
type: docs
weight: 200
url: /zh/net/aspose.words/paragraphformat/linespacingrule/
---
## ParagraphFormat.LineSpacingRule property

获取或设置段落的行距。

```csharp
public LineSpacingRule LineSpacingRule { get; set; }
```

### 例子

展示如何使用行间距。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 下面是我们可以使用以下三个行间距规则来定义
// 段落的“LineSpacingRule”属性用于配置段落之间的间距。
// 1 - 设置最小间距。
// 这将为任意大小的文本行提供垂直填充
// 太小而无法维持最小行高。
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.AtLeast;
builder.ParagraphFormat.LineSpacing = 20;

builder.Writeln("Minimum line spacing of 20.");
builder.Writeln("Minimum line spacing of 20.");

// 2 - 设置精确的间距。
// 使用对于间距来说太大的字体会截断文本。
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Exactly;
builder.ParagraphFormat.LineSpacing = 5;

builder.Writeln("Line spacing of exactly 5.");
builder.Writeln("Line spacing of exactly 5.");

// 3 - 将间距设置为默认行距的倍数，默认为 12 点。
// 这种间距会缩放到不同的字体大小。
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Multiple;
builder.ParagraphFormat.LineSpacing = 18;

builder.Writeln("Line spacing of 1.5 default lines.");
builder.Writeln("Line spacing of 1.5 default lines.");

doc.Save(ArtifactsDir + "ParagraphFormat.LineSpacing.docx");
```

### 也可以看看

* enum [LineSpacingRule](../../linespacingrule/)
* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../paragraphformat/)
* 部件 [Aspose.Words](../../../)


